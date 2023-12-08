```python:
name = fields.Char
create_variant = fields.Selection(['always','dynamic','no_variant'])
display_type = fields.Selection(['radio', 'pills', 'select', 'color'])
sequence = fields.Integer
value_ids = fields.One2many(comodel_name='product.attribute.value')
attribute_line_ids = fields.One2many(comodel_name='product.template.attribute.line')
product_tmpl_ids = fields.Many2many(comodel_name='product.template')
number_related_products = fields.Integer
```
