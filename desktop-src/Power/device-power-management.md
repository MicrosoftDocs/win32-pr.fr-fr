---
description: L’API Power de l’appareil facilite la détermination des appareils qui sont en mesure d’éveil du système à partir d’un état de veille, ainsi que les États de veille pour lesquels ces appareils prennent en charge la mise en éveil. Pour plus d’informations sur les États de veille, consultez États d’alimentation du système.
ms.assetid: aaa776e5-3fc2-41bd-a805-6c09ef73807b
title: Gestion de l’alimentation des appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0982b7de23f7b7d8cf39686c854d64f284d1ce2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951994"
---
# <a name="device-power-management"></a><span data-ttu-id="215b4-104">Gestion de l’alimentation des appareils</span><span class="sxs-lookup"><span data-stu-id="215b4-104">Device Power Management</span></span>

<span data-ttu-id="215b4-105">L’API Power de l’appareil facilite la détermination des appareils qui sont en mesure d’éveil du système à partir d’un état de veille, ainsi que les États de veille pour lesquels ces appareils prennent en charge la mise en éveil.</span><span class="sxs-lookup"><span data-stu-id="215b4-105">The Device Power API makes it easy to determine which devices are able to wake the system from a sleep state, and which sleep states those devices support waking from.</span></span> <span data-ttu-id="215b4-106">Pour plus d’informations sur les États de veille, consultez [États d’alimentation du système](system-power-states.md).</span><span class="sxs-lookup"><span data-stu-id="215b4-106">For more information about sleep states, see [System Power States](system-power-states.md).</span></span>

<span data-ttu-id="215b4-107">La fonction [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) peut être utilisée pour rechercher des appareils qui correspondent à des critères spécifiés dans la liste des appareils.</span><span class="sxs-lookup"><span data-stu-id="215b4-107">The [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) function can be used to search the device list for devices that match specified criteria.</span></span> <span data-ttu-id="215b4-108">Les critères peuvent inclure la capacité de l’appareil à prendre en charge un État du système ou à sortir de cet État.</span><span class="sxs-lookup"><span data-stu-id="215b4-108">The criteria may include the device's ability to support a system state, or wake from that state.</span></span> <span data-ttu-id="215b4-109">Les indicateurs actuellement pris en charge sont disponibles dans Winnt. h et DevPower. h.</span><span class="sxs-lookup"><span data-stu-id="215b4-109">Currently supported flags can be found in WinNT.h and DevPower.h.</span></span>

<span data-ttu-id="215b4-110">La fonction [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) active ou désactive un appareil spécifié pour sortir le système d’un état de veille.</span><span class="sxs-lookup"><span data-stu-id="215b4-110">The [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) function enables or disables a specified device from waking the system from a sleep state.</span></span>

<span data-ttu-id="215b4-111">L’API d’alimentation des appareils permet aux développeurs de créer une meilleure expérience utilisateur en donnant à l’utilisateur des informations supplémentaires sur ce que le système fait et davantage de contrôle sur les appareils du système.</span><span class="sxs-lookup"><span data-stu-id="215b4-111">The Device Power API allows developers to create a better user experience by giving the user more information about what the system is doing, and more control over the devices in the system.</span></span> <span data-ttu-id="215b4-112">La puissance de l’appareil est utile dans les situations où la consommation d’énergie est essentielle, par exemple dans les appareils portables fonctionnant sur batteries.</span><span class="sxs-lookup"><span data-stu-id="215b4-112">Device Power is useful in situations where power consumption is critical, such as in portable devices running on batteries.</span></span> <span data-ttu-id="215b4-113">Par exemple, le schéma de gestion de l’alimentation utilisé dans un ordinateur de bureau peut ne pas être optimal pour un ordinateur portable, de sorte que l’utilisateur peut vouloir désactiver l’éveil du système par certains appareils.</span><span class="sxs-lookup"><span data-stu-id="215b4-113">For example, the power management scheme used in a desktop computer may not be the optimal scheme for a laptop computer, so the user may want to disable certain devices from waking the system.</span></span> <span data-ttu-id="215b4-114">Cela peut économiser de l’énergie, car les appareils désactivés ne dessinent pas de puissance pendant que le système est en mode veille.</span><span class="sxs-lookup"><span data-stu-id="215b4-114">This can conserve energy because the disabled devices will not draw power while the system is in sleep mode.</span></span>

<span data-ttu-id="215b4-115">Pour obtenir un exemple, consultez [utilisation de l’API Power Device](using-the-device-power-api.md).</span><span class="sxs-lookup"><span data-stu-id="215b4-115">For an example, see [Using the Device Power API](using-the-device-power-api.md).</span></span>

 

 



