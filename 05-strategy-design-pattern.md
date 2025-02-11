## Code

```
class Compressor {
    public String compress(String data, String compressionType) {
        switch (compressionType) {
            case "gzip":
                return gzipCompress(data);
            case "deflate":
                return deflateCompress(data);
            case "rar":
                return rarCompress(data);
            default:
                return data;
        }
    }
    private String gzipCompress(String data) {
        // Compress the data using gzip algorithm.
        return "gzip(" + data + ")";
    }
    private String deflateCompress(String data) {
        // Compress the data using deflate algorithm.
        return "deflate(" + data + ")";
    }
    private String rarCompress(String data) {
        // Compress the data using rar algorithm.
        return "rar(" + data + ")";
    }
}


```

## Prompt

\```
{{Paste your code here}}
\```

Can you refactor the above code to make it clean, maintainable code by applying Strategy Design Pattern?