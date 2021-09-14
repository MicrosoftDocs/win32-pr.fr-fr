---
title: Tableaux multidimensionnels
description: Les attributs de tableau peuvent également être utilisés avec des tableaux multidimensionnels.
ms.assetid: a01b904c-fbe8-4af4-8393-6864f7ef7364
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb7bcf94d97e1f35fdd6ab432ea5869e47f79ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119041"
---
# <a name="multidimensional-arrays"></a>Tableaux multidimensionnels

Les attributs de tableau peuvent également être utilisés avec des tableaux multidimensionnels. Toutefois, veillez à ce que chaque dimension du tableau ait un attribut correspondant. Par exemple :

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface multiarray
{
  void arr2d( [in] short        d1size,
              [in] short        d2len,
              [in, size_is( d1size, ), length_is ( , d2len) ] long array2d[*][30] ) ;
}
```

Le tableau précédent est un tableau conforme (de taille d1size) de 30 tableaux d’éléments (avec les éléments d2len fournis pour chaque). La virgule entre les parenthèses de la \[ [**taille \_ est**](/windows/desktop/Midl/size-is) l' \] attribut spécifie que la valeur de d1size est appliquée à la première dimension du tableau. De même, la commande entre les parenthèses de la \[ [**longueur \_ est**](/windows/desktop/Midl/length-is) \] attribute indique que la valeur de d2len est appliquée à la deuxième dimension du tableau.

Le compilateur MIDL 2,0 fournit deux méthodes pour marshaler des paramètres : mode mixte (/OS) et entièrement interprété (**/de l'** environnement **d’exploitation** ou/**Oicf**). Par défaut, le compilateur MIDL compile les interfaces en mode mixte. Vous n’avez pas besoin de spécifier explicitement le commutateur [**/OS**](/windows/desktop/Midl/-os) pour accéder au marshaling en mode mixte.

La méthode entièrement interprétée marshale les données complètement hors connexion. Cela réduit considérablement la taille du code stub, mais entraîne également une baisse des performances. Dans le marshaling en mode mixte, les stubs marshalent certains paramètres en ligne. Bien que cela entraîne une plus grande taille de stub, elle offre également des performances accrues.

> [!Caution]  
> Soyez prudent lors de la compilation des fichiers IDL dans ce mode. L’utilisation de tableaux multidimensionnels en mode mixte peut entraîner des paramètres qui ne sont pas correctement marshalés. Le commutateur de ligne de commande [**/Oicf**](/windows/desktop/Midl/-oi) est recommandé quand votre interface définit des paramètres qui sont des tableaux multidimensionnels.

 

L' \[ [](/windows/desktop/Midl/string) \] attribut de chaîne peut également être utilisé avec des tableaux multidimensionnels. L’attribut s’applique à la dimension la moins significative, telle qu’un tableau de chaînes conforme. Vous pouvez également utiliser des attributs de pointeur multidimensionnel. Par exemple :

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface multiarray
{
  void arr2d([in] short  d1len,
             [in] short  d2len,
             [in] size_is(d1len, d2len) ] long  ** ptr2d) ;
}
```

Dans l’exemple précédent, la variable ptr2d est un pointeur vers un bloc de pointeurs d1len, dont chacun pointe vers des pointeurs d2len vers **long**.

Les tableaux multidimensionnels ne sont pas équivalents aux tableaux de pointeurs. Un tableau multidimensionnel est un bloc de données unique et volumineux en mémoire. Un tableau de pointeurs contient uniquement un bloc de pointeurs dans le tableau. Les données vers lesquelles pointent les pointeurs peuvent se trouver n’importe où dans la mémoire. En outre, la syntaxe C ANSI permet de ne pas spécifier la dimension de tableau la plus significative (la plus à gauche) dans un tableau multidimensionnel. Par conséquent, voici une instruction valide :

`long a1[] [20]`

Comparez ceci à l’instruction non valide suivante :

`long a1[20] []`

 

 