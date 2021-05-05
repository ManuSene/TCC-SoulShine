# TCC-SoulShine
Criação do projeto SoulShine em C#

TELA SPLASH

{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void timer1_Tick(object sender, EventArgs e)
        {
            if (progressBar1.Value < 100)
            {
                progressBar1.Value = progressBar1.Value + 2;
            }
            else
            {
                timer1.Enabled = false;
                this.Visible = false;
                Form2 Form2 = new Form2();
                Form2.ShowDialog();
            }
        }
    }
}


TELA LOGIN

public partial class Form2 : Form
    {
        int contador = 3;

        public Form2()
        {
            InitializeComponent();
        }

        private void label1_Click(object sender, EventArgs e)
        {

        }

        private void textBox1_TextChanged(object sender, EventArgs e)
        {

        }

        private void textBox2_TextChanged(object sender, EventArgs e)
        {

        }

        private void button1_Click(object sender, EventArgs e)
        {
            contador -= 1;
            if (contador <= 0)
            {
                MessageBox.Show("Usuário ou Senha inválidos!", "Acesso negado!");
                this.Close();
            }
            else
            {
                if (textBox1.Text == "manuela" && textBox2.Text == "#manuh")
                {
                    Form1 Form1 = new Form1();
                    MessageBox.Show("Seja bem vinde a SoulShine!");
                    this.Hide();
                    this.Close();
                }
                else
                {
                    MessageBox.Show("Usuário ou Senha inválidos!", "ERRO - restam " + contador + " tentativas");
                }
            }
        }

        private void label2_Click(object sender, EventArgs e)
        {

        }
    }
}
