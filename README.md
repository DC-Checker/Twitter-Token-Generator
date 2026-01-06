# Twitter Account Generator (Updated January 2026)

Welcome to the **Twitter Account Generator**. This powerful utility is designed for users who need to generate Twitter accounts efficiently. Our solution is unique in its capability to solve CAPTCHAs automatically, making it the only mass Twitter account generation tool on the market with this feature.

## Features

- **Automated Account Generation**: Generate Twitter accounts in bulk with full automation support
- **Advanced CAPTCHA Solving**: Integrated captcha solving capabilities ensure your accounts are created without interference
- **Email Verification**: Automatic email verification with support for multiple email services
- **SMS Verification**: Handle SMS-based verification through multiple providers
- **Multi-Solver Support**: Support for multiple CAPTCHA solving services including CastleBreaker, CastleSolver, and Botwitter
- **Proxy Support**: Full proxy support for distributed account generation across multiple IPs
- **Multi-threaded Processing**: Generate multiple accounts simultaneously for maximum efficiency
- **User Friendly Interface**: Simple setup and easy-to-use commands make the tool accessible to everyone
- **Open Source**: Review, modify, and contribute to the code as it is fully open-source

## Prerequisites

- Python 3.8+
- All dependencies in `requirements.txt`

## Installation

1. Clone or download this repository
2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Configure your settings in `config.json`:
```json
{
    "api_keys": {
        "silentmail": "your_key",
        "smsbower": "your_key",
        "anymessage": "your_key"
    },
    "solver_keys": {
        "castlebreaker": "your_key",
        "castlesolver": "your_key",
        "botwitter": "your_key",
        "cds": "your_key"
    },
    "gui_settings": {
        "threads": 2,
        "castle": "Botwitter",
        "email": "SMSBower",
        "funcap": "cds"
    }
}
```

## Usage

### GUI Mode
```bash
python gui.py
```

### Configuration

Configure the tool through `config.json`:

- **API Keys**: Add your email and SMS service API keys
- **Solver Keys**: Add CAPTCHA solver service API keys
- **Proxies**: Add proxy URLs for distributed generation
- **Threads**: Set number of concurrent generation threads
- **Castle Solver**: Choose between CastleBreaker, CastleSolver, or Botwitter
- **Email Service**: Select from SilentMail, SMSBower, or Anymessage
- **Funcaptcha Solver**: Choose your preferred solver (cds, etc.)

## Configuration Options

### Castle Solvers
- **CastleBreaker**: High-performance CAPTCHA solving
- **CastleSolver**: Alternative solving method
- **Botwitter**: Twitter-specific solving

### Email Services
- **SilentMail**: Fast email verification
- **SMSBower**: SMS-based verification
- **Anymessage**: Alternative messaging service

### CAPTCHA Solvers
- **CDS Solver**: For Funcaptcha challenges
- **Funbypass**: Additional bypass method
- **Traili**: Alternative solver
- **RoSolve**: Additional solving option

## File Structure

```
.
├── gui.py                 # Main GUI interface
├── register.py            # Account registration logic
├── config.json            # Configuration file
├── requirements.txt       # Python dependencies
├── core/                  # Core functionality
│   ├── headers.py         # HTTP headers management
│   ├── logger.py          # Logging utilities
│   ├── runtime.py         # Runtime management
│   ├── email/             # Email verification services
│   ├── reverse/           # Header parsing and manipulation
│   └── solver/            # CAPTCHA solving implementations
└── unlocker/              # Account unlock utilities
```

## Performance Tips

1. **Optimal Thread Count**: Start with 2-4 threads and increase based on your system
2. **Proxy Rotation**: Use residential proxies for better success rates
3. **Rate Limiting**: Allow delays between requests to avoid detection
4. **Email Services**: Use reliable email services for consistent verification

## Troubleshooting

- **CAPTCHA Failures**: Ensure your solver API keys are valid and have sufficient credits
- **Email Verification Issues**: Check that email service API keys are configured correctly
- **Connection Problems**: Verify proxy connectivity and network settings
- **Rate Limiting**: If accounts fail to generate, increase delays or reduce thread count

## Support

For issues or questions, check the logs in the output directory or review the configuration settings.

## License

This tool is provided as-is. Use responsibly and in accordance with Twitter's Terms of Service.

## Disclaimer

This tool is for educational purposes only. Ensure all use complies with Twitter's Terms of Service and applicable laws. The developers are not responsible for misuse of this tool.
