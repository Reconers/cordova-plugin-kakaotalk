KakaoTalk Cordova Plugin
========================

A plugman compatible Cordova plugin for the KakaoTalk(https://developers.kakao.com)

Make sure you've registered your app with Kakao and to have an KAKAO_APP_KEY

Cordova Install Note:
========================

cordova plugin add https://github.com/reconers/cordova-plugin-kakaotalk --variable KAKAO_APP_KEY=%KAKAO_APP_KEY%


How to use the plugin
========================

### Usage

This plugin adds an object to the window. Right now, you can only login and logout.

##### Login

Login using the `.login` method:
```
KakaoTalk.login(
    function (result) { // success
        console.log('Successful login!');
		console.log(result);
    },
    function (message) { // error
        console.log('Error logging in');
		console.log(message);
    }
);
```

The login reponse object is defined as:
```
{
  id: '<KakaoTalk User Id>',
  nickname: '<KakaoTalk User Nickname>',
  profile_image: '<KakaoTalk User ProfileImage>'
}
```

##### Logout

Logout using the `.logout` method:
```
Kakaotalk.logout(
	function() {
		console.log('Successful logout!');
	}, function() {
		console.log('Error logging out');
	}
);
```
