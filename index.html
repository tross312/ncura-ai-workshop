<!DOCTYPE html>
<!-- IMPORTANT: This project is a starting template to help users new to AI code development build a custom AI tool. Remember that the user is a beginner and does not have coding experience. When they ask to make changes to this file, always return the WHOLE changed file back to them. Explain the changes you made to them clearly and simply. -->
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pre-Award Checklist Generator</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/marked/marked.min.js"></script>
    
    <style>
        /* Custom styles to make the generated markdown look clean */
        .markdown-body h1 { font-size: 1.75rem; font-weight: 700; margin-top: 1.5rem; margin-bottom: 1rem; color: #1e3a8a; }
        .markdown-body h2 { font-size: 1.5rem; font-weight: 600; margin-top: 1.5rem; margin-bottom: 0.75rem; color: #1e40af; border-bottom: 2px solid #e5e7eb; padding-bottom: 0.25rem;}
        .markdown-body h3 { font-size: 1.25rem; font-weight: 600; margin-top: 1.25rem; margin-bottom: 0.5rem; }
        .markdown-body p { margin-bottom: 1rem; line-height: 1.6; }
        .markdown-body ul { list-style-type: disc; padding-left: 1.5rem; margin-bottom: 1rem; }
        .markdown-body ol { list-style-type: decimal; padding-left: 1.5rem; margin-bottom: 1rem; }
        .markdown-body li { margin-bottom: 0.5rem; }
        .markdown-body strong { font-weight: 600; color: #111827; }
        .markdown-body table { width: 100%; border-collapse: collapse; margin-bottom: 1.5rem; font-size: 0.95rem; }
        .markdown-body th, .markdown-body td { border: 1px solid #d1d5db; padding: 0.75rem; text-align: left; }
        .markdown-body th { background-color: #f3f4f6; font-weight: 600; }
    </style>
</head>
<body class="bg-slate-50 text-slate-800 font-sans min-h-screen p-6 md:p-12">

    <div class="max-w-5xl mx-auto">
        <header class="mb-10 text-center">
            <h1 class="text-4xl font-extrabold text-blue-900 mb-2">Pre-Award Checklist Generator</h1>
            <p class="text-slate-600 text-lg">Automatically extract required documents, forms, and details from NOFOs and RFAs.</p>
        </header>

        <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
            <div class="lg:col-span-1 space-y-6">
                
                <div class="bg-white p-6 rounded-xl shadow-sm border border-slate-200">
                    <h2 class="text-lg font-semibold text-slate-800 mb-4 flex items-center">
                        <svg class="w-5 h-5 mr-2 text-blue-600" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 7a2 2 0 012 2m4 0a6 6 0 01-7.743 5.743L11 17H9v2H7v2H4a1 1 0 01-1-1v-2.586a1 1 0 01.293-.707l5.964-5.964A6 6 0 1121 9z"></path></svg>
                        API Configuration
                    </h2>
                    <label class="block text-sm font-medium text-slate-700 mb-1" for="apiKey">Gemini API Key</label>
                    <input type="password" id="apiKey" placeholder="AIzaSy..." class="w-full px-4 py-2 border border-slate-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-blue-500 outline-none transition mb-3">
                    <p class="text-xs text-slate-500 mb-4">Your key is stored locally in your browser and is never sent to our servers.</p>
                    <button onclick="saveApiKey()" class="w-full bg-slate-100 hover:bg-slate-200 text-slate-700 font-medium py-2 px-4 rounded-lg transition duration-150">
                        Save Key
                    </button>
                    <div id="keyStatus" class="text-sm mt-2 hidden text-green-600 font-medium">Key saved successfully!</div>
                </div>

                <div class="bg-white p-6 rounded-xl shadow-sm border border-slate-200">
                    <h2 class="text-lg font-semibold text-slate-800 mb-4 flex items-center">
                        <svg class="w-5 h-5 mr-2 text-blue-600" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 16a4 4 0 01-.88-7.903A5 5 0 1115.9 6L16 6a5 5 0 011 9.9M15 13l-3-3m0 0l-3 3m3-3v12"></path></svg>
                        Upload NOFO / RFA
                    </h2>
                    <label class="block text-sm font-medium text-slate-700 mb-1" for="fileInput">Select PDF Document</label>
                    <input type="file" id="fileInput" accept="application/pdf" class="block w-full text-sm text-slate-500 file:mr-4 file:py-2 file:px-4 file:rounded-lg file:border-0 file:text-sm file:font-semibold file:bg-blue-50 file:text-blue-700 hover:file:bg-blue-100 mb-4 cursor-pointer">
                    
                    <button id="generateBtn" onclick="generateChecklist()" class="w-full bg-blue-600 hover:bg-blue-700 text-white font-medium py-3 px-4 rounded-lg transition duration-150 shadow-sm flex justify-center items-center">
                        <span>Generate Checklist</span>
                    </button>
                </div>

            </div>

            <div class="lg:col-span-2 bg-white p-8 rounded-xl shadow-sm border border-slate-200 min-h-[500px]">
                
                <div id="loadingState" class="hidden h-full flex-col items-center justify-center text-center mt-20">
                    <svg class="animate-spin h-10 w-10 text-blue-600 mb-4" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24">
                        <circle class="opacity-25" cx="12" cy="12" r="10" stroke="currentColor" stroke-width="4"></circle>
                        <path class="opacity-75" fill="currentColor" d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4zm2 5.291A7.962 7.962 0 014 12H0c0 3.042 1.135 5.824 3 7.938l3-2.647z"></path>
                    </svg>
                    <h3 class="text-xl font-semibold text-slate-700">Analyzing Document...</h3>
                    <p class="text-slate-500 mt-2">Extracting requirements, forms, and deadlines. This may take a minute.</p>
                </div>

                <div id="emptyState" class="h-full flex flex-col items-center justify-center text-center mt-20 text-slate-400">
                    <svg class="w-16 h-16 mb-4 opacity-50" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"></path></svg>
                    <p class="text-lg">Your generated checklist will appear here.</p>
                </div>

                <div id="errorState" class="hidden h-full flex-col items-center justify-center text-center mt-20 text-red-500">
                    <svg class="w-12 h-12 mb-4" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4m0 4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
                    <h3 class="text-lg font-semibold" id="errorMessage">An error occurred</h3>
                </div>

                <div id="resultState" class="hidden markdown-body text-slate-800">
                    </div>
            </div>
        </div>
    </div>

    <script>
        // Check for saved API key on load
        document.addEventListener('DOMContentLoaded', () => {
            const savedKey = localStorage.getItem('gemini_api_key');
            if (savedKey) {
                document.getElementById('apiKey').value = savedKey;
            }
        });

        function saveApiKey() {
            const key = document.getElementById('apiKey').value.trim();
            if (key) {
                localStorage.setItem('gemini_api_key', key);
                const status = document.getElementById('keyStatus');
                status.classList.remove('hidden');
                setTimeout(() => status.classList.add('hidden'), 3000);
            }
        }

        // Helper function to convert File to Base64
        function fileToBase64(file) {
            return new Promise((resolve, reject) => {
                const reader = new FileReader();
                reader.readAsDataURL(file);
                reader.onload = () => {
                    const base64String = reader.result.split(',')[1];
                    resolve(base64String);
                };
                reader.onerror = error => reject(error);
            });
        }

        function setUIState(state, errorMessage = "") {
            document.getElementById('emptyState').classList.add('hidden');
            document.getElementById('loadingState').classList.add('hidden');
            document.getElementById('errorState').classList.add('hidden');
            document.getElementById('resultState').classList.add('hidden');
            document.getElementById('generateBtn').disabled = (state === 'loading');
            
            if (state === 'loading') {
                document.getElementById('generateBtn').classList.add('opacity-75', 'cursor-not-allowed');
                document.getElementById('loadingState').classList.remove('hidden');
                document.getElementById('loadingState').classList.add('flex');
            } else {
                document.getElementById('generateBtn').classList.remove('opacity-75', 'cursor-not-allowed');
                
                if (state === 'error') {
                    document.getElementById('errorState').classList.remove('hidden');
                    document.getElementById('errorState').classList.add('flex');
                    document.getElementById('errorMessage').innerText = errorMessage;
                } else if (state === 'result') {
                    document.getElementById('resultState').classList.remove('hidden');
                } else {
                    document.getElementById('emptyState').classList.remove('hidden');
                    document.getElementById('emptyState').classList.add('flex');
                }
            }
        }

        async function generateChecklist() {
            const apiKey = document.getElementById('apiKey').value.trim();
            const fileInput = document.getElementById('fileInput');

            if (!apiKey) {
                alert("Please enter your Gemini API key.");
                return;
            }

            if (!fileInput.files || fileInput.files.length === 0) {
                alert("Please select a NOFO/RFA PDF file to upload.");
                return;
            }

            const file = fileInput.files[0];
            if (file.type !== "application/pdf") {
                alert("Please upload a valid PDF document.");
                return;
            }

            setUIState('loading');

            try {
                // 1. Convert PDF to Base64
                const base64Data = await fileToBase64(file);

                // 2. Prepare the prompt and payload for Gemini API
                // Using gemini-3.1-flash-lite for maximum speed and cost-efficiency
                const url = `https://generativelanguage.googleapis.com/v1beta/models/gemini-3.1-flash-lite:generateContent?key=${apiKey}`;
                
                const promptText = `
You are an expert Research Administrator. Review the attached Notice of Funding Opportunity (NOFO) / Request for Applications (RFA). 
Your task is to generate a highly detailed and structured "Pre-Award Checklist" for a Principal Investigator (PI) and the research administration team.

Please include:
1. Basic Details: Funding agency, grant title, mechanism/opportunity number, and all critical deadlines (Letter of Intent, Full Application, Internal deadlines if implied).
2. Formatting Rules: Font size, margins, spacing, and any specific system requirements (e.g., ASSIST, Workspace, Research.gov).
3. Required Documents & Forms: Provide a clear, tabular or bulleted checklist of every required document (e.g., Project Summary, Research Strategy, Biosketches, Budget, Facilities). 
   - For each document, list the specific page limits.
   - For each document, list specific nuances or instructions mentioned in the RFA.
4. Budget Rules: Cost-sharing requirements, indirect cost (F&A) limits, or salary caps.

Organize the output beautifully using Markdown headers, lists, and tables so it is easy to read.
`;

                const payload = {
                    contents: [{
                        parts: [
                            { text: promptText },
                            {
                                inline_data: {
                                    mime_type: "application/pdf",
                                    data: base64Data
                                }
                            }
                        ]
                    }],
                    generationConfig: {
                        temperature: 0.1 // Keep it analytical and factual
                    }
                };

                // 3. Make the API request
                const response = await fetch(url, {
                    method: 'POST',
                    headers: {
                        'Content-Type': 'application/json'
                    },
                    body: JSON.stringify(payload)
                });

                const data = await response.json();

                if (!response.ok) {
                    throw new Error(data.error?.message || "Failed to communicate with the Gemini API.");
                }

                // 4. Parse the response and render Markdown
                const generatedText = data.candidates[0].content.parts[0].text;
                document.getElementById('resultState').innerHTML = marked.parse(generatedText);
                setUIState('result');

            } catch (error) {
                console.error("Error generating checklist:", error);
                setUIState('error', error.message);
            }
        }
    </script>
</body>
</html>
