---
description: Moniteur réseau transmet toutes les trames d’une capture aux analyseurs, puis commence à appeler la fonction de désinscription pour tous les protocoles qu’elle identifie. Chaque DLL de l’analyseur doit implémenter une fonction de désinscription pour chaque protocole pris en charge par la DLL de l’analyseur.
ms.assetid: 936d5b00-b0ee-4a29-9396-1e2a7a91a2dd
title: Implémentation de l’annulation de l’inscription
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444502ba3ab19921a6372d4cda872aed85e879cbbdadc2f0176a7187bfc24491
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890479"
---
# <a name="implementing-deregister"></a>Implémentation de l’annulation de l’inscription

Moniteur réseau transmet toutes les trames d’une capture aux analyseurs, puis commence à appeler la fonction de [**désinscription**](deregister.md) pour tous les protocoles qu’elle identifie. Chaque DLL de l’analyseur doit implémenter une fonction de **désinscription** pour chaque protocole pris en charge par la dll de l’analyseur.

Chaque implémentation de la fonction de [**désinscription**](deregister.md) doit appeler la fonction [**DestroyProtocolDatabase**](destroypropertydatabase.md) pour libérer les ressources utilisées pour créer la base de données.

La procédure suivante identifie la seule étape nécessaire à l’implémentation de l’annulation de l' [**inscription**](deregister.md).

**Pour implémenter l’annulation de l’inscription pour un protocole**

-   Appelez [**DestroyProtocolDatabase**](destroypropertydatabase.md) pour libérer les ressources de la base de données.

Voici une implémentation de base de l' [**annulation**](deregister.md)de l’inscription. Notez que l’exemple de code montre la mise en sortie des ressources utilisées pour créer une base de données de propriétés.

``` syntax
#include <windows.h>

VOID WINAPI MyProtocolDeregister (HPROTOCOL hProtocol)
{
  DestroyPropertyDatabase (hProtocol);
}
```

 

 



