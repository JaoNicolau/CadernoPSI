==Declarar variáveis:==
EditText editNome;  
EditText editDescricao;

==ir busca-las ao xml:==
this.editNome = v.findViewById(R.id.editNome);  
this.editDescricao = v.findViewById(R.id.editDescricao);

==guarda o valor numa variável :==
String nome = this.editNome.getText().toString();  
String descricao = this.editDescricao.getText().toString();

==mostra o resultado da variável:==
result.putString("nomeDaTarefa", nome);  
result.putString("descricaoDaTarefa", descricao);