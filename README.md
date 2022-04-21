import 'package:flutter/material.dart';

const Color darkBlue = Color.fromARGB(255, 18, 32, 47);
void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      theme: ThemeData.dark().copyWith(
        scaffoldBackgroundColor: darkBlue,
      ),
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        body: Center(
          child: MyWidget(),
        ),
      ),
    );
  }
}

class MyWidget extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Container(
        decoration: BoxDecoration(
            image: const DecorationImage(
                image: NetworkImage(
                    'https://i1.sndcdn.com/artworks-6fLoqjecGheizi75-1bVkKg-t500x500.jpg')),
            borderRadius: BorderRadius.circular(40)),
        width: 500,
        height: 500,
        padding: const EdgeInsets.all(10),
        margin: const EdgeInsets.all(10),
        child: Column(children: [
          Row(mainAxisAlignment: MainAxisAlignment.end, children: [
            Container(
              width: 40,
              height: 40,
              decoration: BoxDecoration(
                color: Colors.grey[900],
                borderRadius: BorderRadius.circular(40),
              ),
              child: const Icon(
                Icons.bookmark_border,
                color: Colors.white,
                size: 25.0,
              ),
            )
          ]),
          const SizedBox(height: 140),
          const Text(
              'ELDEN RING, developed by FromSoftware, is a set fantasy action RPG adventure. ',
              style: TextStyle(fontSize: 40, fontWeight: FontWeight.bold)),
          const SizedBox(height: 20),
          Row(children: [
            Icon(Icons.circle, color: Colors.grey[900], size: 40),
            Column(children: const [
              Text('BRA', style: TextStyle(fontWeight: FontWeight.bold)),
              Text('     TODAY', style: TextStyle(fontWeight: FontWeight.bold)),
            ]),
            const SizedBox(width: 310),
            const Text('4h ago',
                style: TextStyle(
                  color: Colors.white,
                  fontSize: 15,
                )),
          ]),
          const SizedBox(height: 20),
          Row(
              mainAxisAlignment: MainAxisAlignment.spaceAround,
              children: const [
                Text('Caio Nascimento',
                    style: TextStyle(
                      fontSize: 15,
                    )),
                Icon(
                  Icons.circle,
                  color: Colors.white,
                  size: 3.0,
                ),
                Text('5 min Reads',
                    style: TextStyle(
                      fontSize: 15,
                    )),
                Icon(
                  Icons.circle,
                  color: Colors.white,
                  size: 3.0,
                ),
                Text('1,2k Upvote',
                    style: TextStyle(
                      fontSize: 15,
                    ))
              ])
        ]));
  }
}
