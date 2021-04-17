---
description: L’interface IDownloadJob définit les méthodes suivantes.
ms.assetid: b9a6b722-2e32-4177-bcef-514412e132ec
title: Méthodes IDownloadJob
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f68acd6d7fef37c4ce9309c559a1de1b4d516dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526703"
---
# <a name="idownloadjob-methods"></a>Méthodes IDownloadJob

L’interface [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) définit les méthodes suivantes.



| Méthode                                            | Description                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**Nettoyage**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup)           | Attend la fin d’une opération asynchrone et libère tous les rappels.                                        |
| [**GetProgress**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-getprogress)   | Retourne une interface [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) qui décrit la progression actuelle d’un téléchargement. |
| [**RequestAbort**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-requestabort) | Effectue une demande pour mettre fin à un téléchargement asynchrone.                                                                       |



 

 

 



