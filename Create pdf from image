import img2pdf

def convert_image_to_pdf(image_path, output_pdf_path):
    with open(output_pdf_path, "wb") as pdf_file, open(image_path, "rb") as image_file:
        pdf_file.write(img2pdf.convert(image_file))

# Taking input image file path from the user
image_path = input("Enter the image file path: ")

# Taking output PDF file path from the user
pdf_path = input("Enter the output PDF file path: ")

# Calling the conversion function
convert_image_to_pdf(image_path, pdf_path)

print("Image converted to PDF successfully!")
