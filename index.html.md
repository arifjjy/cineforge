# index.html  
  
<!DOCTYPE html>  
<html lang="en">  
<head>  
<meta charset="UTF-8">  
<meta name="viewport" content="width=device-width, initial-scale=1.0">  
<title>CineForge | Horror and Executive Recommendation Registry</title>  
<link href="https://fonts.googleapis.com/css2?family=Oswald:wght@500;700&family=Roboto:wght@400;500;700&display=swap" rel="stylesheet">  
<style>  
:root {  
    --primary-color: #C62828;  
    --secondary-color: #E6E6E6;  
    --bg-dark-primary: #0A0A0A;  
    --bg-dark-card: #181818;  
    --font-display: 'Oswald', sans-serif;  
    --font-body: 'Roboto', sans-serif;  
    --transition-speed: 0.3s;  
}  
* {margin:0;padding:0;box-sizing:border-box;}  
body {font-family: var(--font-body);line-height:1.6;color:var(--secondary-color);background-color:var(--bg-dark-primary);scroll-behavior:smooth;}  
.container {max-width:1200px;margin:0 auto;padding:0 15px;}  
.hero-section {  
    background: url('https://images.unsplash.com/photo-1517457224233-1ec8a31e13a9?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1600&q=80') no-repeat center center;  
    background-attachment: fixed;background-size: cover;padding:150px 0 120px;text-align:center;position:relative;  
}  
.hero-section::before {  
    content:'';position:absolute;top:0;left:0;right:0;bottom:0;background:rgba(0,0,0,0.92);  
}  
.hero-section .container {position:relative;z-index:10;}  
.hero-section h1 {font-family:var(--font-display);font-size:4rem;font-weight:700;margin-bottom:15px;color:var(--primary-color);text-transform:uppercase;letter-spacing:4px;text-shadow:0 0 10px rgba(198,40,40,0.7);}  
.hero-section .tagline {font-family:var(--font-body);font-size:1.6rem;font-weight:500;color:#C0C0C0;max-width:800px;margin:0 auto;margin-bottom:25px;}  
.hero-section .tagline::after {content:'';display:block;width:150px;height:2px;background-color:var(--primary-color);margin:20px auto 0;}  
.content-section {padding:70px 0;text-align:center;border-bottom:1px solid #282828;}  
.content-section.dark {background-color:var(--bg-dark-card);}  
.content-section h2 {font-family:var(--font-display);font-size:2.8rem;font-weight:700;margin-bottom:40px;color:var(--secondary-color);position:relative;text-transform:uppercase;}  
.content-section h2::after {content:'';display:block;width:80px;height:3px;background-color:var(--primary-color);margin:15px auto 0;}  
.horror-directive {padding:40px;background-color:#120A0A;border:3px dashed var(--primary-color);border-radius:10px;margin-top:30px;box-shadow:0 0 20px rgba(198,40,40,0.3);}  
.horror-directive h3 {font-family:var(--font-display);font-size:2rem;color:var(--primary-color);margin-bottom:12px;text-transform:uppercase;}  
.horror-directive p {color:#E6E6E6;font-size:1rem;max-width:700px;margin:0 auto;}  
.features-grid {display:flex;flex-wrap:wrap;justify-content:space-between;gap:20px;margin-top:40px;}  
.feature-item {flex:1 1 250px;padding:25px;background-color:var(--bg-dark-primary);border-radius:8px;box-shadow:0 5px 15px rgba(0,0,0,0.6),0 0 0 1px rgba(255,255,255,0.05);border-left:4px solid var(--primary-color);transition:transform var(--transition-speed) ease,box-shadow var(--transition-speed) ease;}  
.feature-item:hover {transform:translateY(-5px);box-shadow:0 10px 25px rgba(198,40,40,0.5),0 0 0 1px rgba(255,255,255,0.1);}  
.feature-item .icon {font-size:2.5rem;color:var(--primary-color);margin-bottom:12px;display:block;}  
.feature-item h3 {font-family:var(--font-body);font-size:1.3rem;font-weight:700;margin-bottom:8px;color:var(--secondary-color);}  
.feature-item p {color:#A0A0A0;font-size:0.9rem;}  
.submission-container {max-width:650px;margin:0 auto;}  
.suggestion-form {background:var(--bg-dark-card);padding:35px;border-radius:12px;box-shadow:0 15px 40px rgba(0,0,0,0.8);border:1px solid rgba(255,255,255,0.1);transition:opacity 0.5s ease;}  
.form-group {margin-bottom:20px;position:relative;}  
.form-group label {font-family:var(--font-body);font-weight:700;color:var(--primary-color);text-transform:uppercase;display:block;margin-bottom:6px;font-size:0.95rem;}  
.form-group input[type="text"],.form-group input[type="email"] {width:100%;padding:12px;border:none;border-radius:4px;background-color:#262626;color:var(--secondary-color);font-size:1rem;box-shadow:inset 0 1px 3px rgba(0,0,0,0.4);transition:border-color var(--transition-speed);}  
.form-group input[type="text"]:focus,.form-group input[type="email"]:focus {outline:none;border:1px solid var(--primary-color);box-shadow:0 0 8px rgba(198,40,40,0.8);}  
.validation-error {color:var(--primary-color);font-size:0.8rem;margin-top:5px;text-align:left;display:none;}  
.submit-button {display:block;width:100%;padding:14px;border:none;border-radius:4px;background-color:var(--primary-color);color:white;font-size:1.1rem;font-weight:700;cursor:pointer;text-transform:uppercase;letter-spacing:1px;box-shadow:0 4px 10px rgba(0,0,0,0.5);transition:background-color var(--transition-speed),transform 0.1s;position:relative;overflow:hidden;}  
.submit-button:hover:not(:disabled) {background-color:#A01D1D;transform:translateY(-1px);box-shadow:0 6px 15px rgba(198,40,40,0.4);}  
.submit-button:disabled {background-color:#444;cursor:not-allowed;color:transparent;}  
.loader {position:absolute;top:50%;left:50%;transform:translate(-50%,-50%);width:20px;height:20px;border:3px solid rgba(255,255,255,0.3);border-top-color:#fff;border-radius:50%;display:none;animation:spin 1s linear infinite;}  
@keyframes spin {to{transform:translate(-50%,-50%) rotate(360deg);}}  
.submit-button:disabled .loader {display:block;}  
.success-message {display:none;padding:40px;border-radius:12px;background-color:#120A0A;border:2px solid var(--primary-color);box-shadow:0 15px 40px rgba(198,40,40,0.3);text-align:center;}  
.success-message h3 {font-family:var(--font-display);color:#fff;font-size:2rem;margin-bottom:10px;}  
.success-message p {color:#C0C0C0;font-size:1rem;}  
.footer-section {padding:30px 0;background-color:var(--bg-dark-primary);border-top:1px solid #1c1c1c;}  
.footer-section p {color:#555;font-weight:400;font-size:0.85rem;}  
.animate-hidden {opacity:0;transform:translateY(20px);transition:opacity 0.7s cubic-bezier(0.25,0.46,0.45,0.94),transform 0.7s cubic-bezier(0.25,0.46,0.45,0.94);}  
.animate-show {opacity:1;transform:translateY(0);}  
@media(max-width:992px){.features-grid{flex-direction:column;gap:20px;}}  
@media(max-width:768px){.hero-section h1{font-size:3rem;letter-spacing:2px;}.hero-section .tagline{font-size:1.2rem;}.content-section h2{font-size:2rem;}.suggestion-form{padding:25px;}}  
</style>  
</head>  
<body>  
  
<header class="hero-section">  
<div class="container">  
<h1>EXECUTIVE RECOMMENDATION 🩸</h1>  
<p class="tagline">Submit a cinematic masterpiece and enter to win a Premium Gift Card.</p>  
</div>  
</header>  
  
<main>  
<section id="horror" class="content-section animate-hidden">  
<div class="container">  
<h2>THE HORROR DIRECTIVE</h2>  
<div class="horror-directive">  
<h3>Seeking the Darkest Visions</h3>  
<p>I hold a special spot for horror movies. When submitting, know that titles from the horror or thriller genres will receive priority consideration. Suggest the most visceral, psychological, or impactful film to secure your spot.</p>  
</div>  
</div>  
</section>  
  
<section id="about" class="content-section dark animate-hidden">  
<div class="container">  
<h2>OUR MANDATE</h2>  
<div class="features-grid">  
<div class="feature-item"><span class="icon">🏆</span><h3>CURATED SELECTION</h3><p>We are building an executive list of films—only critically acclaimed and impactful titles are considered.</p></div>  
<div class="feature-item"><span class="icon">🎁</span><h3>PREMIUM REWARD</h3><p>If your movie is selected as the next watch, you'll win an Amazon Gift Card sent directly to your email!</p></div>  
<div class="feature-item"><span class="icon">🔒</span><h3>DATA SECURITY</h3><p>Your submission and email are logged immediately into our secure, audited registry, prioritizing your privacy.</p></div>  
</div>  
</div>  
</section>  
  
<section id="portal" class="content-section animate-hidden">  
<div class="container">  
<h2 class="section-title">SUBMIT YOUR ENTRY</h2>  
<p class="section-description" style="color:#A0A0A0;">Enter your suggestion and email below for a chance to win. Remember, **Horror Submissions** receive priority!</p>  
<div class="submission-container">  
<form id="suggestionForm" action="https://sheetdb.io/api/v1/h3lohmek89yxr" method="POST" class="suggestion-form" novalidate>  
<div class="form-group">  
<label for="movieName">FILM TITLE (HORROR/THRILLER ENCOURAGED):</label>  
<input type="text" id="movieName" name="movieName" placeholder="e.g., The Babadook, Seven, or Citizen Kane" required>  
<div id="movieError" class="validation-error"></div>  
</div>  
<div class="form-group">  
<label for="emailAddress">YOUR EMAIL (REQUIRED FOR REWARD):</label>  
<input type="email" id="emailAddress" name="emailAddress" placeholder="email@example.com" required>  
<div id="emailError" class="validation-error"></div>  
</div>  
<button type="submit" class="submit-button" id="submitButton">SUBMIT TO REGISTRY<div class="loader"></div></button>  
</form>  
<div id="successMessage" class="success-message">  
<h3>SUBMISSION RECEIVED.</h3>  
<p>Your cinematic recommendation has been securely logged to the executive registry. We appreciate your submission and will contact the winning entrant via the provided email address.</p>  
</div>  
</div>  
</div>  
</section>  
</main>  
  
<footer id="footer" class="footer-section">  
<div class="container"><p>&copy; 2024 arifjjy &bull; EXECUTIVE REGISTRY. All rights reserved. Designed for excellence and the pursuit of cinematic fear.</p></div>  
</footer>  
  
<script>  
const sections=document.querySelectorAll('.content-section');  
const observer=new IntersectionObserver((entries,observer)=>{  
entries.forEach(entry=>{  
if(entry.isIntersecting){entry.target.classList.add('animate-show');observer.unobserve(entry.target);}  
});  
},{root:null,rootMargin:'0px',threshold:0.1});  
sections.forEach(section=>observer.observe(section));  
  
document.getElementById('suggestionForm').addEventListener('submit',function(e){  
e.preventDefault();  
const form=e.target;  
const movieInput=document.getElementById('movieName');  
const emailInput=document.getElementById('emailAddress');  
const movieError=document.getElementById('movieError');  
const emailError=document.getElementById('emailError');  
const submitButton=document.getElementById('submitButton');  
const successMessage=document.getElementById('successMessage');  
movieError.style.display='none';  
emailError.style.display='none';  
let isValid=true;  
if(movieInput.value.trim()===''){movieError.textContent='A film title is required for entry.';movieError.style.display='block';isValid=false;}  
if(emailInput.value.trim()===''){emailError.textContent='Your email is required for reward contact.';emailError.style.display='block';isValid=false;}  
else if(!/@.+\./.test(emailInput.value)){emailError.textContent='Please enter a valid email address.';emailError.style.display='block';isValid=false;}  
if(!isValid){return;}  
submitButton.disabled=true;  
fetch(form.action,{method:'POST',body:new FormData(form)})  
.then(response=>{if(response.ok){return response.json();}else{throw new Error('Submission Failed. Server communication error.');}})  
.then(data=>{form.style.opacity='0';movieInput.value='';emailInput.value='';setTimeout(()=>{form.style.display='none';successMessage.style.display='block';},500);})  
.catch(error=>{console.error('Error:',error);alert('CRITICAL ERROR: Submission failed. Check your SheetDB connection or network.');submitButton.textContent='SUBMIT TO REGISTRY';submitButton.disabled=false;});  
});  
</script>  
  
</body>  
</html>  
