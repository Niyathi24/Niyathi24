# Voice-Controlled Shopping Assistant

## Project Overview
Developed an AI-powered Chrome extension that enables voice-controlled shopping on Amazon through seamless speech and text input integration. The extension provides intuitive product search and cart management using intent recognition technology.

## Technical Implementation

### Architecture
- **Chrome Extension**: Side panel interface with dual input modes
- **Speech Recognition**: Picovoice Rhino for AI intent recognition
- **DOM Integration**: JavaScript content scripts for Amazon website interaction
- **Dual Input System**: Voice and text command processing

### Key Features
- **Voice Commands**: "Speak Now" functionality for hands-free shopping
- **Intent Recognition**: AI-powered understanding of user shopping requests
- **Amazon Integration**: Direct product search and cart management
- **Seamless UX**: Smooth transition between speech and text input modes

## Technical Challenges & Solutions

### Content Security Policy (CSP) Compliance
- **Challenge**: CSP restrictions limited DOM manipulation capabilities
- **Solution**: Implemented secure message passing between extension components
- **Approach**: Used Chrome extension APIs for compliant website interaction

### Intent Recognition Accuracy
- **Integration**: Leveraged Picovoice Rhino for robust speech-to-intent conversion
- **Optimization**: Fine-tuned recognition parameters for shopping-specific commands
- **Validation**: Comprehensive testing across various product categories

## Results & Impact

### User Experience Improvements
- **Dual Mode Flexibility**: Voice and text input for diverse user preferences
- **Reduced Friction**: Streamlined product discovery and cart management
- **Accessibility**: Voice commands enabling hands-free shopping experience

### Technical Deliverables
- Functional Chrome extension with side panel interface
- Robust intent recognition system integration
- Cross-browser compatibility and Amazon-specific optimization
- Comprehensive documentation and user feedback report

## Technologies Used
- **Frontend**: JavaScript, HTML, Chrome Extension APIs
- **AI/ML**: Picovoice Rhino for speech recognition
- **Integration**: Amazon DOM manipulation, content scripts
- **Tools**: Chrome Developer Tools, Git version control

## Key Learnings
- Chrome extension development and security considerations
- Speech recognition API integration and optimization
- User-centered design for e-commerce applications
- Cross-platform compatibility challenges and solutions

---

**Project Type**: Internship Project
