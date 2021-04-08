---
title: Client du gestionnaire de groupe de multidiffusion
description: Un client est une entité qui appelle une fonction MGM, telle qu’un protocole de routage ou une application administrative.
ms.assetid: 98d13b48-9f1d-4649-a5a3-03926c7facee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5f2a8ba63903c084547e3d04ea04474171651
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675577"
---
# <a name="multicast-group-manager-client"></a>Client du gestionnaire de groupe de multidiffusion

Un client est une entité qui appelle une fonction MGM, telle qu’un protocole de routage ou une application administrative.

L’API MGM est principalement utilisée par les protocoles de routage de multidiffusion. Les développeurs de protocoles de routage de multidiffusion utilisent l’API MGM pour :

-   Tenir à jour l’appartenance au groupe
-   Contrôle de la propriété de l’interface
-   Recevoir des notifications du gestionnaire de groupe de multidiffusion concernant les demandes de données multidiffusion de protocoles de routage de multidiffusion

Les applications d’administration spécifiques qui doivent surveiller les entrées de transfert de multidiffusion (MFEs) peuvent le faire sans ajouter ou supprimer l’appartenance à un groupe. Les développeurs d’applications administratives utilisent des fonctions MGM spécifiques pour examiner les informations dans MFEs.

> [!Note]  
> Les protocoles de routage de multidiffusion accèdent également à MFEs.

 

Un MFE transmet des informations que le gestionnaire de groupe de multidiffusion crée en fonction de l’appartenance à un groupe. Les MFEs récupérés à partir du gestionnaire de groupe de multidiffusion peuvent fournir des informations statistiques. Une application administrative peut ensuite utiliser ces informations pour déterminer les actions appropriées. Par exemple, une application administrative peut effectuer des actions basées sur le volume de paquets sur une interface spécifique.

 

 




