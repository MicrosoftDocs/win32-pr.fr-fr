---
description: Une fois que la file d’attente a terminé la validation de ses opérations, elle doit être fermée à l’aide de la fonction SetupCloseFileQueue avec le descripteur créé par SetupOpenFileQueue.
ms.assetid: 4cb21699-e476-4832-9678-2bf36f3bda08
title: Fermeture de la file d’attente de fichiers et du fichier INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce5c81c75f7515acfb346b4277e416b0cb2c2a9be6e40464dcfdfc21c3b23bba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887574"
---
# <a name="closing-the-file-queue-and-inf-file"></a>Fermeture de la file d’attente de fichiers et du fichier INF

Une fois que la file d’attente a terminé la validation de ses opérations, elle doit être fermée à l’aide de la fonction [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) avec le descripteur créé par [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue). Le rappel de file d’attente par défaut doit être détruit et recréé pour qu’une autre file d’attente puisse être validée.

Si un contexte par défaut a été initialisé pour une utilisation par la routine de rappel par défaut, il doit également être arrêté en appelant la fonction [**SetupTermDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) . Le *contexte* est un pointeur vers la structure retournée par la fonction [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) .

Lorsque l’accès aux informations INF n’est plus nécessaire, appelez la fonction [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) avec le descripteur créé par [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) pour libérer des ressources système.

 

 



