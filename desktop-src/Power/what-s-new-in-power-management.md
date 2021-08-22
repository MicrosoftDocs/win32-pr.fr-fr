---
description: Windows 10 permet à votre application d’optimiser la consommation d’énergie lorsqu’elle s’exécute sur un appareil mobile.
ms.assetid: a956b88c-8a75-4c1c-af27-53c69feb1596
title: Nouveautés de la gestion de l’alimentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ac6ba320a98fce339f5bfacfe2d9b4a259be5a8150b2bcaabcac41179869e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143192"
---
# <a name="whats-new-in-power-management"></a>Nouveautés de la gestion de l'alimentation

Windows 10 permet à votre application d’optimiser la consommation d’énergie lorsqu’elle est exécutée sur un appareil mobile.

## <a name="battery-saver"></a>Économiseur de batterie

Dans cette version, votre application peut être avertie lorsque l’économiseur de batterie est activé ou désactivé. En répondant à des conditions d’alimentation variables, votre application peut fonctionner de concert avec l’économiseur de batterie pour économiser de l’énergie et accroître la durée de vie de la batterie. Pour obtenir des informations générales sur l’économiseur de batterie, consultez [économiseur de batterie (dans les instructions relatives aux composants matériels)](/windows-hardware/design/component-guidelines/battery-saver).

-   [**GUID \_ \_ \_ État de l’économie d’énergie**](power-setting-guids.md) : utilisez ce nouveau GUID avec la fonction [**PowerSettingRegisterNotification**](/windows/desktop/api/Powersetting/nf-powersetting-powersettingregisternotification) pour être averti lorsque l’économiseur de batterie est activé ou désactivé.

-   [**Système \_ \_État**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) de l’alimentation : cette structure a été mise à jour pour prendre en charge l’économiseur de batterie. Le quatrième membre, **SystemStatusFlag** (précédemment nommé **Reserved1**), indique à présent si l’économiseur de batterie est engagé ou non. Utilisez la fonction [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) pour récupérer un pointeur vers cette structure.

 

 
