.. |foundation| replace:: Foundation 4
.. _foundation: http://foundation.zurb.com/

=======================
Sphinx Foundation Theme
=======================

This is a Sphinx theme based on the |foundation|_ css framework.

Usage
-----

#.	Make the ``foundation`` package available either by installing it through PyPi
	or by including in the ``PYTHONPATH`` in ``conf.py``.
#.	Set the ``html_theme`` variable to ``'foundation'``.
#.	You also need to add the ``foundation`` extension in the ``conf.py``.
	This is neccessary for creation of the top bar navigation.

.. code-block:: python
	
	sys.path[0:0] = [os.path.abspath('_themes/foundation_sphinx_theme')]
	html_theme = 'foundation'
	extensions = ['sphinx.ext.autodoc', 'foundation']

Styles
^^^^^^

There are two ready made styles.

*	``foundation/css/basic.css``
*	``foundation/css/cards.css``

If you want to customize them or make your own style.
Extend the ``sass`` sources in ``foundation/static/foundation/sass``.


Options
^^^^^^^

There are these theme options available:

.. code-block:: python
	
	html_theme_options = {
		'motto': 'Long description which appears next to logo.',

		# Your stylesheet elative to the _static dir.
		# Default is 'foundation/css/basic.css'
		'stylesheet': '/path/to/your/stylesheet.css',

		# Logo image in SVG format. If the browser doesn't support SVG
		# It will try to load JPG with the same name.
		'logo_screen': '',

		# Logo for small screens. If ommited, logo_screen will be used.
		'logo_mobile': '',

		# Path to your favicon.ico file relative to the _static dir.
		'favicon': '',

		# Use this if the top-level items of the toctree don't fit in the top-bar navigation.
		# If True, the whole toctree will be placed inside a single top-level item.
		'top_bar_force_fit': True,

		# The title of the aformentioned top-level item. Default is "Sections"
		'top_bar_content_title': 'Sections',

		# If both are set, a google analytics code will be appended to body of each page.
		'google_analytics_id': 'your-google-analytics-id',
		'google_analytics_domain': 'example.com',

		# The "og:title", "og:type", "og:url", "og:site_name" and "og:description" Open Graph tags
		# will be generated automatically, but you should specify the
		# path to the image that you want to be used
		# in the required "og:image" property relative to the _static dir.
		'opengraph_image': 'path/to/your/opengraph-image.jpg',

		# Any custom additional OG tags
		'opengraph_tags': {
			'foo': 'bar', # will be rendered as <meta property="og:foo" content="bar" />
		},

		# The "description" meta tag will be created automatically, but
		# you can specify additional meta tags here.
		'meta_tags': {
			'foo': 'bar', # will be rendered as <meta name="foo" content="bar">
		},

		# Use this as the base for Open Graph URLs without trailing slash.
		'base_url': 'http://example.com',
   }
