# Ember Routing Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  What are the main task(s) you perform inside the Ember Application Router,
    and what are the main task(s) you perform inside an Ember Route?

    ```md
    The router is where we set the paths that calls go through.
    This controlls the url that is displayed, where the information goes,
    and what information we are sending to that route.
    ```

1.  What is the command to generate a route named `boston` nested under
    `campus`?

    ```md
    ember g route campus/boston
    ```

1.  Suppose you have a nested route at the URL `/campus/boston`. How would you
    use the `link-to` helper to generate an appropriate link?

    ```md
    {{#link-to 'campus.boston'}}Boston Campus{{/link-to}}
    ```

1.  Explain **at least** two differences between the following two route
    definitions.

    ```js
    this.route('products', function () {
      this.route('product', { path: '/:product_id' }); // <= 👀here
    });

    this.route('product', { path: '/products/:product_id' }); // <= 👀 here
    ```

    ```md
    The first route definition defines a route to products as well as a
    path to product that passes over product_id information. The second one
    only defines the route to product and it passes the product_id from
    products. The first one is also nesting the product path under products.
    ```

1.  Suppose we have the following route definition:

    ```js
    this.route('movie', { path: '/movies/:movie_id' }); // <= 👀 here
    ```

    If we navigate in the browser to `/movies/123`, how can we reference the
    value `'123'` inside a Route?

    ```md
    In order to get the information we would need to call it directly
    and refer to the location in the array using -1 to adjust the position.
    ```

1.  Inside a template, how do we reference data provided by a Route?

    ```md
    we would use the same named variable that we are passing over in the
    route.
    ```
