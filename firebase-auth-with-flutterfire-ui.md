# FirebaseAuth with FlutterFire UI

Based on [Flutter Tutorial: Firebase Auth Flow with Flutter Fire UI and CLI || Email and Password](https://www.youtube.com/watch?v=BRB_dME_Xe0)

See also [FlutterFire documentation](https://firebase.flutter.dev/docs/overview)

### 1. Create app
```bash
flutter create my_app
```

### 2. Add `FirebaseCore`
```bash
flutter pub add firebase_core
```

### 3. Activate FlutterFire CLI, if you haven't yet
```bash
dart pub global activate flutterfire_cli
```

### 4. Configure FlutterFire
```bash
flutterfire configure
```

### 5. Initialize Firebase
Add imports to `lib/main.dart`
```dart
import 'package:firebase_core/firebase_core.dart';
import 'firebase_options.dart';
```

Modify `main` method in `lib/main.dart`
```dart
Future<void> main() async {
  WidgetsFlutterBinding.ensureInitialized();
  await Firebase.initializeApp(
    options: DefaultFirebaseOptions.currentPlatform,
  );
  runApp(MyApp());
}
```

### 6. Add FlutterFire UI
```bash
flutter pub add flutterfire_ui
```

### 7. Install Firestore
```bash
flutter pub add cloud_firestore
```

### 8. Install Firestore ODM

See [Firestore ODM Documentation](https://github.com/firebase/flutterfire/blob/master/packages/cloud_firestore_odm/README.md)
```bash
flutter pub add cloud_firestore_odm
flutter pub add json_annotation
```

```bash
flutter pub add --dev build_runner
flutter pub add --dev cloud_firestore_odm_generator
flutter pub add --dev json_serializable
```
