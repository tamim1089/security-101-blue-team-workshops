# Security 101: Blue Team Basics

A 4-part workshop series on defensive cybersecurity, progressing from fundamental security concepts to machine learning-based malware detection. Delivered at Abu Dhabi University's Google Developer Group on Campus.

## Series Overview

This workshop series takes a practical approach to teaching blue team security skills. Each session builds on the previous one, moving from theory to hands-on implementation. By the end of the series, students go from learning basic security principles to training neural networks on malware samples.

**Target Audience**: Beginners with no prior cybersecurity experience  
**Total Duration**: Approximately 6 hours across 4 workshops  
**Format**: Mix of lectures, live demonstrations, and hands-on labs

## Workshop Breakdown

### [Workshop 1: Introduction to Cybersecurity](./workshop-1-intro-to-cybersecurity)
**Duration**: 90 minutes  
**Type**: Lecture + Discussion

Introduction to core cybersecurity concepts and the blue team mindset. Covers the CIA triad, least privilege, zero trust architecture, secure by design, and defense in depth. Explores different career paths in defensive security.

**Key Topics**:
- What cybersecurity actually is (beyond just "hacking")
- The five core security principles that prevent 99% of attacks
- Blue team career paths: SOC analyst, incident responder, digital forensics, malware analyst
- Why security must be built into systems from the start

### [Workshop 2: Linux Fundamentals](./workshop-2-linux-fundamentals)
**Duration**: 90 minutes  
**Type**: Hands-on Lab

Practical introduction to Linux command line essentials. Students connect via SSH to isolated Docker containers and learn file system navigation, permissions, process management, and basic networking commands.

**Key Topics**:
- File operations and directory navigation
- Understanding and modifying permissions with chmod
- Process monitoring and management
- Network utilities (ping, netstat, traceroute)
- Output redirection and piping

**Lab Setup**: SSH access to individual Docker containers running Debian

### [Workshop 3: Security Monitoring with Wazuh](./workshop-3-wazuh-siem)
**Duration**: 60 minutes  
**Type**: Interactive Dashboard Demo

Introduction to Security Information and Event Management (SIEM) using Wazuh. Live demonstration of log aggregation, threat detection, and security event correlation using a real attack scenario.

**Key Topics**:
- How SIEM frameworks collect and analyze security data
- Agent-based monitoring architecture
- Dashboard navigation and log filtering with DQL
- Writing custom detection rules
- Mapping attacks to the MITRE ATT&CK framework

**Lab Setup**: Hosted Wazuh server with Raspberry Pi agent, live SSH brute force demonstration

### [Workshop 4: Malware Analysis with Machine Learning](./workshop-4-malware-analysis-ml)
**Duration**: 90 minutes  
**Type**: Theory + Code Walkthrough

Explores how machine learning can automate malware detection. Explains the binary-to-image conversion technique and walks through training a convolutional neural network to classify malware families.

**Key Topics**:
- Malware behavior: exfiltration, persistence, pivoting
- Static vs dynamic analysis approaches
- Converting executable files to grayscale images
- Training ResNet50 on malware datasets
- Achieving 94% classification accuracy

**Lab Setup**: Google Colab notebook with complete training pipeline

## Prerequisites

**Workshop 1**: None - suitable for complete beginners

**Workshop 2**: Basic computer literacy, familiarity with using a terminal is helpful but not required

**Workshop 3**: Understanding of Workshop 2 Linux commands recommended

**Workshop 4**: Basic understanding of Python, familiarity with machine learning concepts helpful but not required

## Getting Started

Each workshop folder contains:
- Detailed README with learning objectives and key concepts
- Presentation slides (PDF format)
- Lab materials and code samples where applicable
- Additional resources and recommended reading

**Recommended Path**: Complete workshops in order (1→2→3→4) for the best learning experience.

## Tools and Technologies Used

- **Linux**: Debian-based systems, SSH, bash
- **SIEM**: Wazuh (open-source security monitoring)
- **Machine Learning**: Python, PyTorch, ResNet50, Google Colab
- **Virtualization**: Docker (for isolated lab environments)

## Additional Resources

### General Cybersecurity
- [MITRE ATT&CK Framework](https://attack.mitre.org) - Comprehensive knowledge base of adversary tactics
- [OWASP Top 10](https://owasp.org/www-project-top-ten/) - Most critical web application security risks
- [NIST Cybersecurity Framework](https://www.nist.gov/cyberframework)

### Linux Practice
- [OverTheWire: Bandit](https://overthewire.org/wargames/bandit/) - Learn Linux through security challenges
- [Hack The Box Academy](https://academy.hackthebox.com) - Structured learning paths
- [TryHackMe](https://tryhackme.com) - Guided cybersecurity training

### SIEM and Monitoring
- [Wazuh Documentation](https://documentation.wazuh.com)
- [Splunk Fundamentals](https://www.splunk.com/en_us/training.html)
- [Elastic Security](https://www.elastic.co/security)

### Malware Analysis
- [Malware Unicorn](https://malwareunicorn.org) - Reverse engineering workshops
- [VirusTotal](https://www.virustotal.com) - Multi-scanner file analysis
- [ANY.RUN](https://any.run) - Interactive malware sandbox
- "Practical Malware Analysis" by Michael Sikorski

### Certifications Path

**Entry Level**:
- CompTIA Security+
- (ISC)² Certified in Cybersecurity (CC)

**Blue Team Focused**:
- Practical Junior Security Analyst (PJSA) - TCM Security
- Certified SOC Analyst (CSA) - SANS/GIAC
- Certified Defense Analyst (CDA) - TCM Security

**Advanced**:
- GIAC Certified Incident Handler (GCIH)
- GIAC Certified Forensic Analyst (GCFA)
- Offensive Security Defense Analyst (OSDA)

## Workshop Recordings

Full video recordings of all workshops are available on YouTube:  
[Workshop Series Playlist](https://www.youtube.com/playlist?list=PLd8mAolo75WSeTH2MJNjfGFE1KQbLuTlo)

## About

These workshops were created and delivered as part of the Google Developer Group on Campus (GDGOC) at Abu Dhabi University. The goal is to make defensive cybersecurity accessible to students with no prior security experience.

**Instructor**: Abdulrahman Tamim  
Second Year Cyber Security Engineering Student, Abu Dhabi University  
Focus: Malware analysis and low-level security

**Contact**:  
- LinkedIn: [Abdulrahman Tamim](https://linkedin.com/in/abdulrahman-tamim)
- Blog: [Your blog URL if you have one]

## Contributing

Found an error or have suggestions for improving the workshops? Contributions are welcome:

1. Fork the repository
2. Create a feature branch (`git checkout -b improve-workshop-2`)
3. Commit your changes (`git commit -am 'Add missing chmod examples'`)
4. Push to the branch (`git push origin improve-workshop-2`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

Educational materials can be freely used with attribution to the original source.

## Acknowledgments

- Abu Dhabi University's Google Developer Group on Campus for hosting and support
- All workshop participants for their engagement and valuable feedback
- The open-source security community for tools like Wazuh and the malware research community for making datasets publicly available

---

**Note**: These materials represent a learning journey from basic concepts to advanced techniques. While designed for beginners, later workshops assume familiarity with earlier content. The hands-on nature of these workshops means the real learning happens when you actually run the commands and code yourself.

Start with Workshop 1 and work your way through. By Workshop 4, you'll be training neural networks on malware - and actually understanding what's happening under the hood.
