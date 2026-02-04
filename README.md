# Mayraimport openai

# 1. Setup Client
client = openai.OpenAI(api_key="YOUR_API_KEY_HERE")

def ask_assistant(prompt):
    response = client.chat.completions.create(
        model="gpt-4o", # Or "gpt-3.5-turbo"
        messages=[
            {"role": "system", "content": "You are a helpful coding assistant."},
            {"role": "user", "content": prompt}
        ]
    )
    return response.choices[0].message.content

# 2. Run a query
user_input = "Write a Python function to sort a list of strings by length."
print(ask_assistant(user_input))
def simple_ai_assistant(prompt):
    # यह सबसे सरल AI असिस्टेंट है
    # यहाँ हम प्रॉम्प्ट के आधार पर एक निश्चित उत्तर देंगे
    
    prompt = prompt.lower()
    
    if "hello" in prompt or "hi" in prompt:
        return "नमस्ते! मैं आपकी कैसे सहायता कर सकता हूँ?"
    elif "task" in prompt or "काम" in prompt:
        return "आपके कार्य क्या हैं? कृपया विस्तार से बताएँ ताकि मैं मदद कर सकूँ।"
    elif "engineer" in prompt or "इंजीनियर" in prompt:
        return "एक इंजीनियर के तौर पर, मैं कोडिंग, डेटा विश्लेषण या प्रोजेक्ट मैनेजमेंट में मदद कर सकता हूँ।"
    else:
        return "मैं अभी सीख रहा हूँ। क्या आप कुछ और पूछना चाहेंगे?"

# उदाहरण के लिए:
user_input = input("आप AI असिस्टेंट से क्या पूछना चाहते हैं? ")
print(simple_ai_assistant(user_input))
def integrated_ai_assistant(prompt):
    prompt = prompt.lower()
    
    # 1. बुनियादी AI और प्रोजेक्ट मैनेजमेंट तर्क
    if "hello" in prompt or "hi" in prompt or "नमस्ते" in prompt:
        return "नमस्ते! मैं आपका एकीकृत AI सहायक हूँ। मैं कोडिंग, डेटा विश्लेषण और प्रोजेक्ट प्रबंधन में मदद कर सकता हूँ।"
    elif "task" in prompt or "काम" in prompt or "project" in prompt or "प्रोजेक्ट" in prompt:
        return "प्रोजेक्ट मैनेजमेंट मॉड्यूल: मैं आपके कार्यों को व्यवस्थित करने, समय सीमा ट्रैक करने और संसाधनों का प्रबंधन करने में मदद कर सकता हूँ।"
    
    # 2. डेटा प्रोसेसिंग मॉड्यूल
    elif "data" in prompt or "विश्लेषण" in prompt or "analyze" in prompt:
        return "डेटा विश्लेषण मॉड्यूल: कृपया डेटा प्रदान करें। मैं पैटर्न की पहचान करने और रिपोर्ट तैयार करने में सहायता कर सकता हूँ।"
    
    # 3. कोडिंग मॉड्यूल
    elif "code" in prompt or "कोडिंग" in prompt or "function" in prompt or "def" in prompt:
        return "कोडिंग मॉड्यूल: मैं Python, Java और अन्य भाषाओं में कोड स्निपेट्स जनरेट कर सकता हूँ और डीबगिंग में सहायता कर सकता हूँ।"
    
    else:
        return "मैं एक बहुमुखी AI सहायक हूँ। कृपया स्पष्ट करें कि आप किस क्षेत्र में सहायता चाहते हैं - कोडिंग, डेटा या प्रोजेक्ट प्रबंधन?"

# मुख्य प्रोग्राम
user_input = input("एकीकृत AI असिस्टेंट से बात करें: ")
print(integrated_ai_assistant(user_input))
def best_integrated_ai_assistant(prompt):
    prompt = prompt.lower()
    
    # मुख्य पहचान और मार्गन (Routing)
    if "data" in prompt or "विश्लेषण" in prompt or "analyze" in prompt:
        return "समेकित डेटा मॉड्यूल: उन्नत विश्लेषण और विज़ुअलाइज़ेशन के लिए कृपया विस्तृत डेटा इनपुट करें।"
    elif "code" in prompt or "कोडिंग" in prompt or "प्रोग्राम" in prompt:
        return "समेकित कोडिंग मॉड्यूल: मैं जटिल एल्गोरिदम और बहु-भाषा कोड स्निपेट्स तैयार करने में मदद कर सकता हूँ।"
    elif "project" in prompt or "प्रोजेक्ट" in prompt or "कार्य" in prompt:
        return "समेकित प्रोजेक्ट मॉड्यूल: AI-आधारित योजना, संसाधन आवंटन और गतिशील कार्य ट्रैकिंग के लिए तैयार हूँ।"
    elif "hello" in prompt or "hi" in prompt or "नमस्ते" in prompt:
        return "नमस्ते! मैं आपका सबसे उन्नत एकीकृत सहायक हूँ। मैं आपके इंजीनियरिंग कार्यों को सरल बनाने के लिए विशेषज्ञ मॉड्यूल से लैस हूँ।"
    else:
        return "मैं आपके इंजीनियरिंग workflow के लिए डिज़ाइन किया गया हूँ। कृपया बताएँ कि आपको कोडिंग, डेटा विश्लेषण या प्रोजेक्ट प्रबंधन में से किसमें सहायता चाहिए?"

# मुख्य प्रोग्राम
user_input = input("उन्नत एकीकृत AI असिस्टेंट से बात करें: ")
print(best_integrated_ai_assistant(user_input))
