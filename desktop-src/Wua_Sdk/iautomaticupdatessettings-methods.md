---
description: L’interface IAutomaticUpdatesSettings définit les méthodes suivantes.
ms.assetid: 2c6df896-bb59-4d77-acde-64e36ecb7d75
title: Méthodes IAutomaticUpdatesSettings
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5ae30a987dcf9d6573c179e7ef453c10c35a84b915b76a16439ba83a7174fd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049467"
---
# <a name="iautomaticupdatessettings-methods"></a>Méthodes IAutomaticUpdatesSettings

L’interface [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) définit les méthodes suivantes.



| Méthode                                               | Description                                      |
|------------------------------------------------------|--------------------------------------------------|
| [**Actualiser**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-refresh) | Récupère les derniers paramètres de Mises à jour automatiques. |
| [**Enregistrer**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)       | Applique les paramètres de Mises à jour automatiques actuels.  |



 

> [!Note]  
> sur Windows RT, vous ne pouvez plus utiliser la méthode [**IAutomaticUpdatesSettings :: Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save) pour configurer des paramètres de Windows Update par programmation. L’opération de configuration échoue si vous utilisez **Save** pour définir une valeur autre que 4 ([**aunlScheduledInstallation**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel)).

 

 

 



