<!DOCTYPE html>
<html>
  <body>
    <main>
      <h1>Rap Legends</h1>
      <section>
        <h2>Top Rap Moments</h2>
        <p>Witness more <a target="_blank" href="https://raplegends.com">epic rap moments</a> in our gallery.</p>
        <a href="https://raplegends.com"><img src="https://images5.alphacoders.com/869/thumb-1920-869330.jpg" alt="A dynamic rap performance in action."></a>
      </section>
      <section>
        <h2>Rap Icons</h2>
        <h3>Legendary rap artists:</h3>
        <ul>
          <li>Eminem</li>
          <li>Tupac Shakur</li>
          <li>Notorious B.I.G.</li>
        </ul>
        <button id="add-player">Add Player</button>
      </section>
      <section>
        <h2>Join the Rap Enthusiasts Community</h2>
        <form action="https://raplegends.com/submit-rap-photo">
          <fieldset>
            <legend>Are you an Rap enthusiast?</legend>
            <label><input id="yes" type="radio" name="enthusiast" value="yes"> Yes</label>
            <label><input id="no" type="radio" name="enthusiast" value="no"> No</label>
          </fieldset>
          <fieldset>
            <legend>Who is your favorite Rap artist?</legend>
            <select name="favorite-artist" id="favorite-artist">
              <option value="eminem">Eminem</option>
              <option value="tupac">Tupac Shakur</option>
              <option value="biggie">Notorious B.I.G.</option>
            </select>
          </fieldset>
          <input type="text" name="rapphotourl" placeholder="Rap photo URL" required>
          <button type="submit">Submit</button>
        </form>
      </section>
    </main>
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <script>
      $(document).ready(function() {
        $("#add-player").click(function() {
          var newPlayerName = prompt("Enter the name of the new player:");
          if (newPlayerName) {
            $("ul").append("<li>" + newPlayerName + "</li>");
          }
        });
        $("form").submit(function(event) {
          event.preventDefault();
          var selectedPlayer = $("#favorite-player").val();
          var photoUrl = $("input[name='nbaphotourl']").val();
          alert("Favorite artist: " + selectedPlayer + "\nRap Photo URL: " + photoUrl);
        });
      });
    </script>
  </body>
</html>
