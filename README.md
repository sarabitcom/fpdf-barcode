# fpdf-barcode
library to generate pdf document with bar-code support


# Create Object
<pre>
 $pdf = new \Sarabitcom\Fpdf\FpdfCode39('P', 'mm', 'A4');          
</pre>
# Set Margins
<pre>
  $pdf->SetLeftMargin(68);
  $pdf->SetRightMargin(1);
  $pdf->SetTopMargin(90);
</pre>
 
 # Add Page
 <pre>
  $pdf->AddPage();
 </pre>

# Set Headers (Optional)
<pre>
$pdf->SetAuthor('You Name');
$pdf->SetCreator('Sarabit PDF Barcode');
$pdf->SetTitle('Document Title');
$pdf->SetSubject('Document Subject');
</pre>

# Add Barcode
<pre>
 $pdf->Code39(138, 160, "1234567890", 1, 10);
</pre>

# Set Image
<pre>
$imagePath = "/home/user/yourimage.jpeg"; // Absolute Path
$pdf->Image($imagePath, 0, 0, 210, 297);
</pre>

# Set Font
<pre>
// Normal
$pdf->SetFont('Times', '', 12);
// Bold
$pdf->SetFont('Times', 'B', 11);
// Italic
$pdf->SetFont('Times', 'I', 11);
</pre>

# Make Cell
<pre>
$pdf->Text(68, 164, "Your Text Here");
</pre>

#Output
<pre>
$pdf->Output('file.pdf', 'I');
</pre>
