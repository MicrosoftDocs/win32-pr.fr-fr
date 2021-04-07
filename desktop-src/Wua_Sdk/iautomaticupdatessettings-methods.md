---
description: L’interface IAutomaticUpdatesSettings définit les méthodes suivantes.
ms.assetid: 2c6df896-bb59-4d77-acde-64e36ecb7d75
title: Méthodes IAutomaticUpdatesSettings
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a9ecfc43539f70b9373a6db298acc6c688e83a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863746"
---
# <a name="iautomaticupdatessettings-methods"></a>Méthodes IAutomaticUpdatesSettings

L’interface [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) définit les méthodes suivantes.



| Méthode                                               | Description                                      |
|------------------------------------------------------|--------------------------------------------------|
| [**Actualiser**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-refresh) | Récupère les derniers paramètres de Mises à jour automatiques. |
| [**Enregistrer**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)       | Applique les paramètres de Mises à jour automatiques actuels.  |



 

> [!Note]  
> Sur Windows RT, vous ne pouvez plus utiliser la méthode [**IAutomaticUpdatesSettings :: Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save) pour configurer des paramètres de Windows Update par programmation. L’opération de configuration échoue si vous utilisez **Save** pour définir une valeur autre que 4 ([**aunlScheduledInstallation**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel)).

 

 

 



