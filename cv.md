1.  Aleksandr Gordeev
2.  Tel. number: +79117081486; email: gordeeffff@gmail.com
3.  Trying to become frontend developer. Didn't have experience in this sphere before. Learning as fast as I can.
4.  A bit of HTML, CSS, JavaScript and C#.
5.  Training project in C#:
        using System;
        using System.Collections.Generic;
        using System.ComponentModel;
        using System.Data;
        using System.Diagnostics;
        using System.Drawing;
        using System.Linq;
        using System.Text;
        using System.Threading.Tasks;
        using System.Windows.Forms;
        
        namespace BNLauncher
        {
            public partial class Form1 : Form
            {
                public Form1()
                {
                    InitializeComponent();
                }
        
                async void Form1_Load(object sender, EventArgs e)
                {
                    Cmd("start \"\" \"D:\\Battle.net\\Battle.net Launcher.exe\"");
                    await Task.Delay(15000);
                    Cmd("start \"\" C:\\Users\\Alex\\AppData\\Local\\HearthstoneDeckTracker\\HearthstoneDeckTracker.exe");
                    await Task.Delay(45000);
                    if (Process.GetProcessesByName("Hearthstone").Length > 0)
                    {
                        await Task.Delay(2000);
                        Cmd($"taskkill /f /pid \"{Process.GetCurrentProcess().Id}\" &" + 
                            $"taskkill /f /im Battle.net.exe &" +
                            $"taskkill /f /im Agent.exe");
                    }                       
                }
        
                void Cmd(string line)
                {
                    Process.Start(new ProcessStartInfo
                    {
                        FileName = "cmd",
                        Arguments = $"/c {line}",
                        WindowStyle = ProcessWindowStyle.Hidden
                    }).WaitForExit();
                }
            }
        }
6.  Not yet.
7.  2014 - bachelor in European Studies (SPBU, School of International Relations);
    2017 - master in Pacific Studies (SPBU, School of International Relations);
    2020 - fundamentals of programming(ITMO University course)
8.  Have been studying English since I was 8. Now at B2/B2+/C1 level.
