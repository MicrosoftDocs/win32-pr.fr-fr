---
description: Outre la mise en file d’attente des opérations de fichiers individuellement, vous pouvez également mettre en file d’attente tous les fichiers listés dans une section INF.
ms.assetid: 456e1a19-7e9b-40c8-9295-42bb8f740f58
title: Mise en file d’attente d’une section INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5566931131885cf6f300b5a6386639bbd564e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529776"
---
# <a name="queuing-an-inf-section"></a>Mise en file d’attente d’une section INF

Outre la mise en file d’attente des opérations de fichiers individuellement, vous pouvez également mettre en file d’attente tous les fichiers listés dans une section INF.

Vous pouvez faire la file d’attente de tous les fichiers listés dans une section **copier des fichiers** d’un fichier INF en appelant [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona). Pour que cette fonction aboutisse, la section **copier les fichiers** doit être au format approprié et le fichier INF, ou l’un de ses fichiers ajoutés, doit contenir les sections **SourceDisksFiles** et **SourceDisksNames** .

De même, si vous souhaitez supprimer tous les fichiers spécifiés dans la section **supprimer des fichiers** d’un fichier INF, vous pouvez appeler [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona). Pour renommer tous les fichiers d’une section **Renommer des fichiers** d’un fichier INF, utilisez [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona).

 

 



