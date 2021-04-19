---
description: Windows 10 permet à votre application d’optimiser la consommation d’énergie lorsqu’elle s’exécute sur un appareil mobile.
ms.assetid: a956b88c-8a75-4c1c-af27-53c69feb1596
title: Nouveautés de la gestion de l’alimentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e6c8394c2e5e6750b5d01fd997d374a9f87e10d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534512"
---
# <a name="whats-new-in-power-management"></a><span data-ttu-id="8581e-103">Nouveautés de la gestion de l'alimentation</span><span class="sxs-lookup"><span data-stu-id="8581e-103">What's New in Power Management</span></span>

<span data-ttu-id="8581e-104">Windows 10 permet à votre application d’optimiser la consommation d’énergie lorsqu’elle est exécutée sur un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="8581e-104">Windows 10 helps your application optimize power consumption when it's running on a mobile device.</span></span>

## <a name="battery-saver"></a><span data-ttu-id="8581e-105">Économiseur de batterie</span><span class="sxs-lookup"><span data-stu-id="8581e-105">Battery saver</span></span>

<span data-ttu-id="8581e-106">Dans cette version, votre application peut être avertie lorsque l’économiseur de batterie est activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="8581e-106">In this release, your application can be notified when battery saver is turned on or off.</span></span> <span data-ttu-id="8581e-107">En répondant à des conditions d’alimentation variables, votre application peut fonctionner de concert avec l’économiseur de batterie pour économiser de l’énergie et accroître la durée de vie de la batterie.</span><span class="sxs-lookup"><span data-stu-id="8581e-107">By responding to changing power conditions, your application can work in concert with battery saver to save energy and help extend battery life.</span></span> <span data-ttu-id="8581e-108">Pour obtenir des informations générales sur l’économiseur de batterie, consultez [économiseur de batterie (dans les instructions relatives aux composants matériels)](/windows-hardware/design/component-guidelines/battery-saver).</span><span class="sxs-lookup"><span data-stu-id="8581e-108">For general information about battery saver, see [battery saver (in the hardware component guidelines)](/windows-hardware/design/component-guidelines/battery-saver).</span></span>

-   <span data-ttu-id="8581e-109">[**GUID \_ \_ \_ État de l’économie d’énergie**](power-setting-guids.md) : utilisez ce nouveau GUID avec la fonction [**PowerSettingRegisterNotification**](/windows/desktop/api/Powersetting/nf-powersetting-powersettingregisternotification) pour être averti lorsque l’économiseur de batterie est activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="8581e-109">[**GUID\_POWER\_SAVING\_STATUS**](power-setting-guids.md) : Use this new GUID with the [**PowerSettingRegisterNotification**](/windows/desktop/api/Powersetting/nf-powersetting-powersettingregisternotification) function to be notified when battery saver is turned on or off.</span></span>

-   <span data-ttu-id="8581e-110">[**Système \_ \_État**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) de l’alimentation : cette structure a été mise à jour pour prendre en charge l’économiseur de batterie.</span><span class="sxs-lookup"><span data-stu-id="8581e-110">[**SYSTEM\_POWER\_STATUS**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) : This structure has been updated to support battery saver.</span></span> <span data-ttu-id="8581e-111">Le quatrième membre, **SystemStatusFlag** (précédemment nommé **Reserved1**), indique à présent si l’économiseur de batterie est engagé ou non.</span><span class="sxs-lookup"><span data-stu-id="8581e-111">The fourth member, **SystemStatusFlag** (previously named **Reserved1**), now indicates if battery saver is engaged or not.</span></span> <span data-ttu-id="8581e-112">Utilisez la fonction [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) pour récupérer un pointeur vers cette structure.</span><span class="sxs-lookup"><span data-stu-id="8581e-112">Use the [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) function to retrieve a pointer to this structure.</span></span>

 

 
