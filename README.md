# AI Product Description Agent

This project demonstrates an AI-powered multi-agent system that automatically generates detailed product descriptions for marketplace landing pages. It leverages Google AI's Gemini models and the Google Agent Development Kit (ADK) to find product variants, assets (images/videos), specifications, and then creates compelling product content.

## Features

- **Multi-Agent Workflow:**
  - **Search Agent:** Finds product variants and EANs using Google Search.
  - **Assets Agent:** Finds relevant images and videos for the product.
  - **Specifications Agent:** Gathers product specifications and features.
  - **Content Editor Agent:** Creates an attractive product description with key features and technical data.
- **Google AI Integration:** Uses Gemini 2.5 Flash models for fast and efficient content generation.
- **Colab Ready:** Designed to run seamlessly in Google Colab.

## Getting Started

### Prerequisites

- Google Cloud project with Gemini API enabled
- Google API key
- Google Colab environment

### Quick Start

1. Open the notebook in Google Colab:

   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ricardoalmeidagrover/AI_Agent_Describe_Product/blob/main/AI_Agent_To_Describe_Product.ipynb)

2. Install the required libraries (the notebook does this automatically):

   ```python
   !pip install -q google-genai google-adk
   ```

3. Set your Google API key as an environment variable in Colab:

   ```python
   import os
   from google.colab import userdata
   os.environ["GOOGLE_API_KEY"] = userdata.get('GOOGLE_API_KEY')
   ```

   *Store your API key in Colab's user secrets for security.*

4. Run all cells in the notebook sequentially.

## Usage

1. When prompted, enter the product name you want to describe.
2. The notebook will run the agents and display:
   - Product variants
   - Assets (images/videos)
   - Specifications
   - Final product description

## Example Output

```
🚀 Starting the system to search product details 🚀

❓ Please, type the PRODUCT NAME that you want to find details:  iPhone 15

Cool! Let's detail the product iPhone 15

--- 📝 Agent 1 Result (Search) ---
> * iPhone 15
> * iPhone 15 Pro
> * iPhone 15 Pro Max
--------------------------------------------------------------
--- 📝 Agent 2 Result: (Assets) ---
> * [iPhone 15 Images](https://www.google.com/search?q=iPhone+15&tbm=isch)
> * [iPhone 15 Pro Images](https://www.google.com/search?q=iPhone+15+Pro&tbm=isch)
> * [iPhone 15 Pro Max Images](https://www.google.com/search?q=iPhone+15+Pro+Max&tbm=isch)
> * [iPhone 15 Videos](https://www.google.com/search?q=iPhone+15&tbm=vid)
--------------------------------------------------------------
--- 📝 Agent 3 Result (Specification) ---
> * **iPhone 15 Specifications:**
>   * Display: Super Retina XDR display
>   * Chip: A16 Bionic chip
>   * Camera: 48MP Main camera
>   * Storage: 128GB, 256GB, 512GB
--------------------------------------------------------------
--- 📝 Agent 4 Result (Content Manager) ---
> The iPhone 15 is the latest smartphone from Apple, featuring a stunning Super Retina XDR display and the powerful A16 Bionic chip. Capture incredible photos with the 48MP Main camera and enjoy ample storage for all your needs.
>
> **Key Features:**
> * Super Retina XDR display
> * A16 Bionic chip
> * 48MP Main camera
>
> **Technical Data:**
> * Display: Super Retina XDR
> * Chip: A16 Bionic
> * Camera: 48MP Main
> * Storage: 128GB, 256GB, 512GB
--------------------------------------------------------------
```

## License

[MIT License](LICENSE) or your preferred license.
