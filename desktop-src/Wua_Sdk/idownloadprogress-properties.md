---
description: L’interface IDownloadProgress définit les propriétés suivantes.
ms.assetid: 8f64c702-b2b5-4a5f-9365-bc962e35f499
title: Propriétés IDownloadProgress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469246acb59b4aa58efcbf4bb5aa7f04b7e44b6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951236"
---
# <a name="idownloadprogress-properties"></a>Propriétés IDownloadProgress

L’interface [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) définit les propriétés suivantes.



| Propriété                                                                               | Description                                                                                                                                      |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CurrentUpdateBytesDownloaded**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytesdownloaded) | Obtient une chaîne qui spécifie la quantité de données transférées pour le ou les fichiers de la mise à jour en cours de téléchargement, en octets.  |
| [**CurrentUpdateBytesToDownload**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytestodownload) | Obtient une chaîne qui estime la quantité de données à transférer pour le ou les fichiers de la mise à jour en cours de téléchargement, en octets. |
| [**CurrentUpdateDownloadPhase**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatedownloadphase)     | Obtient une valeur d’énumération [**DownloadPhase**](/windows/win32/api/wuapi/ne-wuapi-downloadphase) qui spécifie la phase du téléchargement actuellement en cours.          |
| [**CurrentUpdateIndex**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdateindex)                     | Obtient une valeur d’index de base zéro qui spécifie la mise à jour en cours de téléchargement lorsque plusieurs mises à jour ont été sélectionnées.             |
| [**CurrentUpdatePercentComplete**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatepercentcomplete) | Obtient une estimation du pourcentage de la mise à jour actuelle qui a été téléchargée.                                                               |
| [**PourcentageAchevé**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_percentcomplete)                           | Obtient une estimation du pourcentage de toutes les mises à jour qui ont été téléchargées.                                                                 |
| [**TotalBytesDownloaded**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytesdownloaded)                 | Obtient une chaîne qui spécifie la quantité totale de données téléchargées, en octets.                                                        |
| [**TotalBytesToDownload**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytestodownload)                 | Obtient une chaîne qui représente l’estimation de la quantité totale de données qui seront téléchargées, en octets.                                        |



 

 

 



