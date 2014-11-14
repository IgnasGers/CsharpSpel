CsharpGame
==========

A game designed with C#

Hello everybody, today i'm gonna start with my first GitHub project.

I'm going to start just easy by making a game with C# with VisualStudio 2013 For Desktop.

This piece of code shows a random number in a label by clicking on a button

 public partial class Form1 : Form
    {
        private Random rndGen = new Random();
        
        private void WelkomTekst()
        {
            if (MessageBox.Show("Hey, klaar om 21 te spelen ?", "Welkom!", MessageBoxButtons.OKCancel) == DialogResult.Yes) ;
        }

        public Form1()
        {
            InitializeComponent();
        }

        private void Form1_Load(object sender, EventArgs e)
        {
            WelkomTekst();
        }

        private void button1_Click(object sender, EventArgs e)
        {
            int randomNumber = Convert.ToInt16(rndGen.Next(1, 14));
            label1.Text = Convert.ToString(randomNumber) ;
        }
    }
    
    
