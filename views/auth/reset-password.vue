<template>
	<nb-container class="container">
		<nb-header transparent>
			<nb-body>
				<nb-text class="header"> Reset your password </nb-text>
			</nb-body>
		</nb-header>
		<nb-content padder>
			<nb-container class="content">
				<nb-form>
					<nb-item floatingLabel>
						<nb-label class="text-light">Password</nb-label>
						<nb-input
							:keyboardAppearance="'dark'"
							:autoCapitalize="false"
							class="text-light"
							secureTextEntry
						/>
					</nb-item>
					<nb-item floatingLabel>
						<nb-label class="text-light">Confirm Password</nb-label>
						<nb-input
							:keyboardAppearance="'dark'"
							:autoCapitalize="false"
							class="text-light"
							secureTextEntry
						/>
					</nb-item>
					<nb-button class="btn" full>
						<nb-text class="text-light">Reset your password</nb-text>
					</nb-button>
					<nb-button class="btn" transparent full>
						<nb-text>Resend Verification Code</nb-text>
					</nb-button>
					<nb-button v-bind:onPress="openHome" class="" transparent full>
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
.header {
	color: #fff;
	font-weight: 900;
	font-size: 25px;
}
.btn {
	margin-top: 20px;
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
