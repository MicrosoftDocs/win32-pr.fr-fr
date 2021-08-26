---
title: Attributs de tableau
description: Il existe une relation étroite entre les tableaux et les pointeurs dans le langage C.
ms.assetid: 0d65c993-63e4-42ae-ae24-6c19a71386a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba7bdaa08352a96987066313d4db074872f28b71ec0be0856a32522a849029c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073519"
---
# <a name="array-attributes"></a>Attributs de tableau

Il existe une relation étroite entre les tableaux et les pointeurs dans le langage C. Lorsqu’il est passé en tant que paramètre à une fonction, un nom de tableau est traité comme un pointeur vers le premier élément du tableau, comme indiqué dans l’exemple suivant :


```C++
/* fragment */
extern void f1(char * p1);

void main(void)
{
    char chArray[MAXSIZE];

    fLocal1(chArray);
}
```



Dans un appel local, vous pouvez utiliser le paramètre de pointeur à mars par le biais de la mémoire et examiner le contenu d’autres adresses :


```C++
/* dump memory (fragment) */
void fLocal1(char * pch1)
{
    int i;

    for (i = 0; i < MAXSIZE; i++)
       printf("%c ", *pch1++);
}
```



Lorsqu’un client passe un pointeur vers une procédure distante, le stub client transmet à la fois le pointeur et les données vers lesquelles il pointe. À moins que le pointeur ne soit limité à ses données correspondantes, toute la mémoire du client doit être transmise avec chaque appel distant. En appliquant le typage fort dans la définition de l’interface, MIDL limite le traitement du stub client aux données qui correspondent au pointeur spécifié.

La taille du tableau et la plage d’éléments de tableau transmis à l’ordinateur distant peuvent être des constantes ou des variables. Lorsque ces valeurs sont variables et, par conséquent, déterminées au moment de l’exécution, vous devez utiliser des attributs dans le fichier IDL pour spécifier le nombre d’éléments de tableau à transmettre. Les attributs MIDL suivants prennent en charge les limites de tableau.



| Attribut                             | Description                                             | Default |
|---------------------------------------|---------------------------------------------------------|---------|
| \[[ **tout \_ d’abord** ,](/windows/desktop/Midl/first-is)\]   | Index du premier élément de tableau transmis.           | 0       |
| \[la [ **dernière \_ est**](/windows/desktop/Midl/last-is)\]     | Index du dernier élément de tableau transmis.            | \-      |
| \[la [ **longueur \_ est**](/windows/desktop/Midl/length-is)\] | Nombre total d’éléments de tableau transmis.             | \-      |
| \[le [ **nombre maximal \_ est**](/windows/desktop/Midl/max-is)\]       | Valeur d’index de tableau valide la plus élevée.                        | \-      |
| \[[ **Min \_ est**](/windows/desktop/Midl/min-is)\]       | Valeur d’index de tableau valide la plus basse.                         | 0       |
| \[la [ **taille \_ est**](/windows/desktop/Midl/size-is)\]     | Nombre total d’éléments de tableau alloués pour le tableau. | \-      |



 

> [!Note]  
> L’attribut **Min \_ is** n’est pas implémenté dans RPC. L’index de tableau minimal est toujours traité comme zéro.

 

 

 