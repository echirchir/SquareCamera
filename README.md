# SquareCamera
## Description
Android module that takes a square photo using the native Android Camera APIs. The new Camera2 APIs from the L release is not used because support has to go back to SDK version 14 for my own requirement. 

## Features
- Tap to focus
- Two fingers zooming
- Front & Back camera
- Flash mode

## SDK Support
Support from SDK version 14 onwards

## Example
```
private static final int REQUEST_CAMERA = 0;

// Start CameraActivity
Intent startCustomCameraIntent = new Intent(this, CameraActivity.class);
startActivityForResult(startCustomCameraIntent, REQUEST_CAMERA);

// Receive Uri of saved square photo
@Override
protected void onActivityResult(int requestCode, int resultCode, Intent data) {
    if (resultCode != RESULT_OK) return;

    if (requestCode == REQUEST_CAMERA) {
        Uri photoUri = data.getData();
    }
    super.onActivityResult(requestCode, resultCode, data);
}
```

## Video Demo
Link: https://youtu.be/cSGFiP-gZYU
