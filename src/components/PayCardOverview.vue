<template>
	<ion-grid class="grid">
		<ion-row class="first-row">
			<ion-col>
					<ion-icon :icon="arrowBack" @click="back"></ion-icon>
			</ion-col>
			<ion-col>
				<div class="balance">Balance</div>
				<br />
				<div class="amount">R 7 658</div>
			</ion-col>
		</ion-row>

		<ion-row>
			<ion-col>
				Favorites
			</ion-col>
			<ion-col>
				All users
			</ion-col>
			<ion-col>
				New users
			</ion-col>
		</ion-row>

	</ion-grid>
</template>

<script>
import { IonGrid, IonRow, IonCol, IonIcon } from "@ionic/vue";
import { arrowBack } from 'ionicons/icons';

export default {
	name: "pay-card-overview",
	components: { IonGrid, IonRow, IonCol, IonIcon },
  setup() {
    return {
			arrowBack
    }
  },
  methods: {
		back() {
			this.$router.back();
		}
	}
}
</script>

<style lang="scss" scoped>
.grid {
	border-radius: 0 0 40px 40px;
	background: #ffffff;
	height: 160px;
	padding: 5px 0 0 35px;
	margin: -15px -15px 15px -15px;
}

.first-row {
	margin: 10px 0px 30px 0;
}

.amount, .balance {
	color: #000000;
}

.amount {
	font-size: 25px;
  margin-top: 10px;
}

ion-col {
	padding-right: 20px;
	div {
		float: right;
	}

	ion-icon {
		float: left;
    font-size: 22px;
    background: #e0e0e0;
    padding: 8px 16px 8px 10px;
    margin-left: -42px;
		border-radius: 0 11px 11px 0;
	}
}

</style>
