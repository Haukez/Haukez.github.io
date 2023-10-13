<script>
  import svelteLogo from "./assets/svelte.svg";
  import viteLogo from "/vite.svg";
  import Counter from "./lib/Counter.svelte";
</script>

<main>
  <div>
    <a href="https://vitejs.dev" target="_blank" rel="noreferrer">
      <img src={viteLogo} class="logo" alt="Vite Logo" />
    </a>
    <a href="https://svelte.dev" target="_blank" rel="noreferrer">
      <img src={svelteLogo} class="logo svelte" alt="Svelte Logo" />
    </a>
  </div>
  <h1>Vite + Svelte</h1>

  <div class="card">
    <div id="product-component-1697225035656" />
    <script type="text/javascript">
      /*<![CDATA[*/
      (function () {
        var scriptURL =
          "https://sdks.shopifycdn.com/buy-button/latest/buy-button-storefront.min.js";
        if (window.ShopifyBuy) {
          if (window.ShopifyBuy.UI) {
            ShopifyBuyInit();
          } else {
            loadScript();
          }
        } else {
          loadScript();
        }
        function loadScript() {
          var script = document.createElement("script");
          script.async = true;
          script.src = scriptURL;
          (
            document.getElementsByTagName("head")[0] ||
            document.getElementsByTagName("body")[0]
          ).appendChild(script);
          script.onload = ShopifyBuyInit;
        }
        function ShopifyBuyInit() {
          var client = ShopifyBuy.buildClient({
            domain: "87987a-5.myshopify.com",
            storefrontAccessToken: "ffc899282b4c3b228f56cd2617700829",
          });
          ShopifyBuy.UI.onReady(client).then(function (ui) {
            ui.createComponent("product", {
              id: "8728990548303",
              node: document.getElementById("product-component-1697225035656"),
              moneyFormat: "%E2%82%AC%7B%7Bamount_with_comma_separator%7D%7D",
              options: {
                product: {
                  styles: {
                    product: {
                      "@media (min-width: 601px)": {
                        "max-width": "calc(25% - 20px)",
                        "margin-left": "20px",
                        "margin-bottom": "50px",
                      },
                    },
                  },
                  text: {
                    button: "Add to cart",
                  },
                },
                productSet: {
                  styles: {
                    products: {
                      "@media (min-width: 601px)": {
                        "margin-left": "-20px",
                      },
                    },
                  },
                },
                modalProduct: {
                  contents: {
                    img: false,
                    imgWithCarousel: true,
                    button: false,
                    buttonWithQuantity: true,
                  },
                  styles: {
                    product: {
                      "@media (min-width: 601px)": {
                        "max-width": "100%",
                        "margin-left": "0px",
                        "margin-bottom": "0px",
                      },
                    },
                  },
                  text: {
                    button: "Add to cart",
                  },
                },
                option: {},
                cart: {
                  text: {
                    total: "Subtotal",
                    button: "Checkout",
                  },
                },
                toggle: {},
              },
            });
          });
        }
      })();
      /*]]>*/
    </script>
  </div>

  <p>
    Check out <a
      href="https://github.com/sveltejs/kit#readme"
      target="_blank"
      rel="noreferrer">SvelteKit</a
    >, the official Svelte app framework powered by Vite!
  </p>

  <p class="read-the-docs">Click on the Vite and Svelte logos to learn more</p>
</main>

<style>
  .logo {
    height: 6em;
    padding: 1.5em;
    will-change: filter;
    transition: filter 300ms;
  }
  .logo:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
  }
  .logo.svelte:hover {
    filter: drop-shadow(0 0 2em #ff3e00aa);
  }
  .read-the-docs {
    color: #888;
  }
</style>
