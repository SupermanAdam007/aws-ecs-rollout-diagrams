# Jupyter notebooks to create images of Cloud Architecture
Just don't complicate things. They said... :D

## Powered by [Cloud Diagram Coder GPT](https://chat.openai.com/g/g-gy0aKxsX3-cloud-diagram-coder)

## GIF creation

### Explanation of Parameters in `create_fading_gif`

#### `duration` (default: `0.1`)
- **Description**: Controls the duration of each frame in the GIF, measured in seconds.
- **Default Value**: `0.1` seconds (100 milliseconds) per frame.
- **Impact**:
  - Affects how long each frame (both in static display and during the fading transition) is displayed.
  - Decreasing this value speeds up the animation, while increasing it slows down the animation.

#### `fade_duration` (default: `10`)
- **Description**: Specifies the number of frames used for the fading transition between two images.
- **Default Value**: `10` frames for the fade effect.
- **Impact**:
  - Determines the number of frames in the fade transition from one image to the next.
  - The total duration of the fade effect is calculated as `fade_duration` multiplied by `duration`. 
  - For example, `fade_duration = 10` and `duration = 0.1` results in a 1-second fade effect.

#### `static_duration` (default: `50`)
- **Description**: Controls how many frames each static image is displayed before the fading transition starts.
- **Default Value**: `50` frames for each static image.
- **Impact**:
  - Determines the duration each image is displayed statically (without fading).
  - The total time an image is shown statically is calculated as `static_duration` multiplied by `duration`.
  - For instance, `static_duration = 50` and `duration = 0.1` leads to each image being displayed for 5 seconds before fading.
