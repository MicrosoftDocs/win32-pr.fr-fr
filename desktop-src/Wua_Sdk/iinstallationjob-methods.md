---
description: L’interface IInstallationJob définit les méthodes suivantes.
ms.assetid: 4990ef7c-b6cd-46fc-9e7d-8d1d78edc9f2
title: Méthodes IInstallationJob
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0c1a5850f3d71ad1a6a51046fe890ea9bc7426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113535"
---
# <a name="iinstallationjob-methods"></a>Méthodes IInstallationJob

L’interface [**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) définit les méthodes suivantes.



| Méthode                                                | Description                                                                                                                                           |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Nettoyage**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)           | Attend la fin d’une opération asynchrone, puis libère tous les rappels.                                                              |
| [**GetProgress**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-getprogress)   | Retourne une interface [**IInstallationProgress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) qui décrit la progression actuelle d’une installation ou d’une désinstallation. |
| [**RequestAbort**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-requestabort) | Effectue une demande d’annulation de l’installation ou de la désinstallation.                                                                                         |



 

 

 



