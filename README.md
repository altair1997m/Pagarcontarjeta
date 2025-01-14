# Pagarcontarjeta
package com.example.pagarcontarjeta

import android.os.Bundle
import androidx.activity.ComponentActivity
import androidx.activity.compose.setContent
import androidx.activity.enableEdgeToEdge
import androidx.compose.foundation.layout.Column
import androidx.compose.foundation.layout.fillMaxSize
import androidx.compose.foundation.layout.padding
import androidx.compose.material3.Button
import androidx.compose.material3.OutlinedTextField
import androidx.compose.material3.Scaffold
import androidx.compose.material3.Text
import androidx.compose.runtime.Composable
import androidx.compose.ui.Modifier
import androidx.compose.ui.tooling.preview.Preview
import com.example.pagarcontarjeta.ui.theme.PagarConTarjetaTheme

class MainActivity : ComponentActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        enableEdgeToEdge()
        setContent {
            PagarConTarjetaTheme {
                Scaffold(modifier = Modifier.fillMaxSize()) { innerPadding ->
                    Greeting(
                        name = "Android",
                        modifier = Modifier.padding(innerPadding)
                    )
                }
            }
        }
    }
}

@Composable
fun Greeting(name: String, modifier: Modifier = Modifier) {
    Column {
        //Titulo
        Text(text = "Pagar con tarjeta")

        //Numero de tarjeta
        Text(text = "Número de tarjeta")
        OutlinedTextField(value = "", onValueChange = {})
        Text(text = "Ingrese número de tarjeta")

        //Fecha de expiracion
        Text(text = "Fecha de expiración")
        OutlinedTextField(value = "", onValueChange = {})
        Text(text = "MM/AAAA")
        
        //CVV
        Text(text = "CVV")
        OutlinedTextField(value = "", onValueChange = {})
        Text(text = "Ingrese el CVV")

        //Button
        Button(onClick = {}) {
            Text(text = "Pagar")
        }
    }
}

@Preview(showBackground = true)
@Composable
fun GreetingPreview() {
    PagarConTarjetaTheme {
        Greeting("Android")
    }
