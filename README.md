<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Yasir Tractor Service</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 0; padding: 0; background: #f2f2f2; }
        header { background: #d32f2f; color: white; padding: 20px; text-align: center; }
        .section { padding: 20px; background: white; margin: 15px; border-radius: 10px; }
        .btn { background: #d32f2f; color: white; padding: 10px 20px; display: inline-block; border-radius: 5px; text-decoration: none; }
        footer { background: #333; color: white; text-align: center; padding: 10px; margin-top: 20px; }
        input, select, textarea { width: 100%; padding: 10px; margin: 8px 0; border-radius: 5px; border: 1px solid #999; }
    </style>
</head>
<body>

<header>
    <h1>Yasir Tractor Service</h1>
    <p>भरोसेमंद ट्रैक्टर हल & जुताई सेवा</p>
</header>

<div class="section">
    <h2>हमारी सेवाएँ</h2>
    <p>हल जुताई – <b>₹1000 प्रति घंटा</b></p>
    <p>रूटावेटर – <b>₹1000 प्रति घंटा</b></p>
</div>

<!-- ONLINE BOOKING FORM -->
<div class="section">
    <h2>🟢 Online Booking Form</h2>

    <form id="bookingForm">
        <label>नाम :</label>
        <input type="text" id="name" required>

        <label>मोबाइल नंबर :</label>
        <input type="text" id="mobile" required>

        <label>लोकेशन / एड्रेस :</label>
        <textarea id="location" required></textarea>

        <label>सर्विस चुनें :</label>
        <select id="service">
            <option value="हल जुताई">हल जुताई</option>
            <option value="रोटावेटर">रोटावेटर</option>
        </select>

        <label>कितनी बीघा जमीन :</label>
        <input type="number" id="bigha" placeholder="उदाहरण: 2.5" required>

        <label>तारीख चुनें :</label>
        <input type="date" id="date" required>

        <label>समय चुनें :</label>
        <input type="time" id="time" required>

        <button type="button" class="btn" onclick="sendWhatsApp()">WhatsApp पर Booking भेजें</button>
    </form>
</div>

<script>
function sendWhatsApp() {
    let name = document.getElementById("name").value;
    let mobile = document.getElementById("mobile").value;
    let location = document.getElementById("location").value;
    let service = document.getElementById("service").value;
    let bigha = document.getElementById("bigha").value;
    let date = document.getElementById("date").value;
    let time = document.getElementById("time").value;

    let message = 
        `🚜 *Yasir Tractor Booking*\n\n` +
        `👤 नाम: ${name}\n` +
        `📞 मोबाइल: ${mobile}\n` +
        `📍 लोकेशन: ${location}\n` +
        `🛠 सर्विस: ${service}\n` +
        `🌾 बीघा: ${bigha}\n` +
        `📅 तारीख: ${date}\n` +
        `⏰ समय: ${time}`;

    let phone = "8084738669"; // आपका WhatsApp नंबर

    let url = `https://wa.me/${phone}?text=` + encodeURIComponent(message);

    window.open(url, "_blank");
}
</script>


<div class="section">
