<section id="user-input">
    <!--- This is the main user input section a form tag wraps the inputs we want to collect -->
    <form method="get">
        <div>
            <!-- This is a single input, it has a label and a input field for the user to enter information into. The name signifies the variable the input will be stored in -->
            <label for="adjective1">Adjective</label>
            <input type="text" name="adjective1" placeholder="adjective" />
        </div>
        <!-- Button for the user to click when submiting the form -->
        <input type="submit" />
    </form>
</section>

<!-- The madlib we will populate -->
<section id="madlib">
    <!-- we wrap the mad lib in a paragraph tag, inside of this we will need something to place the text into that the user submits. I am using a span because it displays on the page inline instead of something that would cause a linebreak to happen, such as another p tag or div.  The id is a tag we can use to specify which field this is, I am naming it the same as the name on the form input to keep things simple, it could be anything as long as it is unique. -->
    <p>I said <span id="adjective1"></span></p>
</section>

<!-- We will be putting code inside of script to handle the logic of how to handle the madlib population -->
<script>

function add_value(entry) {
  $("#" + entry["name"]).text(entry["value"])
}

function submit_event(event) {
    event.preventDefault();
    var entries = $(this).serializeArray()
    entries.forEach(add_value(entry))
}

$("#user-input").find("form").submit(submit_event(event))
</script>