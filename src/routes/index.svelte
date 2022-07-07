<script>
    const url = "https://zenquotes.io/api/quotes/";
    let quote_txt = "";

    async function quote() {

        const response = await fetch(url, {
            mode: "no-cors"
        });
        quote_txt = await response.json();
    }

    quote()
</script>

<head>
	<link href="https://fonts.googleapis.com/css2?family=Inter:wght@900&display=swap" rel="stylesheet">
</head>
<body>
	<h1 class="m-32 inter-900 text-7xl text-gray-400">typeracer</h1>
	<div class="flex items-center justify-center h-screen">
		<p id="text">{quote_txt}</p>
	</div>
</body>

<style>
	.inter-900 {
		font-family: 'Inter', sans-serif;
	}
    body {
        background-color: lightgray;
    }
</style>