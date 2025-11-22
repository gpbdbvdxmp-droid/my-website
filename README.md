<div id="result"></div>

  <script>
    function generatePassword() {
      const name = document.getElementById('name').value.trim();
      const number = document.getElementById('number').value.trim();
      const emoji = document.getElementById('emoji').value.trim();
      const crush = document.getElementById('crush').value.trim();
      const song = document.getElementById('song').value.trim();
      const mood = document.getElementById('mood').value.trim();

      let base = name.slice(0,3) + crush.slice(-2) + mood.slice(0,2);
      let randomChunk = Math.random().toString(36).slice(2,6);

      const password = `${base}${number}${emoji}${randomChunk}`;
      document.getElementById('result').innerText = password;
    }
  </script>
</body>
</html>
