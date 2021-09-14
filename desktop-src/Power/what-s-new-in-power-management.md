---
description: Windows 10 permet à votre application d’optimiser la consommation d’énergie lorsqu’elle s’exécute sur un appareil mobile.
ms.assetid: a956b88c-8a75-4c1c-af27-53c69feb1596
title: Nouveautés de la gestion de l’alimentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e6c8394c2e5e6750b5d01fd997d374a9f87e10d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119077"
---
# <a name="whats-new-in-power-management"></a>Nouveautés de la gestion de l'alimentation

Windows 10 permet à votre application d’optimiser la consommation d’énergie lorsqu’elle est exécutée sur un appareil mobile.

## <a name="battery-saver"></a>Économiseur de batterie

Dans cette version, votre application peut être avertie lorsque l’économiseur de batterie est activé ou désactivé. En répondant à des conditions d’alimentation variables, votre application peut fonctionner de concert avec l’économiseur de batterie pour économiser de l’énergie et accroître la durée de vie de la batterie. Pour obtenir des informations générales sur l’économiseur de batterie, consultez [économiseur de batterie (dans les instructions relatives aux composants matériels)](/windows-hardware/design/component-guidelines/battery-saver).

-   [**GUID \_ \_ \_ État de l’économie d’énergie**](power-setting-guids.md) : utilisez ce nouveau GUID avec la fonction [**PowerSettingRegisterNotification**](/windows/desktop/api/Powersetting/nf-powersetting-powersettingregisternotification) pour être averti lorsque l’économiseur de batterie est activé ou désactivé.

-   [**Système \_ \_État**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) de l’alimentation : cette structure a été mise à jour pour prendre en charge l’économiseur de batterie. Le quatrième membre, **SystemStatusFlag** (précédemment nommé **Reserved1**), indique à présent si l’économiseur de batterie est engagé ou non. Utilisez la fonction [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) pour récupérer un pointeur vers cette structure.

 

 
