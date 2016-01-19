# Puzzle 3 Activity Start

> [source code](https://github.com/AndroidPuzzle/Easy/tree/master/activity_start)

- start activity

    ```java
    // in MainActivity
    Intent intent = new Intent(this, SecondActivity.class);
    startActivity(intent);
    ```
    
    ```java
    // callback method
    @Override
    protected void onActivityResult(int requestCode, int resultCode, Intent data) {
        Log.e("demo", "request code: " + requestCode +
                ", result code: " + requestCode +
                ", value: " + data.getStringExtra("key"));
    }
    ```
    

- start activity for result

    > `setResult(intent, RESULT_CODE)`
    
    ```java
    // in MainActivity
    Intent intent = new Intent(this, SecondActivity.class);
    startActivityForResult(intent, REQUEST_CODE);
    ```
    
    ```java
    // in SecondActivity
    Intent intent = new Intent();
    intent.putExtra("key", "value");
    setResult(intent, RESULT_CODE);
    finish();
    ```
    
- request code
    - identifing different request.
- result code
    - identifing different result.