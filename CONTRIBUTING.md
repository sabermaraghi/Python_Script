Contributing to DNS Updater

Thank you for considering contributing to the DNS Updater project! We welcome contributions from the community to improve the script and its functionality. This document outlines the process for contributing.

How to Contribute





Fork the Repository:





Fork the repository on GitHub to your account.



Clone your fork:

git clone https://github.com/your-username/dns-updater.git
cd dns-updater



Create a Branch:





Create a new branch for your changes:

git checkout -b feature/your-feature-name



Make Changes:





Follow Python PEP 8 style guidelines.



Add or update tests if applicable.



Update documentation (e.g., README.md) if you add features.



Test Your Changes:





Run the script locally to ensure it works:

sudo python3 setup_and_update_dns.py --setup
sudo python3 setup_and_update_dns.py --run



Check logs in /var/log/dns-update.log.



Commit and Push:





Commit your changes with a clear message:

git add .
git commit -m "Add feature: describe your changes"
git push origin feature/your-feature-name



Open a Pull Request:





Go to the original repository on GitHub.



Open a pull request (PR) from your branch to the main branch.



Describe your changes in the PR description, referencing any related issues.

Code of Conduct

Please adhere to our Code of Conduct in all interactions.

Reporting Bugs





Open an issue on GitHub with:





A clear title and description.



Steps to reproduce the bug.



Expected and actual behavior.



Your environment (e.g., Ubuntu version, Python version).

Suggesting Features





Open an issue with the "enhancement" label.



Describe the feature, its use case, and potential implementation.

Development Guidelines





Python Version: Use Python 3.6+.



Style: Follow PEP 8 (use tools like black and flake8).



Testing: Add tests for new features (use unittest or pytest).



Logging: Use the existing logging mechanism for consistency.

Questions?

Contact the maintainers via GitHub issues or [your-email@example.com].

Thank you for contributing!
