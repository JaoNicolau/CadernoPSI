==XML==  
LinearLayout com os dois botões de Previous e Next  
LinearLayout    
        android:layout_width="match_parent"    
        android:layout_height="wrap_content">    
  
<Button            android:id="@+id/btnPrevious"    
            android:layout_width="wrap_content"    
            android:layout_height="60dp"    
            android:layout_marginTop="32dp"    
            android:background="@drawable/gradient_button"    
            android:text="Previous"    
            android:textStyle="bold"    
            android:textColor="@color/white"    
            app:backgroundTint="@null"    
            />    
  
<Button            android:id="@+id/btnNext"    
            android:layout_width="wrap_content"    
            android:layout_height="60dp"    
            android:layout_marginTop="32dp"    
            android:background="@drawable/gradient_button"    
            android:text="Next"    
            android:textStyle="bold"    
            android:textColor="@color/white"    
            app:backgroundTint="@null"    
            />    
  
LinearLayout

==EditText para mostrar o nome das tarefas==  
EditText    
    android:id="@+id/editNome"    
    android:layout_width="match_parent"    
    android:layout_height="55dp"    
    android:background="@drawable/glass_background_edit_text"    
    android:paddingStart="20dp"    
    android:textColor="@color/white"    
    android:editable="false"    
    />

==Declarar as variáveis botões==  
Button btnNext;    
Button btnPrevious;

==Declarar variável para mostrar o nome da tarefa==  
EditText editNome;

==Variável para percerrer os index do Array==  
int currentIndexTask;

==Inicializar a flag currentIndexTask==    
this.currentIndexTask = 0;    

==Inicializar o EditNome==  
this.editNome = findViewById(R.id.editNome);

==Inicializar o botão==    
this.btnNext = findViewById(R.id.btnNext);  

==Quando clicares no botão de next ele vai passar de tarefa==  
this.btnNext.setOnClickListener(v -> {    
    Toast.makeText(this, "Next clicado", Toast.LENGTH_SHORT).show();    
     ==Passar para próxima tarefa==    
    this.currentIndexTask = this.currentIndexTask + 1;    
    ==Chamar o método==  
    this.tasksNavigate();    
});  

==Inicializar o btnPrevious==  
this.btnPrevious = findViewById(R.id.btnPrevious);  

==Quando clicares no botão de previous ele vai voltar para a tarefa que estavamos==   
this.btnPrevious.setOnClickListener(v -> {    
    Toast.makeText(this, "Previous clicado", Toast.LENGTH_SHORT).show();    
     ==Passar para a tarefa anterior==   
    this.currentIndexTask = this.currentIndexTask - 1;    
  
    this.tasksNavigate();    
});

==Método para navegar entre os index e ir buscar o nome==  
public void tasksNavigate(){    
    this.editNome.setText(this.listaDeTarefas.get(currentIndexTask).getNome());    
}