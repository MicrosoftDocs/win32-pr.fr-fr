---
description: La \_ \_ propriété de l’appareil de la propriété DeviceDesc de l’appareil contient la description de l’appareil du point de terminaison (par exemple, &\# 0034 ; Haut-parleurs&\# 0034 ;).
ms.assetid: 23715497-a74d-4dab-aade-c7779fe80aa6
title: PKEY_Device_DeviceDesc (Functiondiscoverykeys \_ devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eb68f874979e660fec0cd563db9bcaceb7d5b74
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103846961"
---
# <a name="pkey_device_devicedesc"></a><span data-ttu-id="e7270-103">Périphérique de l' \_ appareil \_</span><span class="sxs-lookup"><span data-stu-id="e7270-103">PKEY\_Device\_DeviceDesc</span></span>

<span data-ttu-id="e7270-104">La propriété de l’appareil de groupe de la propriété **\_ \_ DeviceDesc** contient la description de l’appareil du point de terminaison (par exemple, « Speakers »).</span><span class="sxs-lookup"><span data-stu-id="e7270-104">The **PKEY\_Device\_DeviceDesc** property contains the device description of the endpoint device (for example, "Speakers").</span></span>

<span data-ttu-id="e7270-105">Le membre **VT** de la structure **PROPVARIANT** est défini sur VT \_ LPWStr.</span><span class="sxs-lookup"><span data-stu-id="e7270-105">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="e7270-106">Le membre **pwszVal** de la structure **PROPVARIANT** pointe vers une chaîne de caractères larges se terminant par un caractère null qui contient la description de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e7270-106">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains the device description.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7270-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7270-107">Requirements</span></span>



| <span data-ttu-id="e7270-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7270-108">Requirement</span></span> | <span data-ttu-id="e7270-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7270-109">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7270-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7270-110">Minimum supported client</span></span><br/> | <span data-ttu-id="e7270-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7270-111">Windows Vista \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e7270-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7270-112">Minimum supported server</span></span><br/> | <span data-ttu-id="e7270-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7270-113">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="e7270-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="e7270-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7270-115"><dt>Functiondiscoverykeys \_ devpkey. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7270-115"><dt>Functiondiscoverykeys\_devpkey.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7270-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7270-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7270-117">Propriétés audio principales</span><span class="sxs-lookup"><span data-stu-id="e7270-117">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> <dt>

[<span data-ttu-id="e7270-118">Propriétés de l’appareil</span><span class="sxs-lookup"><span data-stu-id="e7270-118">Device Properties</span></span>](device-properties.md)
</dt> </dl>

 

 




