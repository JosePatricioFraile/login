 public static void main(String[] args) {
        // TODO code application logic here
      Scanner sc = new Scanner(System.in);
        var usuario = "";
        var contraseña = "";
        int contador = 0;
        System.out.println("Usuario");
        usuario = sc.nextLine();
        System.out.println("Contraseña");
        contraseña = sc.nextLine();
        
        while(contador < 2){
            if(!login(usuario, contraseña)){
                System.out.println("Datos erroneos");
                 System.out.println("Usuario");
                usuario = sc.nextLine();
                System.out.println("Contraseña");
                contraseña = sc.nextLine();
                contador++;
            }else if(login(usuario, contraseña)){
                contador = 3;
            }
        }
        if(login(usuario, contraseña)){
            System.out.println("Bienvenido");
        }else{
            System.out.println("Se ha agotado el número de intentos");
        }
    }
    
    static boolean login(String usuario, String contraseña){
        boolean comprobar = false;
        if(usuario.equals("usuario1") && contraseña.equals("asdfg")){
            comprobar = true;
        }
        return comprobar;
    }
}
