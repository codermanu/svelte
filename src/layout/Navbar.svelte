<script>
  import { Link } from "svelte-routing";
</script>

<nav>
  <div class="nav-wrapper">
    <div class="container">
      <Link to="/">
        <span class="brand-logo">Svelte Localization Tutorial</span>
      </Link>
      <ul id="nav-mobile" class="right hide-on-med-and-down">
        <li>
          <Link to="/">Home</Link>
        </li>
        <li>
          <Link to="/pluralization">Pluralization</Link>
        </li>
        <li>
          <Link to="/datetime">DateTime</Link>
        </li>
        <li>
          <Link to="/numbers">Numbers and Currency</Link>
        </li>
      </ul>
    </div>
  </div>
</nav>
