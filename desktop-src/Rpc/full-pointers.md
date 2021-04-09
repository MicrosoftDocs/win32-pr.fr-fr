---
title: Pointeurs complets
description: Contrairement aux pointeurs uniques, les pointeurs complets prennent en charge l’alias.
ms.assetid: 38023942-a4c2-4de7-b7d5-10d508cf083b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18687b496ddd28dca9e70afca8deafb18774500a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941095"
---
# <a name="full-pointers"></a>Pointeurs complets

Contrairement aux pointeurs [uniques](unique-pointers.md) , les pointeurs complets prennent en charge l’alias. Cela signifie que plusieurs pointeurs peuvent faire référence aux mêmes données, comme illustré dans la figure suivante :

![deux pointeurs référençant les mêmes données](images/prog-a02.png)

Un pointeur complet présente les caractéristiques suivantes :

-   Elle peut avoir la valeur null.
-   Elle peut passer de null à non null pendant l’appel. Lorsque la valeur devient non null, le stub client alloue la nouvelle mémoire allouée lors du retour. Le programme client doit libérer cette mémoire avant qu’elle ne se termine.
-   Elle peut passer d’une valeur non null à une valeur null pendant l’appel. Lorsque la valeur est remplacée par null, l’application est responsable de la libération de la mémoire.
-   La valeur peut passer d’une valeur non null à une autre.
-   Le stockage vers lequel pointe un pointeur complet est accessible par un autre pointeur ou nom dans l’opération.
-   Les données de retour sont écrites dans le stockage existant si le pointeur n’a pas la valeur null.

Utilisez l' \[ attribut [**ptr**](/windows/desktop/Midl/ptr) \] pour spécifier un pointeur complet, comme illustré dans l’exemple suivant :

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface FullPtrInterface
{
  void RemoteFn([in,ptr,string]) char *ptrName1,
                [in,ptr,string]  char *ptrName2);
}
```

Dans cet exemple, les paramètres *ptrName1* et *ptrName2* sont définis comme des pointeurs complets vers une chaîne. Il est possible que les deux pointeurs pointent vers la même adresse mémoire contenant une seule chaîne.

\[**pointeur** \] est requis pour fournir la prise en charge des alias. Toutefois, étant donné qu’elle nécessite le plus grand traitement de tous les pointeurs disponibles dans RPC, elle n’est pas recommandée pour la plupart des applications.

 

 