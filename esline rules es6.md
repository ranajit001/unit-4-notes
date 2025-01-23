```javascrity

module.exports = [
  {
    files: ["*.js"],
    languageOptions: {
      ecmaVersion: "latest", // Automatic
      sourceType: "script", // Automatic
      globals: {
        require: "readonly", // Automatic
        module: "readonly", // Automatic
        exports: "readonly", // Automatic
        _dirname: "readonly", // Automatic
        console: "readonly", // Automatic
      },
    },
    rules: {
      "no-undef": "warn", // Automatically detects undefined variables
      "no-unused-vars": "error", // Automatically detects unused variables
      "quotes": ["error", "double"], // Automatically fixes inconsistent quote style (single c
      "semi": ["error", "always"], // Automatically adds missing semicolons
      "indent": ["error", 2], // Automatically fixes indentation
      "no-console": "off", // Allows console logging (manual fix needed for avoiding excessive
      "eol-last": "error", "always"], // Automatically adds a newline at the end of files
      "space-infix-ops": ["error", { "int32Hint": false }], // Automatically ensures spaces ar
      "no-multi-spaces": ["error", { "ignoreEOLComments": false }], // Automatically fixes mul
    },
  },
];
```
