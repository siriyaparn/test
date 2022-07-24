// Prepare a simple Markdown example
var code = "### Hello World" +
        "\r\n" +
        "[visit applications](https://aspose.com)";
// Create a Markdown file
System.IO.File.WriteAllText(dataDir + "document.md", code);

// Convert Markdown to HTML document
//Aspose.Html.Converters.Converter.ConvertMarkdown("document.md", "document.html");
HTMLDocument document = Aspose.Html.Converters.Converter.ConvertMarkdown(dataDir + "document.md");

// Invoke the ConvertHTML method to convert the HTML to PDF.
Aspose.Html.Converters.Converter.ConvertHTML(document, new Aspose.Html.Saving.PdfSaveOptions(), dataDir + "output.pdf");
