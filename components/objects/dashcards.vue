<template>
	<div>
		<v-container>
			<v-row>
				<v-col>
					<h3 class="font-weight-medium">Welcome to Wired Market Space</h3>
				</v-col>

				<v-col>
					<span>Filter By</span>
					<v-btn outlined  tile text >Day</v-btn>
					<v-btn  outlined tile text >Week</v-btn>
					<v-btn outlined  tile text >Month</v-btn>
					<v-btn outlined tile text >Total</v-btn>
					
				</v-col>
			</v-row>

			<v-row>
				<v-col v-for="(card,key) in carddata" :key=key cols=4>
					<v-card :color="card.color" class="elevation-10 pa-4" tile dark >

						<h2 class="text-center" >{{card.cardname}}<v-icon right large>{{card.icon}}</v-icon></h2>
						<h3 class="text-center">{{card.count}}</h3>
						<v-icon large right>mdi-finance</v-icon>
						
					</v-card>
				</v-col>
			</v-row>
		</v-container>
	</div>
</template>

<script type="text/javascript">
	export default{
		data(){
			return{
				carddata:[
				{
					cardname:"Total Orders",
					icon:"mdi-briefcase-check",
					count:134,
					color:"pink darken-3"
				},
				{
					cardname:"Total Income",
					icon:"mdi-cash-multiple",
					count:"134$",
					color:"light-blue darken-4"
				},

				{
					cardname:"Site Traffic",
					icon:"mdi-account-multiple",
					count:"134 views",
					color:"green darken-4"
				},


				]
			}
		}
	}
</script>

<style scoped>
h3.text-center{
	font-size: 30px;
}
</style>