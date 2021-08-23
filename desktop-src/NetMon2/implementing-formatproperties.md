---
description: Moniteur réseau appelle la fonction FormatProperties pour mettre en forme les données affichées dans le volet d’informations de l’interface utilisateur Moniteur réseau.
ms.assetid: d0a58e1d-c867-4277-916e-f408627b5269
title: Implémentation de FormatProperties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50e7b927f15ccb2c216e345b37bc87593e33339671f906e28d33759ca9db0abc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778972"
---
# <a name="implementing-formatproperties"></a>Implémentation de FormatProperties

Moniteur réseau appelle la fonction [**FormatProperties**](formatproperties.md) pour mettre en forme les données affichées dans le volet d’informations de l’interface utilisateur Moniteur réseau. En règle générale, **FormatProperties** est appelé pour mettre en forme la ligne de résumé pour un protocole, puis pour mettre en forme toutes les instances de propriété du protocole dans un frame. Toutefois, Moniteur réseau n’identifie pas le nombre de fois où **FormatProperties** est appelé pour un analyseur spécifique.

Lors de l’appel de [**FormatProperties**](formatproperties.md), moniteur réseau fournit une structure [**PROPERTYINST**](propertyinst.md) pour chaque propriété qu’il affiche. La structure **PROPERTYINST** fournit des informations sur les données à afficher, y compris un pointeur vers la structure [**PROPERTYINFO**](propertyinfo.md) qui spécifie la fonction à utiliser pour mettre en forme la propriété de données affichée.

> [!Note]  
> Une structure [**PROPERTYINFO**](propertyinfo.md) est spécifiée lors de l’ajout d’une propriété à la [*base de données des propriétés*](p.md) de l’analyseur.

 

Moniteur réseau identifie la fonction de format à appeler pour chaque instance de propriété. Le membre **InstanceData** de la structure [**PROPERTYINFO**](propertyinfo.md) peut spécifier les éléments suivants :

-   Fonction [**FormatPropertyInstance**](formatpropertyinstance.md) pour utiliser le [*formateur générique*](g.md) fourni par Moniteur réseau.

    – ou –

-   Nom d’une fonction de format personnalisé fournie par l’analyseur.

Les fonctions [**FormatPropertyInstance**](formatpropertyinstance.md) et format personnalisé retournent les données mises en forme qui s’affichent dans le volet d’informations de l’interface utilisateur Moniteur réseau.

L’illustration suivante montre comment Moniteur réseau identifie la fonction à appeler pour chaque instance de propriété.

![Comment le moniteur réseau identifie la fonction à appeler](images/formatprop1.png)

La procédure suivante identifie les étapes nécessaires à l’implémentation de [**FormatProperties**](formatproperties.md).

**Pour implémenter FormatProperties**

-   À l’aide d’une structure de boucle, appelez la fonction format pour chaque structure [**PROPERTYINST**](propertyinst.md) transmise à l’analyseur dans le paramètre *lpPropInst* de la fonction [**FormatProperties**](formatproperties.md) .

Voici une implémentation de base de [**FormatProperties**](formatproperties.md).

``` syntax
#include <windows.h>

DWORD BHAPI MyProtocolFormatProperties( HFRAME hFrame,
                                        LPBYTE         pMacFrame,
                                        LPBYTE         pBLRPLATEFrame,
                                        DWORD          nPropertyInsts
                                        LPPROPERTYINST  p)
  {
    while( nPropertyInsts-- > 0)
      {
         ( (FORMAT) p->lpPropertyInfo->InstanceData) ) (p);
         p++;
      }
  return BHERR_SUCCESS;
  }
```

 

 



