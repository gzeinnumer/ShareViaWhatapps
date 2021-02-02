# ShareViaWhatapps
 only wa

- MainActivity.java
```java
findViewById(R.id.btn).setOnClickListener(new View.OnClickListener() {
    @Override
    public void onClick(View v) {
        Intent intent = new Intent(Intent.ACTION_SEND);
        intent.setType("text/plain");
        intent.setPackage("com.whatsapp");
        intent.putExtra(Intent.EXTRA_TEXT, "The text you wanted to share");
        try {
            startActivity(intent);
        } catch (android.content.ActivityNotFoundException ex) {
            Toast.makeText(MainActivity.this, "Whatsapp have not been installed.", Toast.LENGTH_SHORT).show();
        }
    }
});
```

---

```
Copyright 2021 M. Fadli Zein
```
