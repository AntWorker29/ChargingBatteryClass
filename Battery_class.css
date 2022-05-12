using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace Lucrarea9_cs_Baterie
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }
        System.Drawing.Graphics Desen;
        System.Drawing.Pen Pen_Black, Pen_Green;
        System.Drawing.SolidBrush radiera, Brush_Green;
        baterie incarcare;

        private void Form1_Load(object sender, EventArgs e)
        {
            Desen = CreateGraphics();
            Pen_Black = new System.Drawing.Pen(System.Drawing.Color.Black, 2);
            Pen_Green = new System.Drawing.Pen(System.Drawing.Color.ForestGreen, 2);
            radiera = new System.Drawing.SolidBrush(this.BackColor);
            Brush_Green = new System.Drawing.SolidBrush(System.Drawing.Color.ForestGreen);
            incarcare = new baterie();
            incarcare.initializare(100, 100);
        }

        private void timer1_Tick(object sender, EventArgs e)
        {
            incarcare.desenez_chenar(Desen, Pen_Black);
            for (int i = 0; i <= 7; i++)
            {
                incarcare.liniute_baterie(Desen, Brush_Green, i);
                System.Threading.Thread.Sleep(500);
            }
            incarcare.sterg(Desen, radiera);
        }
    }
    public class baterie
    {
        int x0, y0;
        public void sterg(System.Drawing.Graphics zona_des, System.Drawing.Brush rad)
        {
            zona_des.FillRectangle(rad, x0 + 1, y0 + 1, x0 - 2, y0 + 99);
        }
        public void desenez_chenar(System.Drawing.Graphics zona_des, System.Drawing.Pen creion_a)
        {
            zona_des.DrawRectangle(creion_a, x0, y0, x0, y0 + 100);
            zona_des.DrawRectangle(creion_a, x0 + 14, y0 - 10, x0 * 3 / 4, 10);
        }
        public void liniute_baterie(System.Drawing.Graphics zona_des, System.Drawing.SolidBrush pensula, int nr_liniuta)
        {
            /// bateria va avea 7 liniute, codate de jos in sus cu nr de la 1 la 7
            if (nr_liniuta == 1)
                zona_des.FillRectangle(pensula, x0 + 2, y0 + 170, x0 - 4, y0 / 5);
            if (nr_liniuta == 2)
                zona_des.FillRectangle(pensula, x0 + 2, y0 + 145, x0 - 4, y0 / 5);
            if (nr_liniuta == 3)
                zona_des.FillRectangle(pensula, x0 + 2, y0 + 120, x0 - 4, y0 / 5);
            if (nr_liniuta == 4)
                zona_des.FillRectangle(pensula, x0 + 2, y0 + 95, x0 - 4, y0 / 5);
            if (nr_liniuta == 5)
                zona_des.FillRectangle(pensula, x0 + 2, y0 + 70, x0 - 4, y0 / 5);
            if (nr_liniuta == 6)
                zona_des.FillRectangle(pensula, x0 + 2, y0 + 45, x0 - 4, y0 / 5);
            if (nr_liniuta == 7)
                zona_des.FillRectangle(pensula, x0 + 2, y0 + 20, x0 - 4, y0 / 5);
        }
        public void initializare(int pozx, int pozy)
        {
            x0 = pozx;
            y0 = pozy;
        }
    }
}
