# I.M.C.
Faça um programa que peça ao usuario seu peso (em kg), altura (em metros), e que calcule o Indice de Massa Corporal (IMC). Exiba o valor do IMC e uma mensagem, indicando a classificação do IMC:
Abaixo de 18.5: "Abaixo do peso"; Entre 18.5 e 24.9: "Peso Normal"; Entre 25 e 29.9: "Sobrepeso", e acima de 30: "Obesidade".
______________________________________________________________________________________________________________________________________________________________________________________________________
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace IMC
{
    public class Program
    {
        static void Main(string[] args)
        {
            string acao, resultado, caminho;
            double peso, altura, imc;

            acao = Console.ReadLine().ToUpper();
            Console.WriteLine();

            while (acao != "S")
            {
                if (acao == "N")
                {
                    Console.Write("Informe o peso: ");
                    double.TryParse(Console.ReadLine(), out peso);

                    Console.Write("Informe a altura: ");
                    double.TryParse(Console.ReadLine(), out altura);

                    imc = Math.Round((peso / (altura * altura)));
                }
                if (imc < 18.5)
                {
                    resultado = "Abaixo do peso";
                }
                else if (imc > 18.5 && imc < 25)
                {
                    resultado = "Peso normal";
                }
                else if (imc > 25 && imc < 30)
                {
                    resultado = "Sobrepeso";
                }
                else if (imc > 30 && imc < 35)
                {
                    resultado = "Obesidade";
                }





                Console.ReadKey();
            }
        }
    }
}
