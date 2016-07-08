# check_amazon
Nagios/Icinga plugin to check Amazon.co.uk for product prices

This monitoring plugin is a simple shell script that accepts the Amazon product ID (Amazon Standard Identification Number, ASIN) as a mandatory parameter. It uses lynx to fetch the Amazon page for that item. Somewhere in the lynx-output is the information about the full name and the price of the product. Various grep commands filter the output, cut and tr remove sections and characters. As a result, the script prints the name of the item and the current price.
The check_amazon plugin accepts two optional parameters: -w for the warning threshold (= the price is near to what you'd like to pay for it) and -c for the critical threshold (= the price is now below the maximum price you're prepared to pay).

More information on https://www.icinga.org/2016/07/08/watch-out-and-shop/

Antony Stone <Antony.Stone@Open.Source.IT>, Heike Jurzik <jurzik@linux-journalist.com>
