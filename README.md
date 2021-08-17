import'package:flutter/material.dart';
import 'dart:math';

class atividade extends StatefulWidget {
  const atividade({Key? key}) : super(key: key);

  @override
  _atividadeState createState() => _atividadeState();
}
class _atividadeState extends State<atividade> {

  var _letras=[
    "IMAGEM DELETADA",
  ];
  var _gerar = "DELETAR";
  void letrasGeradas(){
    var randomico = Random().nextInt(1);
    setState(() {
      _gerar = _letras [randomico];
    });
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
        appBar: AppBar (
          title: Text("Deletando imagens"),
          backgroundColor: Colors.pink,

        ),
        body: Container(
          padding: EdgeInsets.all(60),
          decoration: BoxDecoration(
              border: Border.all(width: 10,color: Colors.pink)
          ),
          child: Column(
            mainAxisAlignment: MainAxisAlignment.spaceEvenly,
            crossAxisAlignment: CrossAxisAlignment.center,

            children: <Widget> [
              Image.asset("imagens/verdura.png"),
              Padding(padding: EdgeInsets.only(top: 10),
                //ignore: deprecated_member_use
                child: RaisedButton(
                  color: Colors.pinkAccent,
                  textColor: Colors.white,
                  child: Text("DELETAR",
                    style: TextStyle(fontSize: 20),
                  ),
                  onPressed: letrasGeradas,
                ),
              ),
              Image.asset("imagens/futra.png"),
              Padding(padding: EdgeInsets.only(top: 10),
                //ignore: deprecated_member_use
                child: RaisedButton(
                  color: Colors.lightBlueAccent,
                  textColor: Colors.white,
                  child: Text("DELETAR",
                    style: TextStyle(fontSize: 20),
                  ),
                  onPressed: letrasGeradas,
                ),
              ),
              Image.asset("imagens/planeta.png"),
              Padding(padding: EdgeInsets.only(top: 10),
                //ignore: deprecated_member_use
                child: RaisedButton(
                  color: Colors.lightBlueAccent,
                  textColor: Colors.white,
                  child: Text("DELETAR",
                    style: TextStyle(fontSize: 20),
                  ),
                  onPressed: letrasGeradas,
                ),
              ),
            ],
          ),
        )
    );
  }
}
