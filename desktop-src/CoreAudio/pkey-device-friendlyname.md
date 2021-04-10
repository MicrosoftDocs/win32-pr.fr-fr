---
description: La \_ propriété de l’appareil de la \_ propriété FriendlyName du périphérique contient le nom convivial de l’appareil de point de terminaison (par exemple, &\# 0034 ; Haut-parleurs (carte audio XYZ) &\# 0034 ;).
ms.assetid: 3ccd6a78-8bc3-4a46-8f11-7c2ae8a23c63
title: PKEY_Device_FriendlyName (Functiondiscoverykeys \_ devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fab8b8f30e04ae66356fb0910e3767d74b7b697a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103846953"
---
# <a name="pkey_device_friendlyname"></a><span data-ttu-id="6ccdd-103">Périphérique de l' \_ appareil \_</span><span class="sxs-lookup"><span data-stu-id="6ccdd-103">PKEY\_Device\_FriendlyName</span></span>

<span data-ttu-id="6ccdd-104">La **propriété \_ \_ FriendlyName** de l’appareil de la carte à-moi contient le nom convivial de l’appareil de point de terminaison (par exemple, « enceintes audio XYZ) »).</span><span class="sxs-lookup"><span data-stu-id="6ccdd-104">The **PKEY\_Device\_FriendlyName** property contains the friendly name of the endpoint device (for example, "Speakers (XYZ Audio Adapter)").</span></span>

<span data-ttu-id="6ccdd-105">Le membre **VT** de la structure **PROPVARIANT** est défini sur VT \_ LPWStr.</span><span class="sxs-lookup"><span data-stu-id="6ccdd-105">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="6ccdd-106">Le membre **pwszVal** de la structure **PROPVARIANT** pointe vers une chaîne de caractères larges se terminant par un caractère null qui contient le nom convivial de l’appareil de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="6ccdd-106">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains the friendly name of the endpoint device.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ccdd-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ccdd-107">Requirements</span></span>



| <span data-ttu-id="6ccdd-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ccdd-108">Requirement</span></span> | <span data-ttu-id="6ccdd-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ccdd-109">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ccdd-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ccdd-110">Minimum supported client</span></span><br/> | <span data-ttu-id="6ccdd-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6ccdd-111">Windows Vista \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6ccdd-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ccdd-112">Minimum supported server</span></span><br/> | <span data-ttu-id="6ccdd-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6ccdd-113">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="6ccdd-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="6ccdd-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ccdd-115"><dt>Functiondiscoverykeys \_ devpkey. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ccdd-115"><dt>Functiondiscoverykeys\_devpkey.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ccdd-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ccdd-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ccdd-117">Propriétés audio principales</span><span class="sxs-lookup"><span data-stu-id="6ccdd-117">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> <dt>

[<span data-ttu-id="6ccdd-118">Propriétés de l’appareil</span><span class="sxs-lookup"><span data-stu-id="6ccdd-118">Device Properties</span></span>](device-properties.md)
</dt> </dl>

 

 




