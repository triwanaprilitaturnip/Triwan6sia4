import 'package : flutter/material.dart';
class HalamanPertama extends StatelessWidget {

@overide
Widget build(BuildContext context) {

return scaffold(
appBar : AppBar(
title : Text ('Halaman Pertama') ,
) ,
body : Center(
child : ListView(
children : <Widget>)[

RaisedButton(
child : Text ('Pindah Halaman Kedua') ,
onPressed : () {
Navigator.pushName(Context , HalamanKedua.routerName) ;
} ,
),
RaisedButton(
child : Text ('Pindah Halaman Ketiga') ,
onPressed : () {
Navigator.pushName(Context , HalamanKetiga.routerName) ;
} ,
),
RaisedButton(
child : Text ('Pindah Halaman Keempat') ,
onPressed : () {
Navigator.pushName(Context , HalamanKeempat.routerName) ;
} ,
),
RaisedButton(
child : Text ('Pindah Halaman Kelima') ,
onPress : () {
Nvigator.pushReplacementNamed(context ,HalamanKelima.routeName) ;
},
),
],
),
),
);
}
}
class HalamanKedua extends StatelessWdidget {

static const String routeName = "/halamanKedua";
@override
Widget build (BuildContext context ) {

return scaffold(
appBar : AppBar(
title: Text("Halaman Kedua"),
),
body :Center(
child : RaisedButton(
child: Text('Kembali'),
onPressed: () [

Nvigator.pop(context);
],
),
),
);
}
}
class HalamanKetiga extends StatelessWdidget {

static const String routeName = "/halamanKetiga";
@override
Widget build (BuildContext context ) {

return scaffold(
appBar : AppBar(
title: Text("Halaman Ketiga"),
),
body :Center(
child : RaisedButton(
child: Text('Kembali'),
onPressed: () [

Nvigator.pop(context);
],
),
),
);
}
}
class HalamanKeempat extends StatelessWdidget {

static const String routeName = "/halamanKeempat";
@override
Widget build (BuildContext context ) {

return scaffold(
appBar : AppBar(
title: Text("Halaman Keempat"),
),
body :Center(
child : RaisedButton(
child: Text('Kembali'),
onPressed: () [

Nvigator.pop(context);
],
),
),
);
}
}
class HalamanKelima extends StatelessWdidget {

static const String routeName = "/halamanKelima";
@override
Widget build (BuildContext context ) {

return scaffold(
appBar : AppBar(
title: Text("Halaman Kelima"),
),
body :Center(
child: Text('Halaman Kelima'),
),
);
}
}
void main () {

runApp(MateriApp
      debugShowCheckedModeBanner: false,
      title: 'Routing Navigation',
      initialRoute: '/',
      routes: {

      '/': (context) => HalamanPertama(),
      HalamanKedua.routeName : (context) => HalamanKedua(),
      HalamanKetiga.routeName : (context) => HalamanKetiga(),
      HalamanKeempat.routeName : (context) => HalamanKeempat(),
      HalamanKelima.routeName : (context) => HalamanKelima(),
      },
      ));
}
