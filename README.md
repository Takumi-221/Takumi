# Takumi
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace sort
{
    internal class Program
    {
        static void Main(string[] args)
        {
            //引数が何も指定されていない場合は"引数なし”と表示
            if (args.Length == 0)
            {
                Console.WriteLine("引数なし");
                return;
            }
            //64個以下の整数を引数に指定する
            //引数が64個より大きい場合を"使用方法: 64個以下の整数を入力してください"と表示
            if (args.Length > 64)
            {
                Console.WriteLine("使用方法: 64個以下の整数を入力してください");
                return;
            }
            //すべての引数を整数に変換する
            //値が整数に変換できない場合、FormatExceptionで処理される
            try
            {
                int [] array = new int[args.Length];
            }

            //整数以外が入力された場合、整数のみ入力してくださいと表示させる
            catch (FormatException)
            {
                Console.WriteLine("整数のみ入力してください");
                return;
            }

            //配列の中身を昇順に並び替える
            for (int i = 0; i < args.Length; i++)
            {
                int[] array = new int[args.Length];
                array[args.Length] = int.Parse(args[0]);
            }
            int target;
            target = 0;
            int[] Sort = new int[args.Length];
            Sort[0] = target;

            Array.Sort(target);
            Console.WriteLine("{0}", string.Join("\n", target));
        }
    }
}
