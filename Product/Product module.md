### Links
- [[Product.attribute]]
- [[Product.attribute.value]]
- [[Product.category]]
- [[Product.product]]
- [[Product.template]]
- [[Template.attribute.line]]
- [[Template attribute value]]
- [[Product/Template.attribute.custom.value]]
- [[Uom.uom]]

### Overview

The product module is one of Odoo's main module. [[Stock module]] and [[MRP]] directly depends on it
Here is a general explanation of the architecture of the [[Product module]].

##### [[Product.product|Product]] and [[Product.template|template]]

The product concept in Odoo is related to the real-world product concept.

On the first level we find [[Product.product|product]] which represent the real 'concrete product' that is based on a [[Product.template|template]]. That product is called a [[Product.product|variant]].
	***Example*** *: two same socks with different colors would translate to the sock being the template and the green sock and red sock being the variants*

##### [[Template.attribute.line]]

The [[Product.template|template]] may have [[Template.attribute.line||attribute.line]] which translates to a summary of all attributes that are available on the template. Each line has the [[Product.attribute|product.attribute]] it refers to and all the [[Product.attribute.value|values]] related to that attribute.
	***Example*** *: let's take the same example as before. The product template is the sock, and the attributes lines could be the color and the size. Each of those attributes have different values: 🟢 green and 🔴 red for the color and S,M and L for the size.*

##### [[Template.attribute.custom.value]]

In some cases, you may want a [[Template.attribute.custom.value|custom values]] on some of your [[Template.attribute.line|attribute lines]]. 
	***Example*** *: let's say you want to personalize your sock with a custom color. In that case you can create a custom value on your product attribute that will allow to enter your own color.*

For now those custom values are entered in a [[sale.order]] thanks to the [[Product configurator|product configurator]] and are displayed in the [[Production|manufacturing order]] view and the [[Shop floor|shop floor]]. 
