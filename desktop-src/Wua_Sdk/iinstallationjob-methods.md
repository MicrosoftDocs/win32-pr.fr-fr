---
description: L’interface IInstallationJob définit les méthodes suivantes.
ms.assetid: 4990ef7c-b6cd-46fc-9e7d-8d1d78edc9f2
title: Méthodes IInstallationJob
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9c188b1d4d749e3bdd9a6f7bdcac179e3703eeb757fd0698dd3bfb67d98fac7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994749"
---
# <a name="iinstallationjob-methods"></a>Méthodes IInstallationJob

L’interface [**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) définit les méthodes suivantes.



| Méthode                                                | Description                                                                                                                                           |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Nettoyage**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)           | Attend la fin d’une opération asynchrone, puis libère tous les rappels.                                                              |
| [**GetProgress**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-getprogress)   | Retourne une interface [**IInstallationProgress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) qui décrit la progression actuelle d’une installation ou d’une désinstallation. |
| [**RequestAbort**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-requestabort) | Effectue une demande d’annulation de l’installation ou de la désinstallation.                                                                                         |



 

 

 



