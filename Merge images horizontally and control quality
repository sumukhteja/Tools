from PIL import Image

def merge_images_horizontally(image1_path, image2_path, output_path, format='JPEG', quality=90):
    # Open the two images
    image1 = Image.open(image1_path)
    image2 = Image.open(image2_path)

    # Calculate the maximum width and height
    max_width = max(image1.width, image2.width)
    max_height = max(image1.height, image2.height)

    # Resize the images to the maximum width and height
    image1 = image1.resize((max_width, max_height))
    image2 = image2.resize((max_width, max_height))

    # Create a new image with the calculated dimensions and appropriate mode
    merged_image = Image.new(image1.mode, (2 * max_width, max_height))

    # Paste the first image on the left side of the merged image
    merged_image.paste(image1, (0, 0))

    # Paste the second image on the right side of the merged image
    merged_image.paste(image2, (max_width, 0))

    # Save the merged image with specified format and quality
    merged_image.save(output_path, format=format, quality=quality)
    print(f"Merged image saved as {output_path}")

# Usage example:
image1_path = r'C:\Users\sunny\image1.jpg'
image2_path = r'C:\Users\sunny\image2.png'
output_path = r'C:\Users\sunny\output.jpg'

merge_images_horizontally(image1_path, image2_path, output_path, format='JPEG', quality=100)
