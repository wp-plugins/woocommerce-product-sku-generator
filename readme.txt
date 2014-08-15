=== WooCommerce Product SKU Generator ===
Contributors: beka.rice, skyverge
Tags: woocommerce, sku, product sku
Donate link: https://www.paypal.com/cgi-bin/webscr?cmd=_xclick&business=paypal@skyverge.com&item_name=Donation+for+WooCommerce+SKU+Generator
Requires at least: 3.8
Tested up to: 3.9.1
Requires WooCommerce at least: 2.1
Tested WooCommerce up to: 2.2-beta
Stable Tag: 1.1
License: GPLv3
License URI: http://www.gnu.org/licenses/gpl-3.0.html

Automatically generate WooCommerce product SKUs from the product slug and/or variation attributes.

== Description ==

> **Requires: WooCommerce 2.1+**

Automatically generate a SKU for parent / simple products, variations, or both when the product is published or updated. Generated SKUs for parent / simple products will use the product slug for the SKU.

If the product is a variable product, this plugin can append attributes for each variation to the SKU to differentiate between them. If you opt to generate all SKUs, the variation attributes will be appended to the product slug. If you only generate variation SKUs, the variation attributes will be appended to whatever you set for the parent SKU.

> **IMPORTANT:** The SKU field will be disabled for simple products and parent products if you generate them using this plugin. Your own SKUs previously assigned to products will be overridden if you update a product, and they will change if you change your product slug. Be sure you want to complete automate SKUs if you leave this enabled all of the time.

You can also selectively enable and disable the plugin if you don't want to override existing SKUs when saving products. You can [view product documentation](http://www.skyverge.com/product/woocommerce-product-sku-generator/) for help.

= Features =
This plugin provides options to:

 - automatically generate simple / parent product SKUs when the product is published or updated using the product slug
 - generate SKUs for product variations using the parent SKU + variation attributes
 - generate both the parent and variation SKUs automatically
 - use the bulk product update action to easily generate SKUs for products created before installing this plugin.

= SKUs for all product types =
The WooCommerce Product SKU generator allows you to determine whether all products, parent / simple products, or product variations should have automatically generated SKUs.

If parent /simple product SKUs are generated, product SKUs will be generated any time a product is published or updated. For example, a product with a slug 'wp-tee-shirt' will have an SKU of 'wp-tee-shirt' (even if this is a parent product of a variable product). The SKU can change if the product slug changes.

= Variable Products =
You can enable SKU creation for variable products under **WooCommerce &gt; Settings &gt; Products** as well. Should you choose to create unique SKUs for each product variation, the attributes for that variation will be appended to the parent SKU.

Let's say you generate SKUs for all products. For a variable product whose parent is 'wp-tee-shirt', the SKU will first use the parent slug, then append the attributes for each variation. For example, if the shirt has a small variation in white, the SKU for that variation will be 'wp-tee-shirt-small-white'.

If you **only** generate SKUs for variations, you can set the parent SKU. If the parent SKU for the same shirt is 1234, the generated SKU will instead look like '1234-small-white'.

If you only create parent / simple SKUs, you will be able to manually create your own variation SKUs, as these will not be overridden by saving or updating a product.

= Bulk Updating =
You can bulk add SKUs to products that you've created prior to installing this plugin. If you select the products you want to update, then bulk edit them, all you have to do is hit "Update". When the products are saved, SKUs will be generated for all products.

This action will also automatically generate the SKUs for product variations if you have them enabled.

= More Details =
 - See the [product page](http://www.skyverge.com/product/woocommerce-product-sku-generator/) for full details and documentation
 - View more of SkyVerge's [free WooCommerce extensions](http://profiles.wordpress.org/skyverge/)
 - View all [SkyVerge WooCommerce extensions](http://www.skyverge.com/shop/)

== Installation ==

1. Be sure you're running WooCommerce 2.1+
2. Upload the entire 'woocommerce-product-sku-generator' folder to the '/wp-content/plugins/' directory
3. Activate the plugin through the 'Plugins' menu in WordPress
4. Go to **WooCommerce &gt; Settings &gt; Products** and scroll down to "Product Data". Here you have the option to generate SKUs for only simple / parent products, variations, or both.
5. View [documentation on the product page](http://www.skyverge.com/product/woocommerce-product-sku-generator/) for more help if needed.

**NOTE that** any time a product is updated, its SKU will be generated, so this may override old SKUs if you update products. This plugin is meant for complete SKU automation, or you can selectively enable / disable it as needed.

== Frequently Asked Questions ==
= What happens to my old SKUs? =
This plugin generates SKUs any time products are created or updated. Your old SKUs will be overridden if you use it - **only** leave the plugin enabled if you don't want to manage SKUs yourself.

You can also selectively disable and re-enable the plugin if you don't want to override SKUs when saving products.

= What happens to variation SKUs? =
Variation SKUs can be overridden if you're not automatically generated them. They will be overridden if you auto-generate them, then try to change them manually. If you'd like to change an SKU for a product, disable the plugin, change the SKU, and update the product. You can re-enable the plugin as needed.

= How do I add SKUs to old products? =
Select the products you'd like to generate SKUs for under **Products**. Go to the bulk actions in the top left and click "Edit", then apply. All you need to do is hit "Update" to save these products, and SKUs will automatically be added.

= This is handy! Can I contribute? =
Yes you can! Join in on our [GitHub repository](https://github.com/bekarice/woocommerce-product-sku-generator/) and submit a pull request :)

== Screenshots ==
1. Plugin Settings
2. Automatic SKU generation upon publish / update
3. Automatic variation SKUs based on attributes (if enabled)
4. Variation SKU generated when you set the parent SKU (if you only generate variation SKUs)

== Changelog ==
= 2014.08.12 - version 1.1 =
 * New: Option to generate only variation SKUs automatically

= 2014.07.23 - version 1.0.2 =
 * Fix: Changed SKU disable method to remove javascript

= 2014.06.13 - version 1.0.1 =
 * Re-versioned + incremented for bug fix
 * Fix: javascript issue during WooCommerce update
 
= 2014.04.15 - version 0.1 =
 * Initial Release
