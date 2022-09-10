<script>
  export /**
* @type {string | null | undefined}
*/
   let type;
  export /**
* @type {any}
*/
   let caption;
</script>

  <button {type}>{caption}</button>

<style>
  button,
  a {
    font: inherit;
    border: 1px solid #ffffff;
    background: #161925;
    padding: 0.5rem 1rem;
    color: #ffffff;
    border-radius: 5px;
    box-shadow: 1px 1px 3px rgba(0, 0, 0, 0.26);
    cursor: pointer;
    text-decoration: none;
  }

  button:focus {
    outline: none;
  }

  button:hover,
  button:active,
  a:hover,
  a:active {
    background: #6B91A4;
    border-color: #6B91A4;
    color:#1F2937;
    box-shadow: 1px 1px 8px rgba(77, 51, 51, 0.26);
  }

  button:disabled,
  button:disabled:hover,
  button:disabled:active {
    background: #ccc;
    border-color: #ccc;
    color: #CBF7ED;
    box-shadow: none;
    cursor: not-allowed;
  }

</style>



