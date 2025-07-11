# YouTube Comment Sentiment Analysis

A comprehensive sentiment analysis project that extracts YouTube comments and analyzes their sentiment using multiple machine learning algorithms.

## 🚀 Features

- **Comment Extraction**: Fetch comments from YouTube videos using YouTube Data API v3
- **Text Preprocessing**: Clean and preprocess comments for analysis
- **Multi-language Support**: Detect and filter English comments
- **Emoji Processing**: Convert emojis to text for better analysis
- **Multiple ML Models**: Compare performance across different algorithms
- **Visualization**: Display model accuracy comparison

## 📋 Table of Contents

- [Installation](#installation)
- [Setup](#setup)
- [Usage](#usage)
- [Models Used](#models-used)
- [Results](#results)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## 🛠️ Installation

### Prerequisites

- Python 3.7 or higher
- Google API Key for YouTube Data API v3

### Required Libraries

```bash
pip install googletrans
pip install emoji
pip install langdetect
pip install pandas
pip install numpy
pip install scikit-learn
pip install tensorflow
pip install matplotlib
pip install nltk
pip install textblob
pip install google-api-python-client
```

## ⚙️ Setup

### 1. Get YouTube API Key

1. Go to [Google Cloud Console](https://console.cloud.google.com/)
2. Create a new project or select an existing one
3. Enable YouTube Data API v3
4. Create credentials (API Key)
5. Replace `DEVELOPER_KEY` in the code with your API key

### 2. Configure the Project

```python
# Replace with your YouTube API key
DEVELOPER_KEY = "YOUR_API_KEY_HERE"

# Set the video ID you want to analyze
video_id = "YOUR_VIDEO_ID_HERE"
```

## 🎯 Usage

### Basic Usage

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/youtube-sentiment-analysis.git
cd youtube-sentiment-analysis
```

2. **Run the Jupyter notebook**
```bash
jupyter notebook Youtube_comment_Sentiment_analysiis.ipynb
```

3. **Follow the notebook cells sequentially**

### Key Steps

1. **Comment Extraction**: Fetch comments from specified YouTube video
2. **Data Preprocessing**: Clean and filter comments
3. **Sentiment Analysis**: Apply TextBlob for initial sentiment labeling
4. **Model Training**: Train multiple ML models
5. **Evaluation**: Compare model performances

## 🤖 Models Used

### 1. Decision Tree Classifier
- **Accuracy**: ~78.8%
- Fast training and prediction
- Good interpretability

### 2. Random Forest Classifier
- **Accuracy**: ~80.4%
- Ensemble method with better generalization
- Reduced overfitting compared to single decision tree

### 3. Recurrent Neural Network (RNN/LSTM)
- **Accuracy**: ~88.8%
- Deep learning approach
- Better at capturing sequential patterns in text

### 4. Gradient Boosting Classifier
- **Accuracy**: ~80.3%
- Ensemble method with sequential learning
- Good performance on structured data

## 📊 Results

The project analyzes sentiment in three categories:
- **Positive**: Comments with positive sentiment
- **Neutral**: Comments with neutral sentiment  
- **Negative**: Comments with negative sentiment

### Model Performance Comparison

| Model | Accuracy |
|-------|----------|
| Decision Tree | 78.8% |
| Random Forest | 80.4% |
| Gradient Boosting | 80.3% |
| RNN (LSTM) | 88.8% |

**Best Performing Model**: RNN (LSTM) with 88.8% accuracy

## 📁 Project Structure

```
youtube-sentiment-analysis/
│
├── Youtube_comment_Sentiment_analysiis.ipynb    # Main notebook
├── youtube_comments.csv                         # Extracted comments data
├── README.md                                   # Project documentation
└── requirements.txt                            # Dependencies
```

## 🔧 Data Processing Pipeline

### 1. Comment Extraction
- Use YouTube Data API v3 to fetch comments
- Handle pagination for large comment sets
- Maximum 1M comments per video

### 2. Text Preprocessing
- Remove punctuation and special characters
- Convert emojis to text descriptions
- Remove URLs and links
- Filter non-English comments
- Convert to lowercase

### 3. Feature Engineering
- TF-IDF vectorization for traditional ML models
- Text tokenization and padding for neural networks
- Label encoding for target variables

### 4. Model Training
- Train-test split (80-20)
- Cross-validation for model selection
- Hyperparameter tuning

## 📈 Visualization

The project includes accuracy comparison visualization using matplotlib:
- Line plot showing model performances
- Clear comparison of different approaches

## 🚨 Important Notes

### API Limitations
- YouTube API has quota limits
- Maximum 100 comments per API call
- Be mindful of daily quotas

### Data Privacy
- Only public comments are extracted
- No personal information is stored
- Comments are processed anonymously

### Model Considerations
- TextBlob is used for initial sentiment labeling
- Models are trained on this labeled data
- Performance depends on comment quality and quantity

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🔮 Future Enhancements

- [ ] Add support for multiple languages
- [ ] Implement real-time sentiment analysis
- [ ] Add more advanced NLP models (BERT, RoBERTa)
- [ ] Create a web interface
- [ ] Add sentiment trend analysis over time
- [ ] Implement topic modeling
- [ ] Add export functionality for results

## 🐛 Known Issues

- Some emojis might not convert properly
- Language detection may fail for very short comments
- API rate limits may affect large-scale analysis

## 📞 Contact

For questions or support, please open an issue in the repository.

---

**Note**: Make sure to keep your API key secure and never commit it to version control. Consider using environment variables for sensitive information.
