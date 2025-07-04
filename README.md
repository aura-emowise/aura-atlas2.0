Google Maps Platform Awards
final iteration


 EmoWise AI Simulator: Your Personal Mental Compass

 Tagline
Real-time biometric-driven AI for proactive emotional well-being and live emotional landscape visualization.

 Introduction
In today's fast-paced urban environments, mental well-being is more critical than ever. Stress, especially in situations like heavy traffic, can significantly impact our physical and emotional health. EmoWise is a conceptual AI-powered system designed not just to track physical activity, but to act as a mental compass and emotional modulator, helping individuals navigate dynamic environments by understanding and influencing their stress levels in real-time.

This demonstrative web application showcases the core principles of EmoWise: real-time biometric analysis, AI-driven stress detection, a proactive intervention mechanism (nVagus stimulator simulation), and an innovative visual representation of the user's emotional state mapped onto their environment.

This is not focused on fitness; it is a mental well-being application.

You can see more about my project EmoWise by clicking on the link  https://www.f6s.com/emowise-project

 Core Method & Value Proposition
EmoWise's method centers on continuous monitoring of physiological indicators of stress (Heart Rate, Blood Pressure, Electrodermal Activity). Our AI analyzes these real-time metrics to determine the user's current emotional state. When stress is detected, the system simulates the activation of an nVagus stimulator to gently guide the user back to a state of calm. Crucially, EmoWise offers a unique "emotional landscape" visualization on a map, illustrating how the user's mental state interacts with their environment. Imagine "stress clouds" (red) appearing in areas where the user experiences high negative emotional load, and "relax zones" (green) where calm prevails. This provides valuable insights into how different locations or situations affect one's mental well-being over time.


TRY IT   https://aura-emowise.github.io/aura-atlas2.0/EWa-Fit-app.html

 Key Features

*   Live Biometric Simulation: Simulates real-time Blood Pressure, Oxygen Saturation (SpO2), and Electrodermal Activity (EDA) to represent physiological state.
*   AI Stress Detection & Classification:Analyzes biometric data to classify the user's state as `STRESSED`, `RECOVERING`, or `NORMAL`.
*   nVagus Stimulator Simulation: Demonstrates automated activation and deactivation of a biofeedback modulator based on AI-detected stress levels.
*   Google Fit Integration: Connects to Google Fit API to fetch historical Heart Rate (HR) and Oxygen Saturation (SpO2) data, providing context (though real-time interaction is simulated).
*   **Dynamic Emotional Landscape Map:
    *   Visualizes a simulated drive route in an urban environment (e.g., LA downtown traffic).
    *   A moving user marker (representing a vehicle) changes color based on the *current* AI-detected state (Red: Stress, Blue: Recovering, Green: Normal, Gold: Zen Master).
    *   Dynamically generates "emotional clouds" (colored circles) around the user's current location on the map. These clouds accumulate and blend colors based on the *history* of the user's emotional state in that specific area, creating a unique "emotional landscape."
*   Zen Master Achievement: Tracks consecutive periods of a 'Normal' AI state, rewarding the user with a "Zen Master" status and visual cue for prolonged calm.
*   Interactive Simulation Controls: Buttons to manually `Induce Stress` or `Remove Stress`, allowing for direct demonstration of the system's reactivity.
*   Toggleable UI Sections: Event Log, Google Fit Data, and Emotional Landscape Map can be hidden/shown for a cleaner user interface.

## How to Run the Demo (Step-by-Step Guide)

This application is designed to run locally using a simple Python web server, connecting to Google's APIs for Fit data and Maps visualization.

### Prerequisites

*   Python 3: Ensure Python 3 is installed on your system.
*   Modern Web Browser: (e.g., Chrome, Firefox, Edge).

 Google Cloud Project Setup (Crucial for API Access)

    *


### Local Server Launch

1.  **Open PowerShell (or Command Prompt):** Ensure you open a fresh instance.
2.  **Navigate to the project directory:** Use the `cd` command.
    ```bash
    cd "C:\Users\leksp\Desktop\GOO DE" 
    # (Replace with the actual path where EWa-Fit-app.html is located)
    
    Verify the path in the prompt.
3.  **Launch the Python simple HTTP server:**
    ```bash
    python -m http.server
    
    Leave this window open. You should see `Serving HTTP on 0.0.0.0 port 8000 (http://0.0.0.0:8000/) ...`

### Access in Browser

1.  **Open your web browser.**
2.  **In the address bar, type the following URL EXACTLY:**
    ```
    http://127.0.0.1:8000/EWa-Fit-app.html


3.  Press Enter. The application should now load.


## Demonstration Flow / How to Interact

1.  Initial Load:
    *   Observe the "Live Biometric Data" and "System Status" updating (simulated data).
    *   The "Event Log" is hidden by default – click "Show Log" to reveal system messages.
    *   "Google Fit Data (Last 24 Hours, Hourly Averages)" is also hidden.

2.  Authorize Google Fit:
    *   Click the "Authorize Google Fit" button. You will be redirected to a Google consent screen. Accept the permissions.
    *   After authorization, you will be redirected back to the app. The log will show "Google Fit Authorized successfully!".
    *   The "Authorize" button will disappear, and "Fetch Google Fit Data" will appear.

3.  Fetch Google Fit Data:
    *   Click "Show Data" under "Google Fit Data".
    *   Click "Fetch Google Fit Data". The log will show fetching messages, and if available, your HR/SpO2 data from Google Fit will appear.

4.  Simulate Stress & Observe AI Reaction:
    *   Click the "Induce Stress" button.
    *   Observe:
        *   **Live Biometric Data:** Blood Pressure and Electrodermal Activity will increase, SpO2 may slightly drop.
        *   **AI Status:** Will change to `STRESS DETECTED` (red).
        *   **nVagus Stimulator:** Will activate (orange).
        *   **Stress Level Indicator:** Will turn red, showing "Stress Detected! 🚨".

5.  **Simulate Recovery:**
    *   Click the "Remove Stress" button.
    *   Observe:
        *   **Live Biometric Data:** Metrics will start to recover.
        *   **AI Status:** May first go `RECOVERING` (blue), then `NORMAL` (green) as biometrics return to baseline.
        *   **nVagus Stimulator:** Will deactivate (inactive).
        *   **Stress Level Indicator:** Will first show "Recovering..." (blue), then "Stress Level: Normal" (green).
        *   **Zen Master:** Continue running in `NORMAL` state. After 50 cycles (approx 75 seconds), the Stress Level Indicator will turn gold and announce "Zen Master!"

6.  **Explore Emotional Landscape Map:**
    *   Click "Show Map" under "Emotional Landscape Map".
    *   Observe:
        *   The map loading with a blue simulated drive route.
        *   A user marker (arrow shape) moving along the route.
        *   The **user marker's color will change** based on the *current* AI status (Red: Stress, Blue: Recovering, Green: Normal, Gold: Zen Master).
        *   **"Emotional Clouds"**: As the user marker moves and its AI status changes, transparent, colored circles will be drawn around the current location.
            *   **Reddish clouds** indicate historical stress in that specific area.
            *   **Greenish clouds** indicate periods of calm/normalcy in that area.
            *   The clouds accumulate and fade over time, illustrating the "emotional footprint" left by the user in that environment. Try inducing stress in one location, then recovering in another, and see the map reflect it.

## Future Enhancements (Ideas for Next Steps)

*   **Persistent Storage:** Implement a backend to store Google Fit tokens and historical biometric data, moving beyond browser-session-only data.
*   **Real-time Google Fit:** Integrate with Google Fit's real-time API or more advanced data streams for live metric updates.
*   **Advanced AI Models:** Develop machine learning models for stress prediction and personalized intervention strategies based on long-term user data patterns.
*   **Personalization:** Allow users to customize nVagus stimulation profiles or stress thresholds.
*   **Integration with Smart Home/Assistants:** Connect EmoWise to smart home devices or voice assistants for environmental modulation (e.g., dimming lights, playing calm music when stress is detected).
*   **Native Mobile App:** Build a native Android application to directly integrate with Health Connect for broader data access and background processing.

## Technologies Used

*   **Frontend:** HTML5, CSS3 (Tailwind CSS), JavaScript
*   **APIs:** Google Fit API, Google Maps JavaScript API
*   **Local Server:** Python's simple HTTP server

---

Thank you for exploring EmoWise AI Simulator! We believe this project highlights a novel approach to mental well-being in the digital age.
