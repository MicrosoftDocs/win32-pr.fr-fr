---
title: Passage à l’état passif
description: Passage à l’état passif
ms.assetid: 544760e6-1706-4384-8e17-8971f0e0c5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a0a3a93b0ff0bd1c16701c82f271847ee435375112a8e7a03120155928fe1ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736853"
---
# <a name="entering-the-passive-state"></a>Passage à l’état passif

La fermeture d’objet force un objet incorporé ou lié à l’état passif. Elle est généralement lancée à partir de l’interface utilisateur de l’application serveur OLE, par exemple lorsque l’utilisateur sélectionne la commande fichier fermer. Dans ce cas, l’application serveur OLE notifie le conteneur, ce qui libère son décompte de références sur l’objet. Lorsque toutes les références à l’objet ont été libérées, l’objet peut être libéré. Lorsque tous les objets ont été libérés, l’application serveur OLE peut se terminer en toute sécurité.

Une application conteneur peut également initier la fermeture de l’objet. Pour fermer un objet, le conteneur libère son décompte de références après avoir effectué une opération d’enregistrement facultative. Vous pouvez concevoir des conteneurs pour libérer des objets lorsqu’ils sont en cours de désactivation après une session d’activation sur place, ce qui permet à l’utilisateur de cliquer à l’extérieur de l’objet sans perdre la session de modification active.

 

 




