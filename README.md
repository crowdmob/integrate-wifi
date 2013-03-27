Wi-Fi Captive Portal Integration
==============

Here's how to integrate our platform onto your Wi-Fi access point.

From your Wi-Fi's administration console, go to the section where you input the 


Here's the URL format we integrate:

`http://crave.crowdmob.com/incoming?source_name={WIFI_PARTNER_ID}&device_uuid_type=mac_address&device_uuid={SMARTPHONEORTABLET_MAC_ADDRESS}&access_point_uuid={STRING_UNIQUELY_IDENTIFYING_ACCESSPOINT}&next={NO_THANKS_REDIRECT_URL}&no_ads={CROWDMOB_NO_INVENTORY_REDIRECT_URL}`

`{WIFI_PARTNER_ID}` - Provided by CrowdMob account manager; this would be `thechicagometro`, for the Chicago Metro Downtown Crowne Plaza

`{SMARTPHONEORTABLET_MAC_ADDRESS}` - This would be a macro typically defined in the Wi-Fi AP administration area

`{STRING_UNIQUELY_IDENTIFYING_ACCESSPOINT}` - This would be a macro typically defined in the Wi-Fi AP administration area

`{NO_THANKS_REDIRECT_URL}` - a percent-encoded url to send the user if they click no-thanks link

`{CROWDMOB_NO_INVENTORY_REDIRECT_URL}` - a percent-encoded url to send the user if we don't have any ads to show (if it's a device we don't understand; can be a backup network)

Example:
==============
`http://crave.crowdmob.com/incoming?source_name=thechicagometro&device_uuid_type=mac_address&device_uuid=11:11:11:11:11&access_point_uuid=lobby-1&next=http:%2F%2Fthechicagometro.weebly.com&no_ads=http:%2F%2Fthechicagometro.weebly.com`
