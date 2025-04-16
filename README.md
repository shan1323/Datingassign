# Datingassign
Penyelesaian masalah kreative
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Meet U - Connect with University Students</title>
<script src="https://cdn.tailwindcss.com/3.4.16"></script>
<script>tailwind.config={theme:{extend:{colors:{primary:'#FF69B4',secondary:'#8A2BE2'},borderRadius:{'none':'0px','sm':'4px',DEFAULT:'8px','md':'12px','lg':'16px','xl':'20px','2xl':'24px','3xl':'32px','full':'9999px','button':'8px'}}}}</script>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Pacifico&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<link href="https://cdn.jsdelivr.net/npm/remixicon@4.5.0/fonts/remixicon.css" rel="stylesheet">
<style>
:where([class^="ri-"])::before { content: "\f3c2"; }
@keyframes fade-in {
from { opacity: 0; transform: translateY(-20px); }
to { opacity: 1; transform: translateY(0); }
}
.animate-fade-in {
animation: fade-in 0.3s ease-out forwards;
}
body {
font-family: 'Poppins', sans-serif;
background-color: #fafafa;
}
input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
-webkit-appearance: none;
margin: 0;
}
input[type="number"] {
-moz-appearance: textfield;
}
.custom-checkbox {
position: relative;
display: inline-block;
width: 20px;
height: 20px;
margin-right: 8px;
}
.custom-checkbox input {
opacity: 0;
width: 0;
height: 0;
}
.checkmark {
position: absolute;
top: 0;
left: 0;
width: 20px;
height: 20px;
background-color: #fff;
border: 2px solid #e5e7eb;
border-radius: 4px;
transition: all 0.2s ease;
}
.custom-checkbox input:checked ~ .checkmark {
background-color: #FF69B4;
border-color: #FF69B4;
}
.checkmark:after {
content: "";
position: absolute;
display: none;
}
.custom-checkbox input:checked ~ .checkmark:after {
display: block;
}
.custom-checkbox .checkmark:after {
left: 6px;
top: 2px;
width: 6px;
height: 10px;
border: solid white;
border-width: 0 2px 2px 0;
transform: rotate(45deg);
}
.custom-switch {
position: relative;
display: inline-block;
width: 48px;
height: 24px;
}
.custom-switch input {
opacity: 0;
width: 0;
height: 0;
}
.switch-slider {
position: absolute;
cursor: pointer;
top: 0;
left: 0;
right: 0;
bottom: 0;
background-color: #e5e7eb;
transition: .4s;
border-radius: 24px;
}
.switch-slider:before {
position: absolute;
content: "";
height: 18px;
width: 18px;
left: 3px;
bottom: 3px;
background-color: white;
transition: .4s;
border-radius: 50%;
}
input:checked + .switch-slider {
background-color: #FF69B4;
}
input:checked + .switch-slider:before {
transform: translateX(24px);
}
.heart-bg {
background-image: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M30 10.8c2.7-4.2 7.9-5.6 12.2-3.2 4.3 2.4 5.9 7.5 3.2 11.7-2.3 3.6-13.7 12.2-15.4 13.7-1.7-1.5-13.1-10.1-15.4-13.7-2.7-4.2-1.1-9.3 3.2-11.7 4.3-2.4 9.5-1 12.2 3.2z' fill='%23FF69B4' fill-opacity='0.05'/%3E%3C/svg%3E");
}
.gradient-text {
background: linear-gradient(90deg, #FF69B4, #8A2BE2);
-webkit-background-clip: text;
background-clip: text;
color: transparent;
}
.custom-range {
-webkit-appearance: none;
width: 100%;
height: 6px;
border-radius: 5px;
background: #e5e7eb;
outline: none;
}
.custom-range::-webkit-slider-thumb {
-webkit-appearance: none;
appearance: none;
width: 20px;
height: 20px;
border-radius: 50%;
background: #FF69B4;
cursor: pointer;
}
.custom-range::-moz-range-thumb {
width: 20px;
height: 20px;
border-radius: 50%;
background: #FF69B4;
cursor: pointer;
border: none;
}
</style>
</head>
<body>
<!-- Sign Up/Login Page -->
<div id="login-page" class="min-h-screen flex flex-col">
<header class="w-full py-6 px-4 md:px-8 bg-white shadow-sm">
<div class="container mx-auto flex justify-center">
<h1 class="text-4xl font-['Pacifico'] gradient-text">Meet U</h1>
</div>
</header>
<main class="flex-grow flex items-center justify-center p-4">
<div class="w-full max-w-md bg-white rounded-xl shadow-lg p-8">
<div class="text-center mb-8">
<h2 class="text-2xl font-semibold text-gray-800">Welcome to Meet U</h2>
<p class="text-gray-600 mt-2">Connect with university students who match your vibe</p>
</div>
<div class="flex justify-center space-x-4 mb-6">
<button id="signup-tab" class="px-4 py-2 text-primary font-medium border-b-2 border-primary">Sign Up</button>
<button id="login-tab" class="px-4 py-2 text-gray-500 font-medium border-b-2 border-transparent">Login</button>
</div>
<!-- Sign Up Form -->
<form id="signup-form" class="space-y-4">
<div>
<label for="username" class="block text-sm font-medium text-gray-700 mb-1">Username</label>
<input type="text" id="username" name="username" required class="w-full px-4 py-2 border border-gray-300 rounded focus:outline-none focus:ring-2 focus:ring-primary/50">
</div>
<div>
<label for="mbti" class="block text-sm font-medium text-gray-700 mb-1">MBTI Personality Type</label>
<div class="relative">
<select id="mbti" name="mbti" required class="w-full px-4 py-2 border border-gray-300 rounded appearance-none focus:outline-none focus:ring-2 focus:ring-primary/50 pr-8">
<option value="" disabled selected>Select your MBTI</option>
<option value="INTJ">INTJ</option>
<option value="INTP">INTP</option>
<option value="ENTJ">ENTJ</option>
<option value="ENTP">ENTP</option>
<option value="INFJ">INFJ</option>
<option value="INFP">INFP</option>
<option value="ENFJ">ENFJ</option>
<option value="ENFP">ENFP</option>
<option value="ISTJ">ISTJ</option>
<option value="ISFJ">ISFJ</option>
<option value="ESTJ">ESTJ</option>
<option value="ESFJ">ESFJ</option>
<option value="ISTP">ISTP</option>
<option value="ISFP">ISFP</option>
<option value="ESTP">ESTP</option>
<option value="ESFP">ESFP</option>
</select>
<div class="absolute inset-y-0 right-0 flex items-center pr-3 pointer-events-none">
<i class="ri-arrow-down-s-line text-gray-400"></i>
</div>
</div>
</div>
<div>
<label for="age" class="block text-sm font-medium text-gray-700 mb-1">Age</label>
<input type="number" id="age" name="age" min="18" max="99" required class="w-full px-4 py-2 border border-gray-300 rounded focus:outline-none focus:ring-2 focus:ring-primary/50">
</div>
<div>
<label for="major" class="block text-sm font-medium text-gray-700 mb-1">Major/Department</label>
<input type="text" id="major" name="major" required class="w-full px-4 py-2 border border-gray-300 rounded focus:outline-none focus:ring-2 focus:ring-primary/50">
</div>
<div>
<label for="password" class="block text-sm font-medium text-gray-700 mb-1">Password</label>
<input type="password" id="password" name="password" required class="w-full px-4 py-2 border border-gray-300 rounded focus:outline-none focus:ring-2 focus:ring-primary/50">
</div>
<div>
<label for="photo" class="block text-sm font-medium text-gray-700 mb-1">Profile Photo (optional)</label>
<div class="flex items-center justify-center w-full">
<label for="photo-upload" class="flex flex-col items-center justify-center w-full h-32 border-2 border-gray-300 border-dashed rounded-lg cursor-pointer bg-gray-50 hover:bg-gray-100">
<div class="flex flex-col items-center justify-center pt-5 pb-6">
<i class="ri-upload-2-line ri-2x text-gray-400 mb-2"></i>
<p class="text-sm text-gray-500">Click to upload or drag and drop</p>
<p class="text-xs text-gray-500">PNG, JPG or JPEG (max. 2MB)</p>
</div>
<input id="photo-upload" type="file" class="hidden" accept="image/*">
</label>
</div>
</div>
<div>
<label for="bio" class="block text-sm font-medium text-gray-700 mb-1">Bio/Introduction (optional)</label>
<textarea id="bio" name="bio" rows="3" class="w-full px-4 py-2 border border-gray-300 rounded focus:outline-none focus:ring-2 focus:ring-primary/50" placeholder="Tell others about yourself..."></textarea>
</div>
<button type="submit" class="w-full py-3 px-4 bg-primary text-white font-medium rounded-button hover:bg-opacity-90 transition duration-200 whitespace-nowrap">Create Account</button>
</form>
<!-- Login Form (hidden by default) -->
<form id="login-form" class="space-y-4 hidden">
<div>
<label for="login-username" class="block text-sm font-medium text-gray-700 mb-1">Username</label>
<input type="text" id="login-username" name="login-username" required class="w-full px-4 py-2 border border-gray-300 rounded focus:outline-none focus:ring-2 focus:ring-primary/50">
</div>
<div>
<label for="login-password" class="block text-sm font-medium text-gray-700 mb-1">Password</label>
<input type="password" id="login-password" name="login-password" required class="w-full px-4 py-2 border border-gray-300 rounded focus:outline-none focus:ring-2 focus:ring-primary/50">
</div>
<div class="flex items-center justify-between">
<div class="flex items-center">
<label class="custom-checkbox">
<input type="checkbox" checked>
<span class="checkmark"></span>
</label>
<span class="text-sm text-gray-600">Remember me</span>
</div>
<a href="#" class="text-sm text-primary hover:underline">Forgot password?</a>
</div>
<button type="submit" class="w-full py-3 px-4 bg-primary text-white font-medium rounded-button hover:bg-opacity-90 transition duration-200 whitespace-nowrap">Login</button>
</form>
<div class="mt-6">
<div class="relative">
<div class="absolute inset-0 flex items-center">
<div class="w-full border-t border-gray-300"></div>
</div>
<div class="relative flex justify-center text-sm">
<span class="px-2 bg-white text-gray-500">Or continue with</span>
</div>
</div>
<div class="mt-6">
<button class="w-full py-3 px-4 border border-gray-300 rounded-button bg-white text-gray-700 font-medium flex items-center justify-center space-x-2 hover:bg-gray-50 transition duration-200 whitespace-nowrap">
<i class="ri-google-fill ri-lg text-red-500"></i>
<span>Sign in with Google</span>
</button>
</div>
</div>
<div class="mt-6 text-center">
<button id="skip-login" class="text-secondary hover:underline font-medium whitespace-nowrap">Skip Login</button>
</div>
</div>
</main>
</div>
<!-- Main Social Platform Interface -->
<div id="main-platform" class="hidden min-h-screen flex flex-col">
<header class="w-full py-4 px-4 md:px-8 bg-white shadow-sm">
<div class="container mx-auto flex justify-between items-center">
<h1 class="text-3xl font-['Pacifico'] gradient-text">Meet U</h1>
<div class="flex items-center space-x-4">
<button id="show-chat-list" class="w-10 h-10 flex items-center justify-center rounded-full bg-gray-100 hover:bg-gray-200">
<i class="ri-message-3-line ri-lg text-gray-700"></i>
</button>
<button id="show-profile" class="w-10 h-10 flex items-center justify-center rounded-full bg-gray-100 hover:bg-gray-200">
<i class="ri-user-line ri-lg text-gray-700"></i>
</button>
</div>
</div>
</header>
<main class="flex-grow flex flex-col items-center justify-center p-4 bg-gray-50">
<div class="w-full max-w-md">
<div class="mb-6 text-center">
<h2 class="text-2xl font-semibold text-gray-800">Find Your Match</h2>
<p class="text-gray-600 mt-1">Swipe right to match, left to pass</p>
</div>
<div class="relative h-[500px] bg-white rounded-xl shadow-lg overflow-hidden">
<div id="profile-card" class="h-full">
<div class="h-3/5 bg-gray-200">
<img id="profile-image" src="https://readdy.ai/api/search-image?query=portrait%20of%20a%20friendly%20smiling%20university%20student%20with%20natural%20lighting%2C%20professional%20photography%2C%20clean%20background%2C%20genuine%20expression%2C%20casual%20outfit%2C%20high%20quality%2C%20detailed%20facial%20features%2C%20soft%20shadows&width=400&height=500&seq=1&orientation=portrait" class="w-full h-full object-cover object-top">
</div>
<div class="h-2/5 p-6">
<div class="flex justify-between items-start">
<div>
<h3 id="profile-name" class="text-2xl font-semibold text-gray-800">Emma Wilson, 21</h3>
<p id="profile-details" class="text-gray-600 mt-1">Computer Science, ENFP</p>
</div>
<div class="flex items-center justify-center w-10 h-10 bg-primary/10 rounded-full">
<i class="ri-information-line ri-lg text-primary"></i>
</div>
</div>
<p id="profile-bio" class="text-gray-700 mt-3 line-clamp-3">Hi there! I'm a third-year CS student who loves coding, hiking, and playing the guitar. Looking to meet new friends who share similar interests or can teach me something new!</p>
</div>
<div class="absolute bottom-0 left-0 right-0 flex justify-center space-x-6 p-4">
<button id="swipe-left" class="w-14 h-14 flex items-center justify-center bg-white shadow-lg rounded-full hover:bg-gray-100 transition duration-200">
<i class="ri-close-line ri-2x text-gray-500"></i>
</button>
<button id="swipe-right" class="w-14 h-14 flex items-center justify-center bg-primary shadow-lg rounded-full hover:bg-opacity-90 transition duration-200">
<i class="ri-heart-3-line ri-2x text-white"></i>
</button>
</div>
</div>
</div>
<div class="mt-6 text-center">
<p class="text-gray-600"><span id="profiles-remaining">10</span> profiles remaining</p>
</div>
</div>
</main>
</div>
<!-- Chat Interface -->
<div id="chat-interface" class="hidden min-h-screen flex">
<!-- Chat List Sidebar -->
<div id="chat-sidebar" class="w-80 bg-white border-r border-gray-200 flex flex-col">
<div class="p-4 border-b border-gray-200">
<div class="flex items-center justify-between">
<h2 class="text-xl font-semibold text-gray-800">Messages</h2>
<button id="back-to-main" class="w-8 h-8 flex items-center justify-center rounded-full hover:bg-gray-100">
<i class="ri-arrow-left-line ri-lg text-gray-700"></i>
</button>
</div>
<div class="mt-3 relative">
<input type="text" placeholder="Search conversations..." class="w-full pl-10 pr-4 py-2 bg-gray-100 border-none rounded-full focus:outline-none focus:ring-2 focus:ring-primary/50 text-sm">
<div class="absolute left-3 top-1/2 transform -translate-y-1/2 w-5 h-5 flex items-center justify-center">
<i class="ri-search-line text-gray-500"></i>
</div>
</div>
</div>
<div class="flex-grow overflow-y-auto">
<div class="chat-contact active p-3 hover:bg-gray-100 cursor-pointer border-l-4 border-primary" data-name="Daniel Lee" data-image="https://readdy.ai/api/search-image?query=portrait%20of%20a%20young%20university%20student%20with%20glasses%2C%20natural%20lighting%2C%20professional%20photography%2C%20clean%20background%2C%20genuine%20smile%2C%20casual%20outfit%2C%20high%20quality%2C%20detailed%20facial%20features&width=50&height=50&seq=2&orientation=squarish" onclick="openChat(this)">
<div class="flex items-center space-x-3">
<div class="relative">
<img src="https://readdy.ai/api/search-image?query=portrait%20of%20a%20young%20university%20student%20with%20glasses%2C%20natural%20lighting%2C%20professional%20photography%2C%20clean%20background%2C%20genuine%20smile%2C%20casual%20outfit%2C%20high%20quality%2C%20detailed%20facial%20features&width=50&height=50&seq=2&orientation=squarish" class="w-12 h-12 rounded-full object-cover object-top">
<div class="absolute bottom-0 right-0 w-3 h-3 bg-green-500 rounded-full border-2 border-white"></div>
</div>
<div class="flex-grow">
<div class="flex justify-between items-center">
<h3 class="font-medium text-gray-800">Daniel Lee</h3>
<span class="text-xs text-gray-500">2m</span>
</div>
<p class="text-sm text-gray-600 truncate">Hey! What are you studying?</p>
</div>
</div>
</div>
<div class="chat-contact p-3 hover:bg-gray-100 cursor-pointer" data-name="Sophia Chen" data-image="https://readdy.ai/api/search-image?query=portrait%20of%20a%20female%20university%20student%20with%20long%20hair%2C%20natural%20lighting%2C%20professional%20photography%2C%20clean%20background%2C%20genuine%20smile%2C%20casual%20outfit%2C%20high%20quality%2C%20detailed%20facial%20features&width=50&height=50&seq=3&orientation=squarish" onclick="openChat(this)">
<div class="flex items-center space-x-3">
<div class="relative">
<img src="https://readdy.ai/api/search-image?query=portrait%20of%20a%20female%20university%20student%20with%20long%20hair%2C%20natural%20lighting%2C%20professional%20photography%2C%20clean%20background%2C%20genuine%20smile%2C%20casual%20outfit%2C%20high%20quality%2C%20detailed%20facial%20features&width=50&height=50&seq=3&orientation=squarish" class="w-12 h-12 rounded-full object-cover object-top">
<div class="absolute bottom-0 right-0 w-3 h-3 bg-gray-300 rounded-full border-2 border-white"></div>
</div>
<div class="flex-grow">
<div class="flex justify-between items-center">
<h3 class="font-medium text-gray-800">Sophia Chen</h3>
<span class="text-xs text-gray-500">1h</span>
</div>
<p class="text-sm text-gray-600 truncate">I'm in the library right now!</p>
</div>
</div>
</div>
<div class="chat-contact p-3 hover:bg-gray-100 cursor-pointer" data-name="James Rodriguez" data-image="https://readdy.ai/api/search-image?query=portrait%20of%20a%20male%20university%20student%20with%20short%20hair%2C%20natural%20lighting%2C%20professional%20photography%2C%20clean%20background%2C%20genuine%20smile%2C%20casual%20outfit%2C%20high%20quality%2C%20detailed%20facial%20features&width=50&height=50&seq=4&orientation=squarish" onclick="openChat(this)">
<div class="flex items-center space-x-3">
<div class="relative">
<img src="https://readdy.ai/api/search-image?query=portrait%20of%20a%20male%20university%20student%20with%20short%20hair%2C%20natural%20lighting%2C%20professional%20photography%2C%20clean%20background%2C%20genuine%20smile%2C%20casual%20outfit%2C%20high%20quality%2C%20detailed%20facial%20features&width=50&height=50&seq=4&orientation=squarish" class="w-12 h-12 rounded-full object-cover object-top">
<div class="absolute bottom-0 right-0 w-3 h-3 bg-gray-300 rounded-full border-2 border-white"></div>
</div>
<div class="flex-grow">
<div class="flex justify-between items-center">
<h3 class="font-medium text-gray-800">James Rodriguez</h3>
<span class="text-xs text-gray-500">5h</span>
</div>
<p class="text-sm text-gray-600 truncate">Are you going to the event tomorrow?</p>
</div>
</div>
</div>
<div id="ukm-monkey-chat" class="chat-contact p-3 hover:bg-gray-100 cursor-pointer" data-name="UKM Monkey" data-is-ai="true" onclick="openChat(this)">
<div class="flex items-center space-x-3">
<div class="relative">
<div class="w-12 h-12 rounded-full bg-secondary flex items-center justify-center text-white font-bold">
<i class="ri-robot-line ri-lg"></i>
</div>
</div>
<div class="flex-grow">
<div class="flex justify-between items-center">
<h3 class="font-medium text-gray-800">UKM Monkey</h3>
<span class="text-xs text-gray-500">AI</span>
</div>
<p class="text-sm text-gray-600 truncate">I can help with conversation starters!</p>
</div>
</div>
</div>
</div>
</div>
<!-- Chat Main Area -->
<div id="chat-main" class="flex-grow flex flex-col heart-bg">
<div id="chat-header" class="p-4 bg-white shadow-sm flex items-center justify-between">
<div class="flex items-center space-x-3">
<div id="chat-avatar" class="relative w-10 h-10">
<img src="https://readdy.ai/api/search-image?query=portrait%20of%20a%20young%20university%20student%20with%20glasses%2C%20natural%20lighting%2C%20professional%20photography%2C%20clean%20background%2C%20genuine%20smile%2C%20casual%20outfit%2C%20high%20quality%2C%20detailed%20facial%20features&width=50&height=50&seq=2&orientation=squarish" class="w-10 h-10 rounded-full object-cover object-top">
<div class="absolute bottom-0 right-0 w-2.5 h-2.5 bg-green-500 rounded-full border-2 border-white"></div>
</div>
<div>
<h3 id="chat-name" class="font-medium text-gray-800">Daniel Lee</h3>
<p id="chat-status" class="text-xs text-gray-500">Online</p>
</div>
</div>
<div class="relative">
<button id="chat-menu-button" class="w-8 h-8 flex items-center justify-center rounded-full hover:bg-gray-100">
<i class="ri-more-2-fill ri-lg text-gray-700"></i>
</button>
<div id="chat-menu" class="hidden absolute right-0 top-full mt-2 w-48 bg-white rounded-lg shadow-lg z-10">
<ul class="py-2">
<li class="px-4 py-2 hover:bg-gray-100 cursor-pointer flex items-center">
<i class="ri-user-line mr-2 text-gray-600"></i>
<span>View Profile</span>
</li>
<li id="share-location-btn" class="px-4 py-2 hover:bg-gray-100 cursor-pointer flex items-center">
<i class="ri-share-line mr-2 text-gray-600"></i>
<span>Share Location</span>
</li>
<li class="px-4 py-2 hover:bg-gray-100 cursor-pointer flex items-center" onclick="showClearChatConfirmation()">
<i class="ri-delete-bin-line mr-2 text-gray-600"></i>
<span>Clear Chat</span>
</li>
<li class="px-4 py-2 hover:bg-gray-100 cursor-pointer flex items-center">
<i class="ri-flag-line mr-2 text-gray-600"></i>
<span>Report User</span>
</li>
</ul>
</div>
</div>
</div>
<div id="chat-messages" class="flex-grow p-4 overflow-y-auto">
<div class="space-y-4">
<div class="flex justify-center">
<div class="bg-white px-4 py-2 rounded-full text-xs text-gray-500">
April 16, 2025
</div>
</div>
<div class="flex justify-start">
<div class="bg-white rounded-lg rounded-tl-none px-4 py-3 max-w-[75%] shadow-sm">
<p class="text-gray-800">Hi! Nice to match with you 😊</p>
<p class="text-xs text-gray-500 text-right mt-1">9:45 AM</p>
</div>
</div>
<div class="flex justify-end">
<div class="bg-primary/10 rounded-lg rounded-tr-none px-4 py-3 max-w-[75%] shadow-sm">
<p class="text-gray-800">Hey Daniel! Nice to match with you too!</p>
<p class="text-xs text-gray-500 text-right mt-1">9:47 AM</p>
</div>
</div>
<div class="flex justify-start">
<div class="bg-white rounded-lg rounded-tl-none px-4 py-3 max-w-[75%] shadow-sm">
<p class="text-gray-800">I saw we're both at the same university! Hey! What are you studying?</p>
<p class="text-xs text-gray-500 text-right mt-1">10:15 AM</p>
</div>
</div>
</div>
</div>
<div class="p-4 bg-white border-t border-gray-200">
<div class="flex items-center space-x-2">
<div class="flex-grow relative">
<input type="text" id="message-input" placeholder="Type a message..." class="w-full pl-4 pr-10 py-3 bg-gray-100 border-none rounded-full focus:outline-none focus:ring-2 focus:ring-primary/50">
<button class="absolute right-3 top-1/2 transform -translate-y-1/2 w-8 h-8 flex items-center justify-center text-gray-500 hover:text-gray-700">
<i class="ri-emotion-line ri-lg"></i>
</button>
</div>
<button id="send-message" class="w-10 h-10 flex items-center justify-center bg-primary rounded-full text-white hover:bg-opacity-90 transition-colors" onclick="sendMessage()">
<i class="ri-send-plane-fill ri-lg"></i>
</button>
</div>
<div class="mt-3 flex flex-wrap gap-2">
<button class="quick-reply px-4 py-2 bg-gray-100 rounded-full text-sm text-gray-700 hover:bg-gray-200 whitespace-nowrap">
I'm studying Psychology!
</button>
<button class="quick-reply px-4 py-2 bg-gray-100 rounded-full text-sm text-gray-700 hover:bg-gray-200 whitespace-nowrap">
Computer Science, what about you?
</button>
<button class="quick-reply px-4 py-2 bg-gray-100 rounded-full text-sm text-gray-700 hover:bg-gray-200 whitespace-nowrap">
I'm in the Business program
</button>
<button class="quick-reply px-4 py-2 bg-gray-100 rounded-full text-sm text-gray-700 hover:bg-gray-200 whitespace-nowrap">
Engineering student here!
</button>
</div>
</div>
</div>
</div>
<!-- Profile View Modal -->
<!-- Location Sharing Modal -->
<div id="location-modal" class="hidden fixed inset-0 bg-black/50 flex items-center justify-center z-50">
<div class="bg-white rounded-xl w-full max-w-md p-6 animate-fade-in">
<div class="text-center mb-6">
<div class="w-16 h-16 mx-auto mb-4 flex items-center justify-center bg-primary/10 rounded-full">
<i class="ri-map-pin-line ri-2x text-primary"></i>
</div>
<h3 class="text-xl font-semibold text-gray-800 mb-2">Share Location</h3>
<p class="text-gray-600">Share your current location with your match</p>
</div>
<div class="mb-6">
<div class="relative w-full h-48 rounded-lg overflow-hidden mb-4">
<img src="https://public.readdy.ai/gen_page/map_placeholder_1280x720.png" class="w-full h-full object-cover">
<div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2">
<div class="w-8 h-8 bg-primary/20 rounded-full flex items-center justify-center">
<div class="w-4 h-4 bg-primary rounded-full"></div>
</div>
</div>
</div>
<div class="space-y-4">
<div>
<label for="location-message" class="block text-sm font-medium text-gray-700 mb-1">Add a message</label>
<input type="text" id="location-message" class="w-full px-4 py-2 border border-gray-300 rounded focus:outline-none focus:ring-2 focus:ring-primary/50" placeholder="I'm at the library">
</div>
<div class="flex items-center space-x-2">
<button class="quick-location-msg px-3 py-1 bg-gray-100 rounded-full text-sm text-gray-700 hover:bg-gray-200 whitespace-nowrap">I'm at the library</button>
<button class="quick-location-msg px-3 py-1 bg-gray-100 rounded-full text-sm text-gray-700 hover:bg-gray-200 whitespace-nowrap">Meet me here</button>
<button class="quick-location-msg px-3 py-1 bg-gray-100 rounded-full text-sm text-gray-700 hover:bg-gray-200 whitespace-nowrap">I'm nearby</button>
</div>
</div>
</div>
<div class="flex space-x-3">
<button id="cancel-location" class="flex-1 py-2 px-4 border border-gray-300 text-gray-700 font-medium rounded-button hover:bg-gray-50 transition duration-200 whitespace-nowrap">Cancel</button>
<button id="share-location" class="flex-1 py-2 px-4 bg-primary text-white font-medium rounded-button hover:bg-opacity-90 transition duration-200 whitespace-nowrap">Share Location</button>
</div>
</div>
</div>
<!-- Clear Chat Confirmation Modal -->
<div id="clear-chat-modal" class="hidden fixed inset-0 bg-black/50 flex items-center justify-center z-50">
<div class="bg-white rounded-xl w-full max-w-sm p-6 animate-fade-in">
<div class="text-center mb-6">
<div class="w-16 h-16 mx-auto mb-4 flex items-center justify-center bg-red-100 rounded-full">
<i class="ri-delete-bin-line ri-2x text-red-500"></i>
</div>
<h3 class="text-xl font-semibold text-gray-800 mb-2">Clear Chat History?</h3>
<p class="text-gray-600">This action cannot be undone. All messages in this conversation will be permanently deleted.</p>
</div>
<div class="flex space-x-3">
<button onclick="hideClearChatConfirmation()" class="flex-1 py-2 px-4 border border-gray-300 text-gray-700 font-medium rounded-button hover:bg-gray-50 transition duration-200 whitespace-nowrap">Cancel</button>
<button onclick="clearChat()" class="flex-1 py-2 px-4 bg-red-500 text-white font-medium rounded-button hover:bg-red-600 transition duration-200 whitespace-nowrap">Clear</button>
</div>
</div>
</div>
<div id="profile-modal" class="hidden fixed inset-0 bg-black/50 flex items-center justify-center z-50">
<div class="bg-white rounded-xl w-full max-w-md max-h-[90vh] overflow-y-auto">
<div class="relative h-64">
<img src="https://readdy.ai/api/search-image?query=portrait%20of%20a%20young%20university%20student%20with%20glasses%2C%20natural%20lighting%2C%20professional%20photography%2C%20clean%20background%2C%20genuine%20smile%2C%20casual%20outfit%2C%20high%20quality%2C%20detailed%20facial%20features&width=500&height=300&seq=5&orientation=landscape" class="w-full h-full object-cover object-top">
<button class="absolute top-4 right-4 w-8 h-8 flex items-center justify-center bg-black/50 rounded-full text-white hover:bg-black/70">
<i class="ri-close-line ri-lg"></i>
</button>
</div>
<div class="p-6">
<h2 class="text-2xl font-semibold text-gray-800">Daniel Lee, 22</h2>
<p class="text-gray-600 mt-1">Computer Science, INTP</p>
<div class="mt-6 space-y-4">
<div>
<h3 class="text-sm font-medium text-gray-500 uppercase">About</h3>
<p class="mt-2 text-gray-700">
Third-year CS student passionate about AI and machine learning. I enjoy coding, playing basketball, and exploring new coffee shops around campus. Looking to connect with like-minded students!
</p>
</div>
<div>
<h3 class="text-sm font-medium text-gray-500 uppercase">Interests</h3>
<div class="mt-2 flex flex-wrap gap-2">
<span class="px-3 py-1 bg-gray-100 rounded-full text-sm text-gray-700">Programming</span>
<span class="px-3 py-1 bg-gray-100 rounded-full text-sm text-gray-700">Basketball</span>
<span class="px-3 py-1 bg-gray-100 rounded-full text-sm text-gray-700">Coffee</span>
<span class="px-3 py-1 bg-gray-100 rounded-full text-sm text-gray-700">Hiking</span>
<span class="px-3 py-1 bg-gray-100 rounded-full text-sm text-gray-700">Reading</span>
</div>
</div>
<div>
<h3 class="text-sm font-medium text-gray-500 uppercase">Location</h3>
<p class="mt-2 text-gray-700 flex items-center">
<i class="ri-map-pin-line mr-2 text-gray-500"></i>
<span>University Library (shared location)</span>
</p>
</div>
</div>
<div class="mt-8 flex space-x-3">
<button class="flex-1 py-3 px-4 bg-primary text-white font-medium rounded-button hover:bg-opacity-90 transition duration-200 whitespace-nowrap">
Message
</button>
<button class="py-3 px-4 border border-gray-300 text-gray-700 font-medium rounded-button hover:bg-gray-50 transition duration-200 whitespace-nowrap">
Report
</button>
</div>
</div>
</div>
</div>
<script>
function sendMessage() {
const messageInput = document.getElementById('message-input');
const chatMessages = document.getElementById('chat-messages');
const chatName = document.getElementById('chat-name').textContent;
const message = messageInput.value.trim();
if (!message) return;
// Create and append user message
const userMessageHTML = `
<div class="flex justify-end">
<div class="bg-primary/10 rounded-lg rounded-tr-none px-4 py-3 max-w-[75%] shadow-sm">
<p class="text-gray-800">${message}</p>
<p class="text-xs text-gray-500 text-right mt-1">${new Date().toLocaleTimeString('en-US', { hour: 'numeric', minute: '2-digit', hour12: true })}</p>
</div>
</div>
`;
chatMessages.insertAdjacentHTML('beforeend', userMessageHTML);
messageInput.value = '';
chatMessages.scrollTop = chatMessages.scrollHeight;
// Only respond if it's UKM Monkey (AI)
if (chatName === 'UKM Monkey') {
setTimeout(() => {
const aiResponses = {
'study': [
"Based on your interests, I'd recommend joining the Computer Science Study Group that meets every Tuesday at the library. They focus on collaborative learning and practical projects.",
"Have you checked out the university's peer tutoring program? They offer free sessions for most major subjects, and it's a great way to meet other students too!",
"The Academic Success Center is hosting a workshop on 'Effective Study Techniques' next week. Would you like me to share more details?",
"I notice you're interested in group study. There's a great quiet study space in the new Student Center building, perfect for group work!"
],
'social': [
"The Student Union is organizing a 'Meet & Greet' event this Friday. It's a perfect opportunity to meet other students who share your interests!",
"Have you considered joining any university clubs? The Photography Club and Debate Society are particularly active this semester.",
"There's an upcoming International Food Festival where you can meet students from different cultures and try amazing food. Want more information?",
"The campus coffee shop hosts weekly social mixers. It's a casual way to meet new people while enjoying great coffee!"
],
'career': [
"The Career Center is offering resume reviews and mock interviews this week. It's a great way to prepare for internship applications!",
"There's an upcoming Tech Career Fair with companies like Google and Microsoft. Would you like tips on how to prepare?",
"I can help you connect with alumni in your field of interest. They often provide valuable career advice and networking opportunities.",
"Have you considered applying for the university's research assistant positions? They're great for gaining practical experience."
],
'general': [
"I noticed you're new here! The university offers a peer mentoring program that might interest you. Would you like to learn more?",
"There's a great wellness center on campus that offers free meditation and yoga sessions. It's perfect for managing study stress!",
"Did you know about the university's free shuttle service? It runs every 15 minutes and covers all major campus locations.",
"The library just launched a new digital resource center. I can guide you through the available tools and resources!"
]
};
let category = 'general';
const messageLC = message.toLowerCase();
if (messageLC.includes('study') || messageLC.includes('class') || messageLC.includes('course')) category = 'study';
if (messageLC.includes('meet') || messageLC.includes('friend') || messageLC.includes('social')) category = 'social';
if (messageLC.includes('job') || messageLC.includes('career') || messageLC.includes('internship')) category = 'career';
const responses = aiResponses[category];
const randomResponse = responses[Math.floor(Math.random() * responses.length)];
const aiMessageHTML = `
<div class="flex justify-start">
<div class="bg-white rounded-lg rounded-tl-none px-4 py-3 max-w-[75%] shadow-sm">
<p class="text-gray-800">${randomResponse}</p>
<p class="text-xs text-gray-500 text-right mt-1">${new Date().toLocaleTimeString('en-US', { hour: 'numeric', minute: '2-digit', hour12: true })}</p>
</div>
</div>
`;
chatMessages.insertAdjacentHTML('beforeend', aiMessageHTML);
chatMessages.scrollTop = chatMessages.scrollHeight;
}, 1000);
}
}
function openMatchedChat(element) {
const chatContact = element.closest('.chat-contact');
const chatName = chatContact.querySelector('.font-medium').textContent;
const chatImage = chatContact.querySelector('img').src;
// Show chat interface
document.getElementById('main-platform').classList.add('hidden');
document.getElementById('chat-interface').classList.remove('hidden');
// Update chat header and open chat
openChat({
getAttribute: (attr) => {
if (attr === 'data-name') return chatName;
if (attr === 'data-image') return chatImage;
if (attr === 'data-is-ai') return 'false';
}
}, true);
// Focus message input
setTimeout(() => {
document.getElementById('message-input').focus();
}, 100);
}
function openChat(element, isNewMatch = false) {
const chatName = element.getAttribute('data-name');
const chatImage = element.getAttribute('data-image');
const isAi = element.getAttribute('data-is-ai') === 'true';
// Update chat header
document.getElementById('chat-name').textContent = chatName;
if (isAi) {
document.getElementById('chat-avatar').innerHTML = `
<div class="w-10 h-10 rounded-full bg-secondary flex items-center justify-center text-white font-bold">
<i class="ri-robot-line ri-lg"></i>
</div>
`;
} else {
document.getElementById('chat-avatar').innerHTML = `
<img src="${chatImage}" class="w-10 h-10 rounded-full object-cover object-top">
<div class="absolute bottom-0 right-0 w-2.5 h-2.5 bg-green-500 rounded-full border-2 border-white"></div>
`;
}
// Clear previous messages
const matchMessage = `
<div class="space-y-4">
<div class="flex justify-center">
<div class="bg-white px-4 py-2 rounded-full text-xs text-gray-500">
${new Date().toLocaleDateString('en-US', { month: 'long', day: 'numeric', year: 'numeric' })}
</div>
</div>
<div class="flex justify-center">
<div class="bg-white px-6 py-3 rounded-xl shadow-sm text-center animate-fade-in">
<div class="w-16 h-16 mx-auto mb-3 flex items-center justify-center bg-primary/10 rounded-full">
<i class="ri-heart-3-fill ri-2x text-primary"></i>
</div>
<h3 class="font-medium text-gray-800 mb-1">It's a Match!</h3>
<p class="text-sm text-gray-600">You and ${chatName} liked each other!</p>
<p class="text-sm text-gray-600 mt-1">Start a conversation now!</p>
</div>
</div>
</div>
`;
document.getElementById('chat-messages').innerHTML = matchMessage;
// Update chat status
document.getElementById('chat-status').textContent = 'Online';
// Remove active class from all contacts and add to clicked one
document.querySelectorAll('.chat-contact').forEach(contact => {
contact.classList.remove('active', 'border-l-4', 'border-primary');
});
element.classList.add('active', 'border-l-4', 'border-primary');
}
document.addEventListener('DOMContentLoaded', function() {
// Add enter key support for sending messages
const messageInput = document.getElementById('message-input');
messageInput.addEventListener('keypress', function(e) {
if (e.key === 'Enter') {
sendMessage();
}
});
// Quick reply buttons functionality
const quickReplyButtons = document.querySelectorAll('.quick-reply');
quickReplyButtons.forEach(button => {
button.addEventListener('click', function() {
const messageInput = document.getElementById('message-input');
messageInput.value = this.textContent.trim();
sendMessage();
});
});
// Tab switching for login/signup
const signupTab = document.getElementById('signup-tab');
const loginTab = document.getElementById('login-tab');
const signupForm = document.getElementById('signup-form');
const loginForm = document.getElementById('login-form');
signupTab.addEventListener('click', function() {
signupTab.classList.add('text-primary', 'border-primary');
signupTab.classList.remove('text-gray-500', 'border-transparent');
loginTab.classList.remove('text-primary', 'border-primary');
loginTab.classList.add('text-gray-500', 'border-transparent');
signupForm.classList.remove('hidden');
loginForm.classList.add('hidden');
});
loginTab.addEventListener('click', function() {
loginTab.classList.add('text-primary', 'border-primary');
loginTab.classList.remove('text-gray-500', 'border-transparent');
signupTab.classList.remove('text-primary', 'border-primary');
signupTab.classList.add('text-gray-500', 'border-transparent');
loginForm.classList.remove('hidden');
signupForm.classList.add('hidden');
});
});
function showClearChatConfirmation() {
document.getElementById('clear-chat-modal').classList.remove('hidden');
document.getElementById('chat-menu').classList.add('hidden');
}
function hideClearChatConfirmation() {
document.getElementById('clear-chat-modal').classList.add('hidden');
}
function clearChat() {
const chatMessages = document.getElementById('chat-messages');
const chatName = document.getElementById('chat-name').textContent;
// Keep only the date header and match message
chatMessages.innerHTML = `
<div class="space-y-4">
<div class="flex justify-center">
<div class="bg-white px-4 py-2 rounded-full text-xs text-gray-500">
${new Date().toLocaleDateString('en-US', { month: 'long', day: 'numeric', year: 'numeric' })}
</div>
</div>
</div>
`;
hideClearChatConfirmation();
}
document.addEventListener('DOMContentLoaded', function() {
// Location sharing functionality
const shareLocationBtn = document.getElementById('share-location-btn');
const locationModal = document.getElementById('location-modal');
const cancelLocation = document.getElementById('cancel-location');
const shareLocation = document.getElementById('share-location');
const locationMessage = document.getElementById('location-message');
const quickLocationMsgs = document.querySelectorAll('.quick-location-msg');
shareLocationBtn.addEventListener('click', function() {
  locationModal.classList.remove('hidden');
  document.getElementById('chat-menu').classList.add('hidden');
});
cancelLocation.addEventListener('click', function() {
  locationModal.classList.add('hidden');
  locationMessage.value = '';
});
quickLocationMsgs.forEach(btn => {
  btn.addEventListener('click', function() {
    locationMessage.value = this.textContent;
  });
});
shareLocation.addEventListener('click', function() {
  if ("geolocation" in navigator) {
    navigator.geolocation.getCurrentPosition(function(position) {
      const lat = position.coords.latitude;
      const lng = position.coords.longitude;
      const message = locationMessage.value.trim() || "Shared location";
      
      const locationHTML = `
        <div class="flex justify-end">
          <div class="bg-primary/10 rounded-lg rounded-tr-none px-4 py-3 max-w-[75%] shadow-sm">
            <div class="relative w-full h-32 rounded-lg overflow-hidden mb-2">
              <img src="https://public.readdy.ai/gen_page/map_placeholder_1280x720.png" class="w-full h-full object-cover">
              <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2">
                <div class="w-6 h-6 bg-primary/20 rounded-full flex items-center justify-center">
                  <div class="w-3 h-3 bg-primary rounded-full"></div>
                </div>
              </div>
            </div>
            <p class="text-gray-800 flex items-center">
              <i class="ri-map-pin-line mr-2"></i>
              <span>${message}</span>
            </p>
            <p class="text-xs text-gray-500 text-right mt-1">${new Date().toLocaleTimeString('en-US', { hour: 'numeric', minute: '2-digit', hour12: true })}</p>
          </div>
        </div>
      `;
      
      const chatMessages = document.getElementById('chat-messages');
      chatMessages.insertAdjacentHTML('beforeend', locationHTML);
      chatMessages.scrollTop = chatMessages.scrollHeight;
      
      locationModal.classList.add('hidden');
      locationMessage.value = '';
    });
  }
});
// Navigation between pages
const loginPage = document.getElementById('login-page');
const mainPlatform = document.getElementById('main-platform');
const chatInterface = document.getElementById('chat-interface');
const profileModal = document.getElementById('profile-modal');
// Form submissions
const signupForm = document.getElementById('signup-form');
const loginForm = document.getElementById('login-form');
const skipLogin = document.getElementById('skip-login');
signupForm.addEventListener('submit', function(e) {
e.preventDefault();
loginPage.classList.add('hidden');
mainPlatform.classList.remove('hidden');
});
loginForm.addEventListener('submit', function(e) {
e.preventDefault();
loginPage.classList.add('hidden');
mainPlatform.classList.remove('hidden');
});
skipLogin.addEventListener('click', function() {
loginPage.classList.add('hidden');
mainPlatform.classList.remove('hidden');
});
// Chat navigation
const showChatList = document.getElementById('show-chat-list');
const backToMain = document.getElementById('back-to-main');
showChatList.addEventListener('click', function() {
mainPlatform.classList.add('hidden');
chatInterface.classList.remove('hidden');
});
backToMain.addEventListener('click', function() {
chatInterface.classList.add('hidden');
mainPlatform.classList.remove('hidden');
});
// Profile modal
const showProfile = document.getElementById('show-profile');
const closeProfileModal = profileModal.querySelector('button');
showProfile.addEventListener('click', function() {
profileModal.classList.remove('hidden');
});
closeProfileModal.addEventListener('click', function() {
profileModal.classList.add('hidden');
});
// Chat menu
const chatMenuButton = document.getElementById('chat-menu-button');
const chatMenu = document.getElementById('chat-menu');
chatMenuButton.addEventListener('click', function() {
chatMenu.classList.toggle('hidden');
});
// Close menu when clicking outside
document.addEventListener('click', function(e) {
if (!chatMenuButton.contains(e.target) && !chatMenu.contains(e.target)) {
chatMenu.classList.add('hidden');
}
});
});
document.addEventListener('DOMContentLoaded', function() {
// Swipe functionality
const swipeLeft = document.getElementById('swipe-left');
const swipeRight = document.getElementById('swipe-right');
const profilesRemaining = document.getElementById('profiles-remaining');
const profileCard = document.getElementById('profile-card');
const profileImage = document.getElementById('profile-image');
const profileName = document.getElementById('profile-name');
const profileDetails = document.getElementById('profile-details');
const profileBio = document.getElementById('profile-bio');
// Sample profiles data
const profiles = [
{
name: 'Emma Wilson',
age: 21,
major: 'Computer Science',
mbti: 'ENFP',
bio: 'Hi there! I\'m a third-year CS student who loves coding, hiking, and playing the guitar. Looking to meet new friends who share similar interests or can teach me something new!',
image: 'https://readdy.ai/api/search-image?query=portrait%20of%20a%20friendly%20smiling%20university%20student%20with%20natural%20lighting%2C%20professional%20photography%2C%20clean%20background%2C%20genuine%20expression%2C%20casual%20outfit%2C%20high%20quality%2C%20detailed%20facial%20features%2C%20soft%20shadows&width=400&height=500&seq=1&orientation=portrait'
},
{
name: 'Michael Johnson',
age: 22,
major: 'Business Administration',
mbti: 'ENTJ',
bio: 'Business student with a passion for entrepreneurship. I enjoy playing tennis, watching documentaries, and trying new restaurants. Looking for friends to explore the city with!',
image: 'https://readdy.ai/api/search-image?query=portrait%20of%20a%20confident%20male%20university%20student%20with%20natural%20lighting%2C%20professional%20photography%2C%20clean%20background%2C%20genuine%20smile%2C%20business%20casual%20outfit%2C%20high%20quality%2C%20detailed%20facial%20features&width=400&height=500&seq=6&orientation=portrait'
},
{
name: 'Olivia Martinez',
age: 20,
major: 'Psychology',
mbti: 'INFJ',
bio: 'Psychology major interested in human behavior and mental health. I love reading, painting, and having deep conversations. Looking for authentic connections with like-minded people.',
image: 'https://readdy.ai/api/search-image?query=portrait%20of%20a%20thoughtful%20female%20university%20student%20with%20natural%20lighting%2C%20professional%20photography%2C%20clean%20background%2C%20gentle%20smile%2C%20casual%20outfit%2C%20high%20quality%2C%20detailed%20facial%20features&width=400&height=500&seq=7&orientation=portrait'
},
{
name: 'William Chen',
age: 23,
major: 'Engineering',
mbti: 'ISTJ',
bio: 'Final year engineering student. I enjoy solving problems, building things, and playing basketball. Looking for study buddies or friends to hang out with on weekends.',
image: 'https://readdy.ai/api/search-image?query=portrait%20of%20a%20serious%20male%20university%20student%20with%20glasses%2C%20natural%20lighting%2C%20professional%20photography%2C%20clean%20background%2C%20slight%20smile%2C%20casual%20outfit%2C%20high%20quality%2C%20detailed%20facial%20features&width=400&height=500&seq=8&orientation=portrait'
},
{
name: 'Sophia Kim',
age: 19,
major: 'Graphic Design',
mbti: 'ESFP',
bio: 'Creative soul studying graphic design. I love art exhibitions, photography, and trying new coffee shops. Looking to connect with other creative minds!',
image: 'https://readdy.ai/api/search-image?query=portrait%20of%20a%20creative%20female%20university%20student%20with%20artistic%20style%2C%20natural%20lighting%2C%20professional%20photography%2C%20clean%20background%2C%20bright%20smile%2C%20stylish%20outfit%2C%20high%20quality%2C%20detailed%20facial%20features&width=400&height=500&seq=9&orientation=portrait'
},
{
name: 'Ethan Patel',
age: 21,
major: 'Medicine',
mbti: 'INTJ',
bio: 'Pre-med student with a passion for healthcare. I enjoy running, reading scientific journals, and playing chess. Looking for friends who can challenge me intellectually.',
image: 'https://readdy.ai/api/search-image?query=portrait%20of%20a%20focused%20male%20university%20student%20in%20casual%20medical%20attire%2C%20natural%20lighting%2C%20professional%20photography%2C%20clean%20background%2C%20confident%20expression%2C%20high%20quality%2C%20detailed%20facial%20features&width=400&height=500&seq=10&orientation=portrait'
},
{
name: 'Isabella Rodriguez',
age: 20,
major: 'International Relations',
mbti: 'ENFJ',
bio: 'Studying international relations and passionate about global issues. I love traveling, learning languages, and attending cultural events. Looking to expand my social circle!',
image: 'https://readdy.ai/api/search-image?query=portrait%20of%20a%20diverse%20female%20university%20student%20with%20natural%20lighting%2C%20professional%20photography%2C%20clean%20background%2C%20warm%20smile%2C%20smart%20casual%20outfit%2C%20high%20quality%2C%20detailed%20facial%20features&width=400&height=500&seq=11&orientation=portrait'
},
{
name: 'Noah Thompson',
age: 22,
major: 'Film Studies',
mbti: 'INFP',
bio: 'Film student and aspiring director. I enjoy watching movies, writing screenplays, and photography. Looking for creative friends to collaborate with on projects.',
image: 'https://readdy.ai/api/search-image?query=portrait%20of%20an%20artistic%20male%20university%20student%20with%20camera%2C%20natural%20lighting%2C%20professional%20photography%2C%20clean%20background%2C%20thoughtful%20expression%2C%20casual%20outfit%2C%20high%20quality%2C%20detailed%20facial%20features&width=400&height=500&seq=12&orientation=portrait'
},
{
name: 'Ava Williams',
age: 21,
major: 'Environmental Science',
mbti: 'ISFJ',
bio: 'Environmental science major passionate about sustainability. I enjoy hiking, gardening, and volunteering. Looking to connect with people who care about our planet.',
image: 'https://readdy.ai/api/search-image?query=portrait%20of%20a%20nature-loving%20female%20university%20student%20outdoors%2C%20natural%20lighting%2C%20professional%20photography%2C%20natural%20background%2C%20friendly%20smile%2C%20outdoor%20outfit%2C%20high%20quality%2C%20detailed%20facial%20features&width=400&height=500&seq=13&orientation=portrait'
}
];
let currentProfileIndex = 1;
let remainingProfiles = profiles.length;
profilesRemaining.textContent = remainingProfiles;
function updateProfile() {
if (currentProfileIndex >= profiles.length) {
// No more profiles
profileCard.innerHTML = `
<div class="h-full flex flex-col items-center justify-center p-6 text-center">
<div class="w-20 h-20 flex items-center justify-center bg-primary/10 rounded-full mb-4">
<i class="ri-search-line ri-2x text-primary"></i>
</div>
<h3 class="text-xl font-semibold text-gray-800 mb-2">No More Profiles</h3>
<p class="text-gray-600">You've gone through all available profiles. Check back later for more!</p>
</div>
`;
return;
}
const profile = profiles[currentProfileIndex];
profileImage.src = profile.image;
profileName.textContent = `${profile.name}, ${profile.age}`;
profileDetails.textContent = `${profile.major}, ${profile.mbti}`;
profileBio.textContent = profile.bio;
}
swipeLeft.addEventListener('click', function() {
// Animation for swipe left
profileCard.style.transition = 'transform 0.3s ease';
profileCard.style.transform = 'translateX(-100px) rotate(-5deg)';
profileCard.style.opacity = '0';
setTimeout(() => {
currentProfileIndex++;
remainingProfiles--;
profilesRemaining.textContent = remainingProfiles;
profileCard.style.transition = 'none';
profileCard.style.transform = 'translateX(100px) rotate(5deg)';
updateProfile();
setTimeout(() => {
profileCard.style.transition = 'transform 0.3s ease, opacity 0.3s ease';
profileCard.style.transform = 'translateX(0) rotate(0)';
profileCard.style.opacity = '1';
}, 50);
}, 300);
});
swipeRight.addEventListener('click', function() {
// Animation for swipe right
profileCard.style.transition = 'transform 0.3s ease';
profileCard.style.transform = 'translateX(100px) rotate(5deg)';
profileCard.style.opacity = '0';
// Add matched profile to chat list
const matchedProfile = profiles[currentProfileIndex];
const chatSidebar = document.querySelector('#chat-sidebar .flex-grow');
const newChatContact = `
<div class="chat-contact p-3 hover:bg-gray-100 cursor-pointer">
<div class="flex items-center space-x-3">
<div class="relative">
<img src="${matchedProfile.image}" class="w-12 h-12 rounded-full object-cover object-top">
<div class="absolute bottom-0 right-0 w-3 h-3 bg-green-500 rounded-full border-2 border-white"></div>
</div>
<div class="flex-grow">
<div class="flex justify-between items-center">
<h3 class="font-medium text-gray-800">${matchedProfile.name}</h3>
<span class="text-xs text-gray-500">now</span>
</div>
<p class="text-sm text-gray-600 truncate cursor-pointer" onclick="openMatchedChat(this)">You matched! Say hello!</p>
</div>
</div>
</div>
`;
chatSidebar.insertAdjacentHTML('afterbegin', newChatContact);
// Show match notification
const matchNotification = document.createElement('div');
matchNotification.className = 'fixed top-4 right-4 bg-white rounded-lg shadow-lg p-4 z-50 flex items-center space-x-3 animate-fade-in';
matchNotification.innerHTML = `
<img src="${matchedProfile.image}" class="w-12 h-12 rounded-full object-cover object-top">
<div>
<h3 class="font-medium text-gray-800">It's a Match!</h3>
<p class="text-sm text-gray-600">You and ${matchedProfile.name} liked each other</p>
</div>
`;
document.body.appendChild(matchNotification);
setTimeout(() => matchNotification.remove(), 3000);
setTimeout(() => {
currentProfileIndex++;
remainingProfiles--;
profilesRemaining.textContent = remainingProfiles;
profileCard.style.transition = 'none';
profileCard.style.transform = 'translateX(-100px) rotate(-5deg)';
updateProfile();
setTimeout(() => {
profileCard.style.transition = 'transform 0.3s ease, opacity 0.3s ease';
profileCard.style.transform = 'translateX(0) rotate(0)';
profileCard.style.opacity = '1';
}, 50);
}, 300);
});
});
C:\users\Dekstop\演示\demo>git init
</script>
</body>
</html>
