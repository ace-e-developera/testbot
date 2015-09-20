console.log("hello");

var TelegramBot = require('node-telegram-bot-api');
var token = '133394201:AAE93LJDmZSinI1CHUf_XwN1ooC8RjSyZQY';

var port = process.env.OPENSHIFT_NODEJS_PORT;
var host = process.env.OPENSHIFT_NODEJS_IP;

var bot = new TelegramBot(token, {webHook: {port: port, host: host}});
bot.setWebHook('applicationname-testbot.rhcloud.com:443/bot' + token);

bot.on('message', function (msg) {
	var chatId = msg.chat.id;
	var chatName = msg.chat.first_name;
	if (msg.text == "hi"){
		bot.sendMessage(chatId, "Hi dear " + chatName + "! :-)");
	}
});
