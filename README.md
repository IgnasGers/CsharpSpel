CsharpSpel
==========

Een spel ontworpen met Csharp

Dag iedereen, ik ga vandaag beginnen met mijn 1ste project op GitHub.

Ik ga gewoon simpel beginnen door een spel te maken op VisualStudio 2013 For Desktop.

    Dit stukje code laat zien dat er een random getal wordt afgebeeld telkens als je op de button klikt.
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
    
    
