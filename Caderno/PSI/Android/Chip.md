==**Colocar esta linha no xml**==
android:checkable="true"

==**Declarar o chip**==
Chip chipDone;

==**Inicializar o objeto do tipo CHIP**==  
==**Criar uma instância da Classe Chip**==  
this.chipDone = v.findViewById(R.id.chipDone);  


==**Apanhar o valor atual do chip**==  
==**O chip guarda um boolean**==  
Boolean chipValue = this.chipDone.isChecked();

==**Ver o valor do chip que pode ser alterado**==
this.chipDone.setOnClickListener(v1 -> {  

  
    Boolean novoChipValue = this.chipDone.isChecked();  
  
    Toast.makeText(getContext(), "Agora o valor do chip é " + novoChipValue, Toast.LENGTH_SHORT)  
            .show();  
});

==/**==  
 ==***Método para controlar o que o user vê quando o estado do chip é alterado**==  
 ==*/==  
private void changeChipDisplay() {  
    Boolean estadoDoChip = this.chipDone.isChecked();  
  
    String textoDoChip = "Por finalizar";  
    if(estadoDoChip) {  
        textoDoChip = "Finalizada";  
        chipDone.setChipIconResource(R.drawable.image_round_bg);  
    } else {  
        chipDone.setChipIconResource(R.drawable.icon);  
    }  
  
    this.chipDone.setText(textoDoChip);  
}