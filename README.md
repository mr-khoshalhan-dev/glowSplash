

##ٍExmaple code




import 'package:flutter/material.dart';
import 'package:glow_splash/glow_splash.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: GlowSplashScreen(
        bgGradient: const LinearGradient(
          colors: [Colors.blue, Colors.purple],
          begin: Alignment.topLeft,
          end: Alignment.bottomRight,
        ),
        logo: Image.network(
          'https://flutter.dev/images/flutter-logo-sharing.png',
          width: 100,
        ),
        showTextLogo: true,
        logoText: "GlowSplash",
        textStyle: const TextStyle(
          fontSize: 28,
          fontWeight: FontWeight.bold,
          color: Colors.yellow,
        ),
        loaderType: LoaderType.dots,
        nextButton: Container(
          padding: const EdgeInsets.symmetric(horizontal: 24, vertical: 12),
          decoration: BoxDecoration(
            color: Colors.white,
            borderRadius: BorderRadius.circular(8),
          ),
          child: const Text("Next", style: TextStyle(color: Colors.black)),
        ),
        onNextPressed: () {
          print("Next pressed!");
        },
        duration: const Duration(seconds: 5),
      ),
    );
  }
}


