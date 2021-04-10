---
title: Stockage persistant sur le serveur
description: Vous pouvez optimiser votre application afin que le stub serveur ne libère pas la mémoire sur le serveur à la fin d’un appel de procédure distante.
ms.assetid: 340334e2-94ac-4be2-a16d-38bc4c64e7db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7237fe6136918e5495ee1f22bac0991d71c5dbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940145"
---
# <a name="persistent-storage-on-the-server"></a>Stockage persistant sur le serveur

Vous pouvez optimiser votre application afin que le stub serveur ne libère pas la mémoire sur le serveur à la fin d’un appel de procédure distante. Par exemple, lorsqu’un descripteur de contexte est manipulé par plusieurs procédures distantes, vous pouvez utiliser l’attribut ACF **\[ allocate (ne pas \_ libérer) \]** pour conserver la mémoire allouée sur le serveur.

L’attribut **\[ allocate (ne pas \_ libérer) \]** est ajouté à la déclaration de **typedef** ACF dans le CCP. Par exemple :

``` syntax
/* ACF file fragment */
typedef [allocate(all_nodes, dont_free)] P_TREE_TYPE;
```

Lorsque l’attribut **\[ allocate (ne pas \_ libérer) \]** est spécifié, la structure des données de l’arborescence est allouée, mais pas libérée, par le stub serveur. Lorsque vous rendez les pointeurs vers des zones de données persistantes disponibles pour d’autres routines, par exemple en copiant les pointeurs vers des variables globales, les données conservées sont accessibles aux autres fonctions serveur. L’attribut **\[ allocate (ne pas \_ libérer) \]** est particulièrement utile pour gérer les structures de pointeur persistantes dans le cadre des informations d’État du serveur associées à un type de handle de contexte.

 

 




