---
title: Interfaces QMGR
description: Utilisez les interfaces du gestionnaire de files d’attente (QMGR) suivantes pour télécharger des fichiers et surveiller des travaux dans la file d’attente de téléchargement.
ms.assetid: b5b59d4f-fa18-4225-8b6f-5d4033c61650
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a17bd3c27fad81416b916b52b055bc879b44f251113d43b6118e179b609762fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118679993"
---
# <a name="qmgr-interfaces"></a>Interfaces QMGR

\[Les interfaces du gestionnaire de files d’attente (QMGR) peuvent être utilisées dans les systèmes d’exploitation spécifiés dans la section Configuration requise de la rubrique. Il est possible qu’ils soient modifiés ou indisponibles dans les versions ultérieures. Utilisez plutôt les [interfaces bits](bits-interfaces.md).\]

Utilisez les interfaces du gestionnaire de files d’attente (QMGR) suivantes pour télécharger des fichiers et surveiller des travaux dans la file d’attente de téléchargement.



| Interface                                                                 | Description                                                                                                                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IBackgroundCopyCallback1**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopycallback1)<br/>   | Implémentez pour recevoir une notification lorsque des événements se produisent.<br/>                                                                                               |
| [**IBackgroundCopyGroup**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopygroup)<br/>           | Utilisez pour gérer le groupe. Par exemple, ajoutez un travail au groupe, définissez les propriétés du groupe et démarrez et arrêtez le groupe dans la file d’attente de téléchargement.<br/> |
| [**IBackgroundCopyJob1**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyjob1)<br/>             | Utilisez pour ajouter des fichiers au travail et pour récupérer l’état du travail.<br/>                                                                                         |
| [**IBackgroundCopyQMgr**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyqmgr)<br/>             | Utilisez pour créer un nouveau groupe, récupérer un groupe existant ou énumérer tous les groupes de la file d’attente.<br/>                                                       |
| [**IEnumBackgroundCopyGroups**](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopygroups)<br/> | Utilisez pour récupérer une liste de groupes dans la file d’attente de téléchargement.<br/>                                                                                            |
| [**IEnumBackgroundCopyJobs1**](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopyjobs1)<br/>   | Utilisez pour récupérer une liste de travaux dans le groupe.<br/>                                                                                                       |



 

 

 





