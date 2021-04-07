---
description: Une fois toutes les opérations de fichier en attente, la file d’attente doit être validée. Cela entraîne le traitement des opérations de fichier mises en file d’attente.
ms.assetid: 536f47f5-785e-4a83-a500-c769442e3e68
title: Validation d’une file d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d995f6811dbd19bba9e13f29bc119cdf2f471f74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759790"
---
# <a name="committing-a-queue"></a>Validation d’une file d’attente

Une fois toutes les opérations de fichier en attente, la file d’attente doit être validée. Cela entraîne le traitement des opérations de fichier mises en file d’attente.

Une file d’attente de fichiers ne peut pas être réutilisée une fois qu’elle a été validée. La meilleure pratique consiste à collecter toutes les opérations de fichier requises pour la file d’attente de fichiers et à valider la file d’attente une seule fois. Si un traitement supplémentaire de la file d’attente est requis après sa validation, le descripteur de la file d’attente doit être fermé et une nouvelle file d’attente de fichiers doit être créée. Pour valider la file d’attente de fichiers, appelez la fonction [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) , en spécifiant une routine de rappel. La routine de rappel recevra des notifications de **SetupCommitFileQueue** lors du traitement des opérations de fichier. Si vous souhaitez utiliser la routine de rappel de file d’attente par défaut, vous devez d’abord initialiser le contexte nécessaire en appelant [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) ou [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex). Pour plus d’informations sur la routine de rappel de file d’attente par défaut, consultez [routine de rappel de file d’attente par défaut](default-queue-callback-routine.md).

> [!Note]  
> [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) doit être appelé avant la fermeture de la file d’attente. Toutes les opérations qui ne sont pas validées quand [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) est appelé ne sont pas exécutées.

 

 

 



