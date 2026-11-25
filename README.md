
<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Digital Clock</title>

<style>
    body {
        margin: 0;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        background: #080808;
        font-family: Arial, sans-serif;
        color: white;
    }

    .clock {
        text-align: center;
        padding: 40px;
        border: 2px solid #00ffff;
        border-radius: 20px;
        box-shadow: 0 0 25px #00ffff;
    }

    h1 {
        color: #00ffff;
        font-size: 25px;
    }

    #time {
        font-size: 65px;
        font-weight: bold;
        color: #00ffff;
        text-shadow: 0 0 20px #00ffff;
    }

    #date {
        font-size: 20px;
        margin-top: 15px;
        color: #ffffff;
    }
</style>
</head>

<body>

<div class="clock">
    <h1> DIGITAL CLOCK </h1>
    <div id="time">00:00:00</div>
    <div id="date"></div>
</div>

<script>
function updateClock() {
    const now = new Date();

    let hours = String(now.getHours()).padStart(2, '0');
    let minutes = String(now.getMinutes()).padStart(2, '0');
    let seconds = String(now.getSeconds()).padStart(2, '0');

    document.getElementById("time").innerHTML =
        `${hours}:${minutes}:${seconds}`;

    document.getElementById("date").innerHTML =
        now.toLocaleDateString('th-TH', {
            day: 'numeric',
            month: 'long',
            year: 'numeric'
        });
}

setInterval(updateClock, 1000);
updateClock();
</script>

</body>
</html>
