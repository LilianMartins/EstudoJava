import java.wat.*;
import java.awt.event.*;
import javax.swing.*;
import javax.swing.event.*;
//Procure no javadoc cada umas das classes que vc. não conhece neste exemplo. Assim vc. saberá em que pacotes elas estão e as conhecerá melhor! ;-)
public class MeuNote extends JFrame{
    //Componentes
    private JToolBar toolbar = new JToolBar("Ferramentas");
    private JMenuBar menubar = new JMenuBar();
    private JMenu arquivo = new JMenu("Arquivo");
    private JTextArea texto = new JTextArea();
     
    //Ações:
    private Action novo = new NovoAction(this.texto);
    private Action salvar = new SalvarAction(this.texto);
    private Action abrir = new AbrirAction();
 
    public MeuNote(){
        super("Meu Notepad");
        //Desliga automaticamente a aplicação quando o usuário fecha a janela.
        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        Container interno = this.getContentPane();
        this.montaMenu();
        this.montaToolBar();
        this.montaGUI();
    }
    private void montaMenu(){
        //JMenuItem pode ser construído a partir de um objeto que implementa a interface Action
        JMenuItem itemNovo = new JMenuItem(this.novo);
        JMenuItem itemSalvar = new JMenuItem(this.salvar);
        JMenuItem itemAbrir = new JMenuItem(this.abrir);
        this.arquivo.add(itemNovo);
        this.arquivo.add(itemSalvar);
        this.arquivo.add(itemAbrir);
        this.menubar.add(this.arquivo);
        this.setJMenuBar(this.menubar);
    }
 
    private void montaToolBar(){
        //Barras de ferramenta swing também aceitam objetos que implementam Action como parâmetro de construtor
        this.toolbar.add(this.novo);
        this.toolbar.add(this.salvar);
        this.toolbar.add(this.abrir);
    }
 
    private void montaGUI(Container interno){
        interno.setLayout(new BorderLayout());
        interno.add(this.toolbar, BorderLayout.NORTH);
        interno.add(new JScrollPane(this.texto));
    }
 
    public static void main(String args[]){
        //Vc. sabe o que fazer...
    }
}
