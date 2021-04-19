---
description: L’interface IDownloadJob définit les propriétés suivantes.
ms.assetid: 50e672d7-0ad6-402d-878c-4ac79b70a036
title: Propriétés IDownloadJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c9bd940b4b091f2eeefbaaa2a60d66306a3e14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515267"
---
# <a name="idownloadjob-properties"></a>Propriétés IDownloadJob

L’interface [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) définit les propriétés suivantes.



| Propriété                                        | Description                                                                                                                                              |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AsyncState**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_asyncstate)   | Obtient l’objet d’état spécifique à l’appelant qui est passé à la méthode [**IUpdateDownloader. BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) .           |
| [**IsCompleted**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_iscompleted) | Obtient le paramètre qui indique si l’appel à [**IUpdateDownloader. BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) a été traité complètement. |
| [**Mises à jour**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_updates)         | Obtient une interface qui contient une collection en lecture seule des mises à jour spécifiées dans un téléchargement.                                                  |



 

 

 



