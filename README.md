# 📄 AI Job Recommender System

A powerful AI-driven job recommendation application that analyzes your resume and provides personalized job suggestions from LinkedIn and Naukri, along with skill gap analysis and career roadmap planning.

## 🌟 Features

- **Resume Analysis**: Extract and summarize your resume using OpenAI's GPT models
- **Skill Gap Analysis**: Identify missing skills, certifications, and experiences needed for better job opportunities
- **Career Roadmap**: Get personalized recommendations for skill development and career progression
- **Multi-Platform Job Search**: Fetch job recommendations from:
  - LinkedIn (global job market)
  - Naukri (India-focused job market)
- **Intelligent Keyword Extraction**: Automatically generate relevant job search keywords based on your resume
- **User-Friendly Interface**: Built with Streamlit for an intuitive web experience

## 🚀 Getting Started

### Prerequisites

- Python 3.13 or higher
- OpenAI API Key
- Apify API Token

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd Job-Recommender-System
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```
   Or using Python package manager:
   ```bash
   pip install streamlit openai pymupdf python-dotenv apify-client
   ```

3. **Set up environment variables**
   
   Create a `.env` file in the project root directory:
   ```env
   OPENAI_API_KEY=your_openai_api_key_here
   APIFY_API_TOKEN=your_apify_api_token_here
   ```

### Running the Application

1. **Start the Streamlit app**
   ```bash
   streamlit run app.py
   ```

2. **Open your browser**
   - The app will automatically open at `http://localhost:8501`
   - If not, navigate to the URL shown in the terminal

## 📋 How to Use

1. **Upload Resume**: Click on the file uploader and select your resume (PDF format)
2. **AI Analysis**: The system will:
   - Extract and summarize your resume
   - Analyze skill gaps and missing areas
   - Generate a personalized career roadmap
3. **Get Job Recommendations**: Click the "Get Job Recommendations" button to fetch relevant jobs from LinkedIn and Naukri
4. **View Results**: Browse through job listings with direct links to apply

## 📁 Project Structure

```
Job-Recommender-System/
├── app.py                 # Main Streamlit application
├── mcp_server.py         # MCP server implementation
├── requirements.txt      # Project dependencies
├── pyproject.toml        # Project configuration
├── README.md             # This file
└── src/
    ├── __init__.py       # Package initialization
    ├── helper.py         # Utility functions (PDF extraction, OpenAI calls)
    ├── job_api.py        # Job fetching APIs (LinkedIn & Naukri)
```

## 🔧 Dependencies

| Package | Version | Purpose |
|---------|---------|---------|
| streamlit | >=1.56.0 | Web application framework |
| openai | >=2.33.0 | AI language model integration |
| pymupdf | >=1.27.2.3 | PDF text extraction |
| python-dotenv | >=1.2.2 | Environment variable management |
| apify-client | >=2.5.0 | Job scraping from LinkedIn & Naukri |
| mcp | >=1.27.0 | Model Context Protocol support |

## 🤖 AI-Powered Features

### Resume Summary
Extracts key information from your resume including:
- Skills and expertise
- Educational background
- Work experience and achievements

### Skill Gap Analysis
Identifies:
- Missing technical skills
- Required certifications
- Industry-specific experience gaps

### Career Roadmap
Provides personalized recommendations for:
- Skills to learn
- Certifications to pursue
- Industry exposure opportunities

## 🌐 Job Sources

- **LinkedIn**: Global job market with international opportunities
- **Naukri**: India's largest job portal for region-specific positions

## 📝 Configuration

### Environment Variables Required

- `OPENAI_API_KEY`: Your OpenAI API key for GPT access
  - Get it from: https://platform.openai.com/api-keys

- `APIFY_API_TOKEN`: Your Apify token for job scraping
  - Get it from: https://apify.com/

### Customization

Edit parameters in `src/job_api.py`:
- `location`: Change default search location for LinkedIn jobs (default: "Dhaka")
- `rows`: Adjust number of job results (default: 60)
- `sortBy`: Change sorting preference (default: "relevance")

## ⚙️ Technical Architecture

- **Frontend**: Streamlit (Python-based web UI)
- **AI Engine**: OpenAI GPT API
- **Data Extraction**: PyMUPDF for PDF processing
- **Job Scraping**: Apify platform with residential proxies
- **Data Management**: Apify datasets

## 🔒 Security Notes

- Keep your `.env` file private and never commit it to version control
- Add `.env` to `.gitignore`
- Rotate API keys regularly
- Use environment variables for sensitive credentials

## 📊 Example Workflow

1. User uploads a resume (PDF)
2. System extracts text using PyMUPDF
3. OpenAI analyzes and generates:
   - Professional summary
   - Skill gap analysis
   - Career development roadmap
4. User reviews insights and clicks job search
5. System extracts relevant keywords from resume summary
6. Apify fetches jobs from LinkedIn and Naukri
7. Results displayed with direct application links

## 🐛 Troubleshooting

### API Connection Issues
- Verify your API keys are correctly set in `.env`
- Check internet connectivity
- Ensure API quota is not exceeded

### PDF Extraction Problems
- Ensure PDF is not password-protected
- Try with a different PDF file to isolate the issue
- Check PyMUPDF version compatibility

### No Jobs Found
- Try different keywords
- Check location settings
- Ensure Apify API token is valid

## 🤝 Contributing

Contributions are welcome! Please:
1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Open a pull request

## 📄 License

This project is licensed under the MIT License - see LICENSE file for details.

## 📧 Support

For issues, questions, or suggestions:
- Create an issue in the repository
- Contact: [Your Contact Info]

## 🙏 Acknowledgments

- OpenAI for GPT API
- Apify for job scraping infrastructure
- Streamlit for the web framework
- PyMUPDF for PDF processing

---

**Version**: 0.1.0  
**Last Updated**: May 2026  
**Status**: Active Development
