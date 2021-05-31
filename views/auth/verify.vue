<template>
	<nb-container class="container">
		<nb-header transparent>
			<nb-body>
				<nb-text class="header"> Verify your account </nb-text>
			</nb-body>
		</nb-header>
		<nb-content padder>
			<nb-container class="content">
				<nb-form>
					<nb-item floatingLabel>
						<nb-label class="text-light">Verification Code</nb-label>
						<nb-input
							class="text-light"
							:keyboardAppearance="'dark'"
							:autoCapitalize="false"
						/>
					</nb-item>
					<nb-button class="btn" full>
						<nb-text class="text-light">Verify Account</nb-text>
					</nb-button>

					<nb-button v-bind:onPress="openHome" class="btn" transparent full>
						<nb-text>Already have an account? Login</nb-text>
					</nb-button>
				</nb-form>
			</nb-container>
		</nb-content>
	</nb-container>
</template>

<script>
export default {
	props: {
		navigation: {
			type: Object
		}
	},
	data: function () {
		return {}
	},
	methods: {
		openHome() {
			this.navigation.navigate('Home')
		}
	}
}
</script>

<style>
.container {
	background-color: #03293d;
	color: red;
}

.content {
	background-color: #03293d;
	align-items: stretch;
	justify-content: center;
}

.btn {
	margin-top: 20px;
}
.header {
	color: #fff;
	font-weight: 900;
	font-size: 25px;
}

.text-color-primary {
	color: #fff;
	margin-top: 10px;
}
.text-light {
	color: #fff;
	font-weight: 700;
	line-height: 25px;
}
</style>
