<script>
  import logo from './assets/svelte.png';
  import Counter from './lib/Counter.svelte';

  // @ts-ignore
  const Algebra = window.Algebra;
  // I THINK PROBLEM IS NAMESPACE CONFLICT WITH DOM 'Element' class and Ganja.js Element class

  var Complex = Algebra(0,1);
  console.log(Complex);
  var result = Algebra(0,1,()=>(3+2e1)*(1+4e1));
  console.log(result);
  // console.log(Algebra(0,1).inline(()=>(3+2e1)*(1+4e1)));
</script>

<main>
  <img src={logo} alt="Svelte Logo" />
  <h1>Hello world!</h1>

  <Counter />
</main>

<style>
  :root {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
      Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }

  main {
    text-align: center;
    padding: 1em;
    margin: 0 auto;
  }

  img {
    height: 16rem;
    width: 16rem;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4rem;
    font-weight: 100;
    line-height: 1.1;
    margin: 2rem auto;
    max-width: 14rem;
  }

  p {
    max-width: 14rem;
    margin: 1rem auto;
    line-height: 1.35;
  }

  @media (min-width: 480px) {
    h1 {
      max-width: none;
    }

    p {
      max-width: none;
    }
  }
</style>
