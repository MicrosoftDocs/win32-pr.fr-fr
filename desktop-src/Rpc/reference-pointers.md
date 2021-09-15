---
title: Pointeurs de référence
description: Les pointeurs de référence sont les pointeurs les plus simples et nécessitent le moins de traitement par le stub client.
ms.assetid: 393aec84-8e8f-41b9-956f-d28a80d3a8c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 427605f330b1a73c541c95019f8ca4bdd6cc8ef4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311446"
---
# <a name="reference-pointers"></a>Pointeurs de référence

Les pointeurs de référence sont les pointeurs les plus simples et nécessitent le moins de traitement par le stub client. Lorsqu’un programme client passe un pointeur de référence à une procédure distante, le pointeur de référence contient toujours l’adresse d’un bloc de mémoire valide. Elle pointe toujours vers le même bloc de mémoire lorsque la procédure distante se termine. Ces pointeurs sont principalement utilisés pour implémenter la sémantique de référence et pour autoriser les \[ paramètres [**out**](/windows/desktop/Midl/out-idl) \] en C.

Dans l’exemple suivant, la valeur du pointeur ne change pas pendant l’appel, bien que le contenu des données à l’adresse indiquée par le pointeur puisse changer.

![modification des données à une adresse de pointeur de référence statique](images/prog-a07.png)

Un pointeur de référence présente les caractéristiques suivantes :

-   Il pointe toujours vers un stockage valide et n’a jamais la valeur **null**.
-   Il ne change jamais pendant un appel et pointe toujours vers le même stockage avant et après l’appel.
-   Les données retournées par la procédure distante sont écrites dans le stockage existant.
-   Le stockage désigné par un pointeur de référence n’est pas accessible par un autre pointeur ou tout autre nom dans la fonction.

Utilisez l' \[ [](/windows/desktop/Midl/ref) \] attribut ref pour spécifier des pointeurs de référence dans les définitions d’interface, comme indiqué dans l’exemple suivant.

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface RefPtrInterface
{
  void RemoteFn([in, out, ref] char *pChar);
}
```

Cet exemple définit le paramètre *pChar* comme un pointeur vers un caractère unique, et non un tableau de caractères. Il s’agit d’un paramètre de \[ **sortie** \] et d’un pointeur de référence qui pointe vers la mémoire que la routine de serveur RemoteFn remplira avec des données.

 

 