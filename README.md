# Hand-Controlled Pong Game 🏓

A computer vision-based Pong game that uses hand tracking to control the paddles. Built with OpenCV and MediaPipe, this interactive game allows players to control paddles using their hands detected through a webcam.

## 🎮 Features

- **Hand Tracking Controls**: Control left and right paddles using your hands
- **Real-time Gameplay**: Smooth ball physics with collision detection
- **Score Tracking**: Keep track of points for both players
- **Game Over Screen**: Displays final score when ball goes out of bounds
- **Reset Functionality**: Press 'R' to restart the game
- **Live Video Feed**: Small preview window showing the webcam feed

## 🛠️ Technologies Used

- **Python 3.x**
- **OpenCV**: Computer vision and image processing
- **MediaPipe**: Hand detection and tracking
- **NumPy**: Numerical operations

## 📁 Project Structure

```
3_Pong_Game_Recording/
├── script.py              # Main game script
├── utils.py               # Hand detection utilities
├── README.md              # Project documentation
├── Resources/             # Game assets
│   ├── Ball.png          # Ball sprite
│   ├── FrontDesign.png   # Game background/overlay
│   ├── gameover.png      # Game over screen
│   ├── imgbat1.png       # Left paddle sprite
│   └── imgbat2.png       # Right paddle sprite
└── __pycache__/          # Python cache files
```

## 🚀 Installation

1. **Clone or download this repository**

2. **Install required dependencies:**

   ```bash
   pip install opencv-python mediapipe numpy
   ```

3. **Ensure you have a webcam connected to your computer**

## 🎯 How to Play

1. **Run the game:**

   ```bash
   python script.py
   ```

2. **Game Controls:**

   - Use your **left hand** to control the left paddle
   - Use your **right hand** to control the right paddle
   - Move your hands up and down to move the paddles
   - The ball will bounce off paddles and walls
   - Score points when the opponent misses the ball

3. **Game Controls:**
   - Press **'R'** to reset/restart the game
   - Close the window or press **Ctrl+C** to exit

## 🎮 Gameplay Mechanics

- **Paddle Control**: Hand positions control paddle Y-coordinates
- **Ball Physics**: Ball bounces off top/bottom walls and paddles
- **Collision Detection**: Ball reverses X-direction when hitting paddles
- **Scoring**: Points awarded when ball passes opponent's paddle
- **Game Over**: Triggered when ball goes beyond left or right boundaries

## 🔧 Technical Details

### Hand Detection (`utils.py`)

- **HandDetector Class**: Wrapper around MediaPipe hands solution
- **Real-time Processing**: Processes webcam feed for hand landmarks
- **Bounding Box Detection**: Calculates hand position and boundaries
- **PNG Overlay Function**: Alpha blending for transparent image overlays

### Game Logic (`script.py`)

- **Ball Movement**: Physics-based movement with configurable speed
- **Collision System**: Boundary and paddle collision detection
- **Score Management**: Real-time score tracking and display
- **Game State**: Handles game over and reset functionality

## 📊 Configuration

You can modify these variables in `script.py` to customize gameplay:

```python
ball_position = [191, 82]    # Initial ball position
speedX = 15                  # Horizontal ball speed
speedY = 15                  # Vertical ball speed
```

## 🎨 Assets

The game uses PNG images with alpha channels for:

- Ball sprite with transparency
- Paddle sprites for left and right hands
- Background design overlay
- Game over screen

## 🐛 Troubleshooting

**Camera not working:**

- Ensure webcam is connected and not used by other applications
- Try changing the camera index in `cv2.VideoCapture(0)` to `1` or `2`

**Hand detection issues:**

- Ensure good lighting conditions
- Keep hands clearly visible to the camera
- Adjust detection confidence in `HandDetector` parameters

---

**Enjoy playing! 🎮**
