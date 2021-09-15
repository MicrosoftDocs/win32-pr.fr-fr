---
title: Attribut size_is
description: L’attribut \ size \_ is \ est associé à une constante entière, une expression ou une variable qui spécifie la taille d’allocation du tableau.
ms.assetid: 5252c1a2-8e07-4e28-8280-6a9563d1b291
keywords:
- size_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7159c68d6bc3c1485c14db20d97c488916cb7b22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311401"
---
# <a name="the-size_is-attribute"></a>La \[ taille \_ est un \] attribut

La \[ [taille \_ est](/windows/desktop/Midl/size-is) \] un attribut associé à une constante entière, une expression ou une variable qui spécifie la taille d’allocation du tableau. Prenons l’exemple d’un tableau de caractères dont la longueur est déterminée par l’entrée utilisateur :

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface arraytest
{
  void fArray2([in] short sSize,
               [in, out, size_is(sSize)] char achArray[*]);
}
```

> [!Note]  
> L’astérisque ( \* ) qui marque l’espace réservé pour la dimension variable-tableau est facultatif.

 

Le stub serveur doit allouer de la mémoire sur le serveur qui correspond à la mémoire sur le client pour ce paramètre. La variable qui spécifie la taille doit toujours être au moins un \[ [](/windows/desktop/Midl/in) \] paramètre in. L' **attribut directionnel est requis pour que la valeur taille soit définie à l’entrée sur le stub serveur. \[ \]** Cette valeur de taille fournit les informations dont le stub serveur a besoin pour allouer la mémoire.

Le paramètre de taille peut également être \[ in, [out](/windows/desktop/Midl/out-idl) \] . Cela est utile si, par exemple, le tableau envoyé par le client n’est pas suffisamment grand pour les données que le serveur doit stocker dans celui-ci. Vous pouvez utiliser un paramètre **\[ in, \] out** size pour renvoyer la taille requise au programme client.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Plusieurs niveaux de pointeurs](multiple-levels-of-pointers.md)
</dt> </dl>

 

 