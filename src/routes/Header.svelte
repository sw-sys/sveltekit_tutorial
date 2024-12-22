<script>
    // Destructure the `name` prop passed to this component
    let { name } = $props();

    // Object defining character replacements (e.g., 'e' becomes '3', 'l' becomes '1')
    const replacements = {
        e: '3',  // Replace 'e' with '3'
        l: '1',  // Replace 'l' with '1'
        a: '@',  // Replace 'a' with '@'
        o: '0',  // Replace 'o' with '0'
        s: '$',  // Replace 's' with '$'
    };

    // Function to transform the name string by replacing specific characters
    const transformName = (str) => {
        // Use a regular expression to match the characters in the replacements object
        // and replace them using the corresponding value from the replacements object
        return str.replace(/[elaso]/g, (char) => replacements[char] || char);
    };

    let message = "Hello, world!";
</script>

<!-- Display the original name  -->
<h1>Hello {name}</h1>

<!-- Display the transformed name using the transformName function -->
133tised:
<h2>{transformName(name)}</h2>
  
  <div class="example">
    {message}
  </div>
  
  <style lang="postcss">
    .example {
      display: flex;
      background: linear-gradient(45deg, #f06, transparent);
      &::after {
        content: " (Styled with PostCSS)";
      }
    }
  </style>
  