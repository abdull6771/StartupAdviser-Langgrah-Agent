# Startup Adviser

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg) ![LangGraph](https://img.shields.io/badge/LangGraph-Workflows-orange.svg) ![Gradio](https://img.shields.io/badge/Gradio-UI-green.svg) ![License](https://img.shields.io/badge/License-MIT-yellow.svg)

**Startup Adviser** is an AI-powered tool designed to help entrepreneurs refine their startup ideas by providing data-driven insights across key areas: market research, business models, financial forecasts, pitch deck outlines, legal compliance, and a comprehensive report. Built with Python, LangGraph, and Gradio, it leverages a multi-agent workflow to deliver actionable feedback through an interactive web interface, complete with a downloadable PDF report.

## Features

- **Multi-Agent Workflow**: Powered by LangGraph, each agent specializes in a specific analysis:
  - *Market Research*: Identifies trends, opportunities, and market gaps.
  - *Business Model*: Recommends scalable models (e.g., Freemium, Subscription).
  - *Financial Forecast*: Generates realistic projections with clear assumptions.
  - *Pitch Deck*: Crafts concise, investor-ready outlines.
  - *Legal Compliance*: Suggests business structures, IP protection, and regulatory considerations.
  - *Summary*: Compiles all insights into a polished report.
- **Interactive UI**: Built with Gradio for an accessible, user-friendly experience.
- **PDF Export**: Generates professional reports using ReportLab.
- **Scalable Design**: Modular architecture allows for easy enhancements (e.g., web scraping, image generation).

## Demo

Try it out! Enter a startup idea like "A SaaS platform to reduce restaurant food waste" and get a full analysis instantly.

*(Insert a screenshot or GIF of the Gradio interface here once you generate one.)*

## Installation

### Prerequisites
- Python 3.8+
- Git

### Steps
1. **Clone the Repository**
   ```bash
   git clone https://github.com/abdull6771/StartupAdviser.git
   cd StartupAdviser
   ```

2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

   *Required packages:*
   - `langchain_groq`
   - `langgraph`
   - `gradio`
   - `reportlab`
   - *(Add others as needed from your environment)*

3. **Set Up Environment Variables**
   Create a `.env` file in the root directory and add your Grok API key:
   ```bash
   GROQ_API_KEY="your-api-key-here"
   ```

4. **Run the Application**
   ```bash
   python app.py
   ```
   Open the provided Gradio URL (e.g., `http://127.0.0.1:7860`) in your browser.

## Usage

1. Launch the app with `python app.py`.
2. Input your startup idea in the Gradio interface (e.g., "A mobile app for sustainable grocery shopping").
3. Review the outputs:
   - Market Research
   - Business Model
   - Financial Forecast
   - Pitch Deck
   - Legal Compliance
   - Final Report
4. Download the generated PDF report for sharing or presentation.

## Example Output

For the input: *"A SaaS platform to reduce restaurant food waste"*  
- **Market Research**: Highlights 11.4M tons of annual U.S. restaurant food waste and a $25B cost.
- **Business Model**: Recommends a Freemium model for scalability.
- **Financial Forecast**: Projects profitability by Year 3 with a $100K initial investment.
- *(See full output in the PDF report)*

## Project Structure

```
StartupAdviser/
│
├── app.py              # Main script with agent workflow and Gradio UI
├── requirements.txt    # List of dependencies
├── README.md           # This file
└── .env.example        # Example environment file
```

## How It Works

- **LangGraph Workflow**: A `StateGraph` orchestrates the agents, passing data through a defined sequence (Market Research → Business Model → Financial Forecast → Pitch Deck → Legal Compliance → Summary).
- **AI Backend**: Uses `ChatGroq` (Mixtral-8x7B) for fast, high-quality reasoning.
- **Frontend**: Gradio provides an intuitive interface with text inputs and outputs.
- **Report Generation**: ReportLab formats the analysis into a professional PDF.

## Contributing

Contributions are welcome! Here’s how to get involved:
1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/YourFeature`).
3. Commit your changes (`git commit -m "Add YourFeature"`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Open a Pull Request.

### Ideas for Enhancement
- Add real-time web scraping for market data (e.g., using X or web search APIs).
- Integrate image generation for pitch deck visuals.
- Expand financial modeling with sensitivity analysis.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Built with [LangGraph](https://github.com/langchain-ai/langgraph) by LangChain.
- Powered by [Grok](https://xai.com) from xAI.
- UI enabled by [Gradio](https://gradio.app).
- Special thanks to the open-source community!

## Contact

Have questions or want to collaborate? Reach out to me on [LinkedIn](https://www.linkedin.com/in/abdullahi-ahmad-babura-57653b205/) or open an issue here!

---

### Notes for Setup
1. **File Naming**: Save your main script as `app.py` (or adjust the README accordingly).
2. **Requirements File**: Create a `requirements.txt` with:
   ```
   langchain_groq
   langgraph
   gradio
   reportlab
   ```
   Run `pip install -r requirements.txt` to install.
3. **Environment File**: Include a `.env.example` with `GROQ_API_KEY=` for users to copy and fill in.
4. **License File**: Add a basic `LICENSE` file with MIT terms if you choose that license.
5. **Visuals**: After running the app, take a screenshot of the Gradio UI and add it to the README (upload to the repo and link it).

### Posting to GitHub
1. **Create a Repository**: Go to GitHub, create a new repo (e.g., `StartupAdviser`), and push your code.
2. **Add README**: Paste the above content into `README.md` in the root directory.
3. **Commit and Push**:
   ```bash
   git add .
   git commit -m "Initial commit with Startup Adviser code and README"
   git push origin main
   ```
