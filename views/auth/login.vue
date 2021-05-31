<template>
	<nb-container class="container">
		<nb-header transparent>
			<nb-body>
				<nb-text class="header"> Login to continue </nb-text>
			</nb-body>
		</nb-header>
		<nb-content padder>
			<nb-container class="content">
				<nb-form>
					<nb-item floatingLabel>
						<nb-label class="text-light">Email Address</nb-label>
						<nb-input
							class="text-light"
							:keyboardAppearance="'dark'"
							:autoCapitalize="false"
							keyboardType="email-address"
						/>
					</nb-item>
					<nb-item floatingLabel>
						<nb-label class="text-light">Password</nb-label>
						<nb-input
							:keyboardAppearance="'dark'"
							:autoCapitalize="false"
							class="text-light"
							secureTextEntry
						/>
					</nb-item>
					<nb-button class="btn" full>
						<nb-text class="text-light">Sign In</nb-text>
					</nb-button>

					<nb-button v-bind:onPress="openRegister" class="btn" transparent full>
						<nb-text>Create your new account</nb-text>
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
		openRegister() {
			this.navigation.navigate('Register')
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
