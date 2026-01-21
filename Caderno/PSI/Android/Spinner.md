==**Declarar variáveis:**==
Spinner spinner;

==**Configurar o spinner**==  
Apanhar o spinner do layout  
this.spinner = v.findViewById(R.id.spinner);  

==**Construir o array para colocar dentro do spinner**==  
String[] exemplo = {"Lazer","Estudar","Limpar"};  

==**Criar o adapter para colocar a lista**==  
ArrayAdapter<String> adapter = new ArrayAdapter<>(  
        getContext(),  
        android.R.layout.simple_spinner_dropdown_item,  
        exemplo);  
        
==Passar o drop down para dentro do spinner==
this.spinner.setAdapter(adapter);