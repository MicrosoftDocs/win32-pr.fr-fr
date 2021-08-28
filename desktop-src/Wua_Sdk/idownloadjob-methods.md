---
description: L’interface IDownloadJob définit les méthodes suivantes.
ms.assetid: b9a6b722-2e32-4177-bcef-514412e132ec
title: Méthodes IDownloadJob
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03a153120f2d558dcc905d4e8b4de8a0993d842eaec895b7fd881ed2b8504f8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756809"
---
# <a name="idownloadjob-methods"></a>Méthodes IDownloadJob

L’interface [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) définit les méthodes suivantes.



| Méthode                                            | Description                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**Nettoyage**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup)           | Attend la fin d’une opération asynchrone et libère tous les rappels.                                        |
| [**GetProgress**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-getprogress)   | Retourne une interface [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) qui décrit la progression actuelle d’un téléchargement. |
| [**RequestAbort**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-requestabort) | Effectue une demande pour mettre fin à un téléchargement asynchrone.                                                                       |



 

 

 



