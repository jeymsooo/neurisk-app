## Neurisk: Muscle Injury Risk Prediction for Basketball Players

This project is a Streamlit web app that predicts muscle injury risk for basketball players using EMG data collected from MyoWare 2.0 sensors. Users can capture or upload EMG signals, which are filtered and analyzed to extract muscle features. Combined with player info, these features are used by a machine learning model to classify injury risk (low, medium, high) for specific muscle groups. The app then provides evidence-based training and rehab recommendations tailored to the risk level, based on recent sports science research (2020–2025).

## How to Use

1. **Connect the Hardware**  
   - Attach the MyoWare 2.0 EMG sensor to the target muscle group (calves, hamstrings, or quadriceps) following proper electrode placement guidelines.
   - Connect the sensor to the ESP32 and ensure the ESP32 is powered and ready to transmit data.

2. **Launch the Streamlit App**  
   - In your terminal, navigate to the project directory and run:
     ```bash
     streamlit run src/interface/streamlit_app.py
     ```
   - The app will open in your web browser.

3. **Input Player Information**  
   - Enter the player's name, age, height, weight, training frequency, previous injury history, muscle group to test, and contraction type.

4. **Capture or Upload EMG Data**  
   - **To capture live EMG:**  
     - Select the connection type (Serial or WiFi).
     - Click "Capture EMG" and follow the on-screen instructions to enter the ESP32 connection details.
     - Click "Begin Test" to start capturing EMG data.
   - **To upload EMG data:**  
     - Use the file uploader to select a CSV file containing raw EMG data.
   - **To simulate EMG features:**  
     - Check the "Simulate EMG Features" box to generate synthetic data for testing.

5. **Predict Injury Risk**  
   - Once EMG features are available, click the centered "Predict Injury Risk" button.
   - The app will display the predicted risk level (low, medium, or high) for the selected muscle group.

6. **View Training Recommendations**  
   - After prediction, review the evidence-based training and rehabilitation recommendations tailored to the player's risk level, including specific routines for before, during, and after practice.

---

**Note:**  
- Ensure the MyoWare 2.0 sensor is properly attached and the ESP32 is configured for data transmission before capturing EMG.
- For best results, use clean, noise-free EMG data and follow all on-screen instructions.
