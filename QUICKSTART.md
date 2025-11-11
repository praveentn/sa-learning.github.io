# 🚀 QUICK START GUIDE

## 5-Minute Setup

### Step 1: Install Dependencies
```bash
pip install openai python-dotenv jupyter
```

### Step 2: Configure Azure OpenAI
Create a `.env` file with your credentials (see `env.example`):
```
AZURE_ENDPOINT=https://your-endpoint.cognitiveservices.azure.com/
AZURE_API_KEY=your-api-key-here
AZURE_DEPLOYMENT=gpt-5-chat
```

### Step 3: Generate Demo Content
Open Jupyter Notebook:
```bash
jupyter notebook learning_system_notebook.ipynb
```

Run the first code cell to import and configure, then run:
```python
demo_path = quick_start_demo(AZURE_ENDPOINT, AZURE_API_KEY, AZURE_DEPLOYMENT)
```

This generates a small curriculum (2 fields × 2 topics) in ~2-3 minutes.

### Step 4: Start Learning
1. Open `sa_learning_tracker.html` in your browser
2. Drag & drop the generated JSON file (from `learning_content/` folder)
3. Start checking off items as you learn!

---

## 📁 What You Got

- **solution_architect_learning_system.py** - Core Python module
- **learning_system_notebook.ipynb** - Ready-to-use Jupyter notebook
- **sa_learning_tracker.html** - Beautiful learning interface
- **README.md** - Complete documentation
- **requirements.txt** - Python dependencies
- **env.example** - Configuration template

---

## 🎯 Common Commands

### Generate Full Curriculum
```python
llm, cm = initialize_system(AZURE_ENDPOINT, API_KEY, DEPLOYMENT)
filepath = generate_full_curriculum(llm, cm, max_topics_per_field=3)
```

### Add New Field
```python
cm.load_json("learning_content/sa_learning_v1_*.json")
add_new_field_with_content(llm, cm, "Serverless Architecture", True)
```

### Add Topics
```python
add_topics_to_field(llm, cm, "Cloud Architecture", num_topics=3, create_new_version=True)
```

---

## 💡 Pro Tips

1. **Start Small**: Use `quick_start_demo()` first
2. **Test Once**: Generate 2-3 topics to verify quality
3. **Version Everything**: Always set `create_new_version=True`
4. **Mobile-Friendly**: HTML tracker works great on phones
5. **Offline**: Once loaded, tracker needs no internet

---

## ⚡ Quick Troubleshooting

**Issue**: API errors
- **Fix**: Check your `.env` file has correct credentials

**Issue**: JSON not loading in tracker
- **Fix**: Make sure the JSON file is from the `learning_content/` folder

**Issue**: Progress not saving
- **Fix**: Enable browser LocalStorage / try different browser

---

## 📊 What Gets Generated Per Topic

Each topic includes **20+ aspects** with 5+ items each:
- 💡 Facts & Concepts
- 💻 Code Examples  
- 🎯 Use Cases
- 🌟 Real Examples
- 👥 Client Stories
- ⚠️ Issues & Solutions
- 🧠 Key Points
- 👶 Simple Explanations
- 🔄 Analogies
- ❓ MCQs
- ✅ Best Practices
- 🛠️ Tools
- 🎤 Interview Questions
- 🏋️ Exercises
- And more!

That's **100+ learning items per topic**! 🎓

---

## 🎬 Next Steps

1. ✅ Run quick demo
2. ✅ Review quality in HTML tracker
3. ✅ Generate full curriculum (2-4 hours)
4. ✅ Master one field at a time
5. ✅ Track your progress daily

**Happy Learning!** 🚀
