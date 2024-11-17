# C 01

This set of exercises focuses on fundamental pointer and array manipulation concepts in C, aiming to strengthen students' understanding of pointer operations. Each task requires implementing a function without using external functions, except for the write function in the string display exercise. The exercises cover tasks such as assigning values to integers via pointers, swapping values between integers using pointers, performing mathematical operations (division and modulus) with results stored in pointers, handling strings including displaying and counting characters, and reversing and sorting integer arrays. Students are required to submit their code files as per the specifications of each exercise.

This project covers the topic of module C 01 from the 42 C Piscine, a series of programming exercises in C. It includes general instructions, an introduction to the subject, and a set of tasks focused on pointer and array manipulation.

- **`ft_ft`** - Takes a pointer to an int as a parameter and assigns the value 42 to the pointed int.
- **`ft_ultimate_ft`** - Takes a pointer to multiple pointers (int), and assigns the value 42 to the pointed int.
- **`ft_swap`** - Takes two pointers to int and swaps the values of the two integers.
- **`ft_div_mod`** - Takes two integer values (a and b) and two pointers to int (div and mod). It divides a by b, storing the quotient in div and the remainder in mod.
- **`ft_ultimate_div_mod`** - Takes two pointers to int (a and b). It divides the value of a by that of b, storing the quotient in a and the remainder in b.
- **`ft_putstr`** - Takes a pointer to a char (string) and displays the string to standard output.
- **`ft_strlen`** - Takes a pointer to a char (string) and returns the number of characters in the string.
- **`ft_rev_int_tab`** - Takes a pointer to an int and the size of an array, and reverses the order of the elements in the array.
- **`ft_sort_int_tab`** - Takes a pointer to an int and the size of an array, and sorts the array in ascending order.
<details>
	<summary>Exercises:</summary>

- [ex00:](https://github.com/vinislima/42sp_piscine_c01/tree/main/ex00)
    
    ```c
    /* ************************************************************************** */
    /*                                                                            */
    /*                                                        :::      ::::::::   */
    /*   ft_ft.c                                            :+:      :+:    :+:   */
    /*                                                    +:+ +:+         +:+     */
    /*   By: vinda-si <vinda-si@student.42.fr>          +#+  +:+       +#+        */
    /*                                                +#+#+#+#+#+   +#+           */
    /*   Created: 2024/08/19 16:45:47 by vinda-si          #+#    #+#             */
    /*   Updated: 2024/08/20 18:17:06 by vinda-si         ###   ########.fr       */
    /*                                                                            */
    /* ************************************************************************** */
    
    // nessa lista temos o primeiro contato
    // com ponteiros, onde armazenamos o referência
    // de objetos, como variáveis
    // neste caso um ponteiro do tipo inteiro
    void	ft_ft(int *nbr);
    
    void	ft_ft(int *nbr)
    {
    	// aqui estamos armanezando no ponteiro um valor
    	*nbr = 42;
    }
    
    // // início da main
    // #include <unistd.h>
    // #include <stdio.h>
    
    // void	ft_ft(int *nbr);
    
    // int	main(void)
    // {
    // 	// declaramos uma variável do tipo inteiro
    // 	int	a;
    // 	// aqui atribuimos um valor à ela
    // 	a = 20;
    // 	// usamos um printf, para mostrar o valor inicialmente
    // 	// armazenado nela, neste caso vinte
    // 	printf("Antes: %d\n", a);
    // 	// chamando a função, passamos o endereço de memória
    // 	// da variável, que ira apontar para o valor armazenado nela
    // 	ft_ft(&a);
    // 	// desta forma ao imprimir novamente a várivel teremos do valor
    // 	// do ponteiro da função, quarenta e dois
    // 	printf("Depois: %d", a);
    // 	return (0);
    // }
    ```
    
- [ex01:](https://github.com/vinislima/42sp_piscine_c01/tree/main/ex01)
    
    ```c
    /* ************************************************************************** */
    /*                                                                            */
    /*                                                        :::      ::::::::   */
    /*   ft_ultimate_ft.c                                   :+:      :+:    :+:   */
    /*                                                    +:+ +:+         +:+     */
    /*   By: vinda-si <vinda-si@student.42.fr>          +#+  +:+       +#+        */
    /*                                                +#+#+#+#+#+   +#+           */
    /*   Created: 2024/08/19 19:05:09 by vinda-si          #+#    #+#             */
    /*   Updated: 2024/08/20 16:52:15 by vinda-si         ###   ########.fr       */
    /*                                                                            */
    /* ************************************************************************** */
    
    // nesta função somos aprentados para o conceito
    // de níveis de ponteiros, onde um ponteiro, aponta
    // para outro ponteiro. Neste caso, como exemplo
    // trabalharemos com um ponteiro de nove níveis
    void	ft_ultimate_ft(int *********nbr);
    
    void	ft_ultimate_ft(int *********nbr)
    {
    	// esse ponteiro recebe o valor de quanrenta e dois
    	*********nbr = 42;
    }
    
    // // inicio da main
    // #include <stdio.h>
    // #include <unistd.h>
    
    // void ft_ultimate_ft(int *********nbr);
    
    // int main()
    // {
    // 	// como precisamos de um ponteiro de nove níveis
    // 	// criamos um variável sem atribuir valor
    // 	// e vamos criando ponteiro e passamos o endeço
    // 	// de mémoria dessa variável para um ponteiro
    // 	// e vamos nessa sequência até alcançar nove níveis
    // 	int number;
    // 	int *ptr1 = &number;
    // 	int **ptr2 = &ptr1;
    // 	int ***ptr3 = &ptr2;
    // 	int ****ptr4 = &ptr3;
    // 	int *****ptr5 = &ptr4;
    // 	int ******ptr6 = &ptr5;
    // 	int *******ptr7 = &ptr6;
    // 	int ********ptr8 = &ptr7;
    // 	int *********ptr9 = &ptr8;
    // 	// testamos a impressão da variável antes de
    // 	// chamar a função
    // 	printf("%i\n",number);
    // 	// chamamos a função e passamos o ultimo ponteiro
    // 	ft_ultimate_ft(ptr9);
    // 	// imprimimos a variável inicial novamente que
    // 	// desta vez ira imprimir o conteúdo do ponteiro da função
    // 	printf("%i",number);
    // }
    ```
    
- [ex02:](https://github.com/vinislima/42sp_piscine_c01/tree/main/ex02)
    
    ```c
    /* ************************************************************************** */
    /*                                                                            */
    /*                                                        :::      ::::::::   */
    /*   ft_swap.c                                          :+:      :+:    :+:   */
    /*                                                    +:+ +:+         +:+     */
    /*   By: vinda-si <vinda-si@student.42.fr>          +#+  +:+       +#+        */
    /*                                                +#+#+#+#+#+   +#+           */
    /*   Created: 2024/08/20 11:58:34 by vinda-si          #+#    #+#             */
    /*   Updated: 2024/08/20 16:53:35 by vinda-si         ###   ########.fr       */
    /*                                                                            */
    /* ************************************************************************** */
    
    // aqui vamos ter contato com o conceito de manipulação
    // de ponteiros, onde iremos trocar o conteúdo deles
    void	ft_swap(int *a, int *b);
    // a função recebe dois ponteiros do tipo inteiro
    void	ft_swap(int *a, int *b)
    {
    	// para a manipulação iremos declarar uma variável
    	// que armazenará momentaneamente o valor de um deles
    	int	change;
    	// aqui ela armazena o valor do ponteiro a
    	change = *a;
    	// desta forma podemos armazenar no ponteiro a
    	// o valor do ponteiro b
    	*a = *b;
    	// e finalmente no ponteiro b, podemos armazenar
    	// em b o valor de a, que estava armanezado na
    	// variável change
    	*b = change;
    }
    
    // // iniciamos o main aqui
    // #include <unistd.h>
    // #include <stdio.h>
    
    // void	ft_swap(int *a, int *b);
    
    // int	main()
    // {
    // 	// declaramos e atribuimos valores
    // 	// as variaveis 
    // 	int a = 10;
    // 	int b = 40;
    // 	// testamos para verificar os valores
    // 	// armazenados nas variáveis
    // 	printf("a = %i, b = %i\n", a, b);
    // 	// chamamos a função que ira realizar a troca
    // 	// para isso passamos os endereços de mémoria
    // 	ft_swap(&a, &b);
    // 	// imprimindo novamente vemos que a troca ocorreu
    // 	printf("a = %i, b = %i", a, b);
    // 	return(0);
    // }
    ```
    
- [ex03:](https://github.com/vinislima/42sp_piscine_c01/tree/main/ex03)
    
    ```c
    
    /* ************************************************************************** */
    /*                                                                            */
    /*                                                        :::      ::::::::   */
    /*   ft_div_mod.c                                       :+:      :+:    :+:   */
    /*                                                    +:+ +:+         +:+     */
    /*   By: vinda-si <vinda-si@student.42.fr>          +#+  +:+       +#+        */
    /*                                                +#+#+#+#+#+   +#+           */
    /*   Created: 2024/08/20 15:46:19 by vinda-si          #+#    #+#             */
    /*   Updated: 2024/08/21 17:59:22 by vinda-si         ###   ########.fr       */
    /*                                                                            */
    /* ************************************************************************** */
    
    void	ft_div_mod(int a, int b, int *div, int *mod);
    // aqui vamos testar como armazenar valores em ponteiros
    // utilizando valores recebidos para realizar operações matemáticas
    void	ft_div_mod(int a, int b, int *div, int *mod)
    {
    	// o ponteiro div deve conter o resultado da divisão
    	// entre os inteiros a e b
    	*div = a / b;
    	// o ponteiro mod recebe a operação de módulo entre a e b
    	*mod = a % b;
    }
    
    // // inicio da main
    // #include <stdio.h>
    
    // void	ft_div_mod(int a, int b, int *div, int *mod);
    
    // int	main()
    // {
    // 	// declaramos quatro variáveis
    // 	// onde vamos atribuir valores a duas
    // 	// e as outras duas iremos utilizar seus endereços
    // 	// para receber os resultados das operações realizadas na função
    // 	int a, b, div, mod;
    // 	// atribuimos valore à a e b
    // 	a = 20;
    // 	b = 5;
    // 	// passamos as variáveis e endereços para a função
    // 	ft_div_mod(a, b, &div, &mod);
    // 	// aqui imprimimos os valores armazenados nas variáveis
    // 	// que antes não tinham valores atribuidos
    // 	printf("div: %d, mod: %d", div, mod);
    // 	return(0);
    // }
    
    ```
    
- [ex04:](https://github.com/vinislima/42sp_piscine_c01/tree/main/ex04)
    
    ```c
    /* ************************************************************************** */
    /*                                                                            */
    /*                                                        :::      ::::::::   */
    /*   ft_ultimate_div_mod.c                              :+:      :+:    :+:   */
    /*                                                    +:+ +:+         +:+     */
    /*   By: vinda-si <vinda-si@student.42.fr>          +#+  +:+       +#+        */
    /*                                                +#+#+#+#+#+   +#+           */
    /*   Created: 2024/08/20 18:44:55 by vinda-si          #+#    #+#             */
    /*   Updated: 2024/08/20 19:52:39 by vinda-si         ###   ########.fr       */
    /*                                                                            */
    /* ************************************************************************** */
    
    void	ft_ultimate_div_mod(int *a, int *b);
    // aqui o objetivo é manipular a informação no ponteiro
    // de tal forma que com a função, os ponteiros recebam
    // os valores e com neles mesmo façamos a alteração de memória
    // armazenando os resultados
    void	ft_ultimate_div_mod(int *a, int *b)
    {
    	// declaramos duas variáveis para momentaneamente
    	// armazene os valores dos cálculos
    	int	div;
    	int	mod;
    	// div recebe o valor da divisão dos valores entre a e b
    	div = *a / *b;
    	// mod recebe o valor do módulo dos valores entre a e b
    	mod = *a % *b;
    	// aqui ponteiro recebe o valor de div
    	*a = div;
    	// aqui o ponteiro recebe o valor de mod
    	*b = mod;
    }
    
    // // início da main
    // #include <unistd.h>
    // #include <stdio.h>
    
    // void	ft_ultimate_div_mod(int *a, int *b);
    
    // int	main()
    // {
    // 	// declaramos e atribuímos valores as variáveis
    // 	int a = 40;
    // 	int b = 10;
    // 	// imprimimos para verificar os valores armazenados
    // 	printf("a = %i, b = %i\n", a, b);
    // 	// chamamos a função e passamos os endereços de memórias das variáveis
    // 	ft_ultimate_div_mod(&a, &b);
    // 	// imprimimos novamente os valores das variáveis, que agora contém
    // 	// os valores dos cálculos realizados na função
    // 	printf("a = %i, b = %i", a, b);
    // 	return(0);
    // }
    ```
    
- [ex05:](https://github.com/vinislima/42sp_piscine_c01/tree/main/ex05)
    
    ```c
    /* ************************************************************************** */
    /*                                                                            */
    /*                                                        :::      ::::::::   */
    /*   ft_putstr.c                                        :+:      :+:    :+:   */
    /*                                                    +:+ +:+         +:+     */
    /*   By: vinda-si <vinda-si@student.42.fr>          +#+  +:+       +#+        */
    /*                                                +#+#+#+#+#+   +#+           */
    /*   Created: 2024/08/21 10:50:07 by vinda-si          #+#    #+#             */
    /*   Updated: 2024/08/21 11:37:27 by vinda-si         ###   ########.fr       */
    /*                                                                            */
    /* ************************************************************************** */
    
    #include <unistd.h>
    // aqui vamos imprimir strings
    // o ponteiro recebido aponta para o início da string
    void	ft_putstr(char *str);
    
    void	ft_putstr(char *str)
    {
    	// declaramos uma variável que servirá de contador
    	// no laço de repetição
    	int	i;
    	// atribuímos o valor inicial a variável
    	i = 0;
    	// esse laço se repetirá enquanto o elemento
    	// da string for diferente de nulo
    	// o contador irá proporcionar que seja possível
    	// percorrer a string
    	while (str[i] != '\0')
    	{
    		// utilizando a função write, será impresso
    		// cada elemento da string, até que seja atingido
    		// o elemento nulo
    		write(1, &str[i], 1);
    		i++;
    	}
    }
    
    // // início da main
    // void	ft_putstr(char *str);
    
    // int main(void)
    // {
    // 	// chamamos a função e passamos a string
    // 	ft_putstr("teste");
    // 	return(0);
    // }
    ```
    
- [ex06:](https://github.com/vinislima/42sp_piscine_c01/tree/main/ex06)
    
    ```c
    /* ************************************************************************** */
    /*                                                                            */
    /*                                                        :::      ::::::::   */
    /*   ft_strlen.c                                        :+:      :+:    :+:   */
    /*                                                    +:+ +:+         +:+     */
    /*   By: vinda-si <vinda-si@student.42.fr>          +#+  +:+       +#+        */
    /*                                                +#+#+#+#+#+   +#+           */
    /*   Created: 2024/08/21 11:59:11 by vinda-si          #+#    #+#             */
    /*   Updated: 2024/08/21 16:01:42 by vinda-si         ###   ########.fr       */
    /*                                                                            */
    /* ************************************************************************** */
    
    // essa função recebe um ponteiro
    // para o início de uma string
    // e retornará o comprimento dela
    int	ft_strlen(char *str);
    
    int	ft_strlen(char *str)
    {
    	int	i;
    	// novamente usaremos um laço de repetição
    	// utilizando um contador para percorrer
    	// a string e conseguir saber seu comprimento
    	i = 0;
    	// enquanto o elemento acessado na string
    	// não for igual a nulo, permanecemos dentro
    	// do laço e o contador é incrementado
    	while (str[i] != '\0')
    	{
    		i++;
    	}
    	// após a condição ser atendida, saímos do laço
    	// e retornamos o valor do contador, que neste caso
    	// será o comprimento da string
    	return (i);
    }
    
    // // início da main
    // #include <stdio.h>
    
    // int	ft_strlen(char *str);
    
    // int main(void)
    // {
    // 	// como o retorno da função é um inteiro
    // 	// declaramos uma variável desse tipo
    // 	// para receber o valor
    // 	int i;
    // 	// na atribuição colocamos a função
    // 	// que retornará o valor
    // 	i = ft_strlen("teste");
    // 	// iremos imprimir o valor recebido
    // 	printf("%d",i);
    // 	return(0);
    // }
    ```
    
- [ex07:](https://github.com/vinislima/42sp_piscine_c01/tree/main/ex07)
    
    ```c
    /* ************************************************************************** */
    /*                                                                            */
    /*                                                        :::      ::::::::   */
    /*   ft_rev_int_tab.c                                   :+:      :+:    :+:   */
    /*                                                    +:+ +:+         +:+     */
    /*   By: vinda-si <vinda-si@student.42.fr>          +#+  +:+       +#+        */
    /*                                                +#+#+#+#+#+   +#+           */
    /*   Created: 2024/08/21 16:12:49 by vinda-si          #+#    #+#             */
    /*   Updated: 2024/08/22 10:57:43 by vinda-si         ###   ########.fr       */
    /*                                                                            */
    /* ************************************************************************** */
    
    // nessa função iremos receber um ponteiro para
    // que aponta pra início de array de inteiros
    // e outro com a quantidade de elementos no array,
    // e será realizada a inversão dos elementos dela
    void	ft_rev_int_tab(int *tab, int size);
    
    void	ft_rev_int_tab(int *tab, int size)
    {
    	// declaramos três variáveis, uma para realizar o
    	// armazenamento temporário da troca, outras duas
    	// que serão contadores
    	int	change;
    	int	count_first;
    	int	count_end;
    	// atribuimos o valor de zero para o primeiro
    	// contador, para interagirmos com o primeiro
    	// elemento do array
    	count_first = 0;
    	// o segundo contador será utilizado para interagir
    	// com o último elemento do array, será usado o menos
    	// um pois no array porque a contagem se inícia em zero
    	// e desta forma não iremos ultrapassar o limite do array
    	count_end = size - 1;
    	// enquanto primeiro contador for menor do que
    	// o contador do final da string ficaremos dentro do
    	// laço de repetição
    	while (count_first < count_end)
    	{
    		// atribuimos a variável de armazenamento de troca o valor
    		// do primeiro item do array
    		change = tab[count_first];
    		// agora podemos atribuir a primeira posição o valor da última posição
    		tab[count_first] = tab[count_end];
    		// e o último elemento recebe o valor do primeiro que estava armazenado
    		// na variável de troca
    		tab[count_end] = change;
    		// incrementando a variável do início para acessar o elemento seguinte
    		count_first++;
    		// decrementamos a variável do fim para acessar o elemento antterior
    		count_end--;
    	}
    	// ficaremos nesse looping até a condição ser falsa, nesse momento as variáveis
    	// já estarão trocadas e ambas estarão no meio do array
    }
    
    // // início da main
    // #include <stdio.h>
    // #include <unistd.h>
    
    // void	ft_rev_int_tab(int *tab, int size);
    
    // int	main(void)
    // {	
    // 	// declaramos duas variáveis, uma para a quantidade de elementos
    // 	// outra para o index do array
    // 	int size = 5;
    // 	int index = 0;
    // 	// aqui declaramos e atribuímos elementos para o array
    // 	int array[] = {1, 2, 3, 4, 5};
    // 	// o laço de repetição percorrerá enquanto o index
    // 	// for menor que a quantidade de elementos dele
    // 	// realizamos a primeira impressão para verificar a ordem
    // 	while(index < size)
    // 	{
    // 		printf("%i,",array[index]);
    // 		index++;
    // 	}
    // 	// chamamos a função e passamos o array e o a quantidade elementos
    // 	ft_rev_int_tab(array, size);
    // 	// fazemos novamente um laço para passar pelo array e confirmar
    // 	// que a inversão ocorreu
    // 	index = 0;
    // 	while(index < size)
    // 	{
    // 		printf("%i,",array[index]);
    // 		index++;
    // 	}
    // }
    ```
    
- [ex08:](https://github.com/vinislima/42sp_piscine_c01/tree/main/ex08)
    
    ```c
    /* ************************************************************************** */
    /*                                                                            */
    /*                                                        :::      ::::::::   */
    /*   ft_sort_int_tab.c                                  :+:      :+:    :+:   */
    /*                                                    +:+ +:+         +:+     */
    /*   By: vinda-si <vinda-si@student.42.fr>          +#+  +:+       +#+        */
    /*                                                +#+#+#+#+#+   +#+           */
    /*   Created: 2024/08/22 11:12:28 by vinda-si          #+#    #+#             */
    /*   Updated: 2024/08/22 19:29:05 by vinda-si         ###   ########.fr       */
    /*                                                                            */
    /* ************************************************************************** */
    
    // nessa função vamos ser apresentados ao conceito
    // de métodos de ordenação, neste caso específico
    // o bubble sort.
    // aqui a função recebe dois inteiros, um ponteiro para
    // o início da array e um com a quantidade de elementos
    void	ft_sort_int_tab(int *tab, int size);
    
    void	ft_sort_int_tab(int *tab, int size)
    {
    	// declaramos três variáveis, duas de index
    	// e outra para comportar os elementos durante
    	// a mudança de posição
    	int	count_a;
    	int	count_b;
    	int	change;
    	// o laço de repitação será inicado no primeiro elemento
    	// do array e seguira sendo executado enquanto o contador
    	// for menor que o tamanho, novamente subtraindo um para
    	// evitar ultrapassar o tamanho do array
    	// dessa maneira que foi implementado, iremos repetir a
    	// verificação de valores, em todos os elementos da array
    	count_a = 0;
    	while (count_a < size - 1)
    	{
    		count_b = 0;
    		// esse laço irá se repetir enquanto o segundo contador
    		// for menor que a quantidade de elementos do array,
    		// subtraído da quantidade de elementos já interados,
    		// porque a cada interação o maior número passa a ocupar
    		// a última posição, então não devemos mais acessa-lo.
    		// excluindo novamente o ultimo elemento para
    		// não ultrapassar o tamanho do array
    		while (count_b < size - count_a - 1)
    		{
    			// aqui é testado se o elemento é maior que o próximo
    			// em caso de ser verdadeiro, entramos na condição
    			if (tab[count_b] > tab[count_b + 1])
    			{
    				// entrando na condição vamos realizar
    				//a troca de posições entre eles
    				change = tab[count_b];
    				tab[count_b] = tab[count_b + 1];
    				tab[count_b + 1] = change;
    			}
    			count_b++;
    		}
    		count_a++;
    		// iremos realizar esse teste até o final passando
    		// pelo array em uma quantidade de vezes igual ao seu tamanho
    	}
    }
    
    // // início da main
    // #include <stdio.h>
    // #include <unistd.h>
    
    // void	ft_sort_int_tab(int *tab, int size);
    
    // int	main(void)
    // {
    // 	// declaramos duas variáveis, uma para a quantidade de elementos
    // 	// outra para o index do array
    // 	int size = 6;
    // 	int index = 0;
    // 		// aqui declaramos e atribuímos elementos para o array
    // 	int array[] = {212, 13, 40, 5, 19, 0};
    // 	// o laço de repetição percorrerá enquanto o index
    // 	// for menor que a quantidade de elementos dele
    // 	// realizamos a primeira impressão para verificar a ordem
    // 	while(index < size)
    // 	{
    // 		printf("%i,",array[index]);
    // 		index++;
    // 	}
    // 	printf("\n");
    // 	// chamamos a função e passamos o array e o a quantidade elementos
    // 	ft_sort_int_tab(array, size);
    // 	// fazemos novamente um laço para passar pelo array e confirmar
    // 	// que a inversão ocorreu
    // 	index = 0;
    // 	while(index < size)
    // 	{
    // 		printf("%i,",array[index]);
    // 		index++;
    // 	}
    // }
    ```
</details>