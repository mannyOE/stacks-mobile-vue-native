<template>
	<app-navigator></app-navigator>
</template>

<script>
import {createAppContainer, createStackNavigator} from 'vue-native-router'

import HomeScreen from './views/auth/login.vue'
import RegisterScreen from './views/auth/signup.vue'
import VerifyScreen from './views/auth/verify.vue'

import ForgotView from './views/auth/forgot-password.vue'
import ResetView from './views/auth/reset-password.vue'

const StackNavigator = createStackNavigator(
	{
		Home: {
			screen: HomeScreen,
			navigationOptions: {
				headerShown: false
			}
		},
		Register: {
			screen: RegisterScreen,
			navigationOptions: {
				headerShown: false
			}
		},
		Verify: {
			screen: VerifyScreen,
			navigationOptions: {
				headerShown: false
			}
		},
		Reset: {
			screen: ResetView,
			navigationOptions: {
				headerShown: false
			}
		},
		Forgot: {
			screen: ForgotView,
			navigationOptions: {
				headerShown: false
			}
		}
	},
	{
		initialRouteName: 'Home'
	}
)

const AppNavigator = createAppContainer(StackNavigator)

import Vue from 'vue-native-core'
import {VueNativeBase} from 'native-base'

// registering all native-base components to the global scope of the Vue
Vue.use(VueNativeBase)
export default {
	components: {AppNavigator},
	data: function () {
		return {
			btnTitle: 'Click Me',
			btnClickCount: 0
		}
	},
	methods: {
		handleBtnClickCount: function () {
			this.btnClickCount = this.btnClickCount + 1
		}
	}
}
</script>

<style>
.container {
	background-color: #ffffff;
	align-items: center;
	justify-content: center;
	flex: 1;
}
.text-color-primary {
	color: blue;
}
</style>
