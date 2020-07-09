<script>
  import "../node_modules/materialize-css/dist/css/materialize.min.css";
  // import "../node_modules/materialize-css/dist/js/materialize.min.js";

  import { Router, Route } from "svelte-routing";

  import Navbar from "./layout/Navbar.svelte";
  import Home from "./pages/Home.svelte";
  import Pluralization from "./pages/Pluralization.svelte";
  import Numbers from "./pages/Numbers.svelte";
  import DateTime from "./pages/DateTime.svelte";
  
      import { dictionary, locale } from 'svelte-i18n';
    
    // ...
    dictionary.set({
        en: {
            app: {
                title: 'Internationalization',
                subtitle: 'Getting started with localization',
            },
        },
        ar: {
            app: {
                title: 'تدويل',
                subtitle: 'الشروع في التعريب',
            },
        },
        fr: {
            app: {
                title: 'Internationalisation',
                subtitle: 'Premiers pas avec la localisation',
            },
        },
    });
    locale.set('fr');
</script>

<style>

</style>

<Router>
  <Navbar />
  <div class="container">
    <Route path="/" component={Home} />
    <Route path="/pluralization" component={Pluralization} />
    <Route path="/numbers" component={Numbers} />
    <Route path="/datetime" component={DateTime} />
  </div>
</Router>
