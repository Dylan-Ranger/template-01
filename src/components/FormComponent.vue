<template>
	<div>
		<ion-label>Amount</ion-label>
		<br />
		<ion-input type="number" placeholder="R 0.00" />
		<ion-grid>
			<ion-row>
				<ion-col v-for="(item, index) in tokens" :key="index" class="tokens">
					{{ item }}
				</ion-col>
			</ion-row>
			<ion-row class="reason-wrapper">
			<ion-item>
				<ion-label class="reason">Reason</ion-label>
				<ion-select aria-label="Select One">
					<ion-select-option value="payment">Payment</ion-select-option>
					<ion-select-option value="transfer">Transfer</ion-select-option>
					<ion-select-option value="refund">Refund</ion-select-option>
				</ion-select>
			</ion-item>
			</ion-row>
		</ion-grid>
	</div>
</template>

<script>
import { IonGrid, IonRow, IonCol, IonLabel, IonInput, IonSelectOption, IonSelect, IonItem } from "@ionic/vue";

export default {
	name: "form-component",
	components: { IonGrid, IonRow, IonCol, IonLabel, IonInput, IonSelectOption, IonSelect, IonItem },
  data() {
		return {
			tokens: ["R 25", "R 50", "R 100", "R 200"]
		}
	}
}
</script>

<style lang="scss" scoped>
ion-label {
	font-weight: bold;
}

ion-input {
	background: #fff;
	border-radius: 20px;
	padding: 5px 8px !important;
	margin: 10px 0;
}

.tokens {
	background: #fff;
	border-radius: 20px;
	font-weight: bold;
	margin: 5px;
	text-align: center;
	padding: 7px;
}

.reason-wrapper {
	margin: 10px 0;
	background: #ffffff;
	// padding: 9px;
	border-radius: 20px;

	.reason {
		border-right: 2px grey solid;
	}

	.reason-options {
		margin-left: 15px;
	}
}

ion-item {
	width: 100%;
	--background: none; 
}
</style>
