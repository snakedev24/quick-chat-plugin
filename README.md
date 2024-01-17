What is Quick Chat shortcode for embedding chat room into post or page?
You can do that by placing [quick-chat] (including [] brackets) inside post or page where you want your chat to appear. This short code will use all default options. If you need to change some of default options you can use shortcode attributes. Here's Quick Chat shortcode with all atributes and their default values included.

[quick-chat height="400" room="default" userlist="1" userlist_position="left" smilies="1" send_button="0" loggedin_visible="1" guests_visible="1" avatars="1" counter="1"]

Shortcode attributes details:

height - You control Quick Chat height by giving height attribute to the [quick-chat] shortcode. For example to have 600 pixels high Quick Chat message history container embedded on your page you would add [quick-chat height="600"] inside page where you want your chat to appear. If you omit height attribute default height is 400 pixels. *** room - You can give room attribute to the [quick-chat] shortcode. So if you want your embedded chat to show chat room identified by word "musictalk" you will display this chat like this:** [quick-chat room="musictalk"]. Every chat (sidebar or in-post) with "musictalk" room attribute will show this same content. If you omit room shortcode attribute, default behavior is to show predefined chat room identified by the "default" word.

userlist - If you wan't to hide user list you can set this shortcode attribute value to 0 like this [quick-chat userlist="0"].

userlist_position - To use embedded chat with user list on the left side of your chat room you can embedd it into your post or page using [quick-chat userlist_position="left"] shortcode. You can also use "top" and "right" values for userlist_position shortcode attribute.

smilies - If you wan't to hide emoticons container you can set this shortcode attribute value to 0 like this [quick-chat smilies="0"].

send_button - Messages are submited using Enter key on your keyboard. Additionally to control send button visibility you can use "send_button" shortcode attribute. To embed Quick Chat with send button displayed you can use [quick-chat send_button="1"] shortcode.

loggedin_visible, guests_visible - When using embedded chat you can use "loggedin_visible" and "guests_visible" shortcode attributes whose value can be "0" to hide chat room for specified user group or "1" to display it. Default value for both "loggedin_visible" and "guests_visible" shortcode atributes is "1", so this means that if you omit this shortcode attributes chat will be displayed to all users. For example to display chat room only to logged in users and hide it for guests you can use [quick-chat loggedin_visible="1" guests_visible="0"] shortcode.

avatars - You use "avatars" shortcode attribute whose value can be "0" to hide avatars or "1" to show them. To embed Quick Chat with avatars hidden you can use following shortcode [quick-chat avatars="0"].

counter - You use "counter" shortcode attribute whose value can be "0" to hide characters left counter or "1" to show it. To embed Quick Chat with counter hidden you can use following shortcode [quick-chat counter="0"].

How do I configure chat room options when using Quick Chat sidebar widget?
Every short code attribute setting has equivalent widget option setting. This way you can control all sidebar widget options available to chat room embedded to page or post using shortcode.

Can you tell me more about Quick Chat PHP caching plugins support?
Caching plugin support is tested with WP Super Cache and W3 Total Cache and my custom caching solution where Quick Chat automatically clears cache when necessary. If you use some other caching plugin you should manually clear cache every time you change any of quick chat options, modify shortcode, sidebar widget options or similar. PHP caching compatibility is achieved using AJAX to load and operate chat.

My theme has no widget support. How can I embed Quick Chat into my web site using PHP?
To embed Quick Chat on your page using PHP you can use following PHP code:

<?php global $quick_chat; if(is_object($quick_chat) && method_exists($quick_chat, 'quick_chat')){ echo $quick_chat->quick_chat(400, 'default', 1, 'left', 0, 0, 1, 1, 1, 1); ?> } ?> 

You can replace "400" with wanted Quick Chat message history window height and 'default' with your chat room name. The third parameter should be 1 when you want to display user list (0 otherwise) and fourth parameter will decide where will user list be placed ('right', 'left' or 'top'). Fifth parameter will decide will smilies be displayed (1) or hidden (0). Sixth parameter can take value (0) to hide send button and (1) to display it. Last two parameters can take value (0) to hide chat for logged in users (7th parameter) or guests (8th parameter) and (1) to display it. Last two parameters determine will avatars and character counter be displayed (1) or hidden (0).

What are the requirements for Quick Chat audio notification features?
Quick Chat can use sound to notify you of incoming messages. For this feature to work you need modern HTML5 audio tag enabled browser like Mozilla Firefox 3.5+, Google Chrome 6+, Opera 10.5+ or Internet Explorer 9 (IE works but not recommended).

Can I change messages notification sound?
Sure you can. You just replace "message-sound.mp3", "message-sound.ogg" and "message-sound.wav" from your "wp-content/plugins/quick-chat/sounds" directory with your own message notification sound files. Three sound file types are necessary because not all HTML5 audio tag enabled browsers support all audio file formats.

How should I configure timeout options inside General section of Quick Chat admin options?
Generally the lower you go with timing options the more stress is put to your server but your chat is more responsive. Default values are optimal so please don't go overboard with making them much lower.

How do I use private chat?
To initiate private chat with another chat user click his chat user name on the list of chat users. Simultaneously you can have multiple one on one private chat sessions. Quick Chat administrator users can control who is allowed to initiate private chat session (logged in users and/or guests) from Quick Chat admin options.

Where can I find my chat room transcripts?
You can find all of your chat room transcript files inside your "wp-content/plugins/quick-chat/transcripts" directory.

What's up with the private message clean up available from the inside of Quick Chat options, private chat options section?
Even if you can't see them, Quick Chat private chat invitations and private chat messages are left inside your WordPress database after private chat sessions and can in time pile up to slow down your Quick Chat. You should periodically clean those to keep Quick Chat database sparkling clean (preferably when no private chat sessions are in progress).

What happened to Quick Chat translating abilities?
Translation feature has been removed as of Quick Chat 4.00 version because Microsoft has converted its translation service into paid service

30. How do I enable or disable country flags on my chat user list?
Quick Chat is using Quick Flag WordPress plugin to resolve IP address to country flag so to enable this feature you must install and activate Quick Flag plugin. To hide country flag display you can deactivate Quick Flag plugin or enable "Disable Quick Flag WordPress plugin integration" checkbox in Quick Count admin options.

31. How do I Avoid losing CSS customizations after Quick Chat update?
After Quick Chat loads its own CSS file it will search for quick-chat.css file inside your current theme directory. If this file exists Quick Chat will load it after its own CSS file. CSS customizations placed inside quick-chat.css file inside your theme directory wont be lost after Quick Chat upgrade (be aware that your theme upgrade will probably delete this file).
