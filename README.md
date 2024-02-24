We aim to transform medical documents from PDF to structured JSON, utilizing pdf2image for conversion, OpenCV for image processing, and pytesseract for optical character recognition (OCR).

**Technical Architecture Overview**

1. **Convert PDF to Image:**
   - **Tool Used:** pdf2image Python module.
   - **Description:** This step involves converting each page of a PDF document (prescription document or patient details document) into separate image files.

2. **Image Processing:**
   - **Tool Used:** OpenCV (cv2 Python module).
   - **Description:** This step will process the converted images to enhance them for better text extraction. Image processing might include noise reduction, thresholding, or other techniques to make the text more legible for OCR.

3. **Extract Text from Image:**
   - **Tool Used:** pytesseract.
   - **Description:** This step involves using OCR (Optical Character Recognition) to extract text from the processed images. The output will be raw text that contains the information from the original PDFs.

4. **Data Structuring and Regular Expressions:**
   - **Tools Used:** JSON for structuring, Python's `re` module for Regular Expressions.
   - **Description:** After extracting the text, this step will structure the data into JSON format. Regular expressions will be used to identify and organize specific data points (like patient names, medication details, dosages, etc.) into a structured form.

### Installations

```bash
pip install pdf2image
pip install pytesseract
pip install opencv-python
pip install Pillow
```

- **Poppler Installation:**
  - **Description:** Visit the Poppler GitHub page (https://github.com/Belval/pdf2image) for instructions on how to install Poppler on your system.
