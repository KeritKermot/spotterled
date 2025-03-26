import time
import board
import neopixel

# Configuration
LED_PIN = board.D18  # GPIO18 (pin 12)
LED_COUNT = 256  # Number of LEDs in the matrix (16x16)
LED_BRIGHTNESS = 0.2  # Brightness (0.0 to 1.0)

# Initialize the LED matrix
pixels = neopixel.NeoPixel(LED_PIN, LED_COUNT, brightness=LED_BRIGHTNESS, auto_write=False)

# Function to clear the matrix
def clear_matrix():
    pixels.fill((0, 0, 0))
    pixels.show()

# Function to set a pixel color
def set_pixel(x, y, color):
    index = y * 16 + x
    pixels[index] = color

# Example animation
def example_animation():
    for y in range(16):
        for x in range(16):
            set_pixel(x, y, (255, 0, 0))  # Set pixel to red
            pixels.show()
            time.sleep(0.01)
    clear_matrix()

if __name__ == "__main__":
    try:
        example_animation()
    except KeyboardInterrupt:
        clear_matrix()