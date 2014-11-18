CsharpGame
==========

A game designed with C#

Hello everybody, today i'm gonna start with my first GitHub project.

I'm going to start just easy by making a game with C# with VisualStudio 2013 For Desktop.

This piece of code shows a random number in a label by clicking on a button

 public partial class Form1 : Form
    {
        private Random rndGen = new Random();

        int punten;

        Form form2 = new Form();

        private void WelkomstWoord()
        {
            var result = MessageBox.Show("Hey, wil je graag een spel spelen?", "Spel kiezen", MessageBoxButtons.OKCancel);
            if (result == DialogResult.Cancel)
            {
                Close();
            }
            else
            {
                form2.Show();
            }
        }

        public Form1()
        {
            InitializeComponent();
            form2
        }
        
        private void Form1_Load(object sender, EventArgs e)
        {
            WelkomstWoord();
        }

        private void KaartGever_Click(object sender, EventArgs e)
        {
            int randomNumber = rndGen.Next(1, 14);

           punten += randomNumber;

            DealerKaarten.Text = randomNumber.ToString();
            SpelerKaarten.Text = punten.ToString();
            if ( Convert.ToInt32(SpelerKaarten.Text) > 21)
            {
                var result = MessageBox.Show("Mijn excuses u heeft meer dan 21, wilt u nog een keer?", "Sorry!",         MessageBoxButtons.YesNo);
                 if (result == DialogResult.Yes)
                {
                    DealerKaarten.Text = "";
                    SpelerKaarten.Text = "";
                    form2.Show();
                }
                 else
                 {
                     Close();
                 }
            }
            
        }
    }
