---
description: '\_ \_ Propriété DeviceInterface FriendlyName.'
ms.assetid: beef2153-489f-4ff5-a161-b4e2cd4ac1fa
title: PKEY_DeviceInterface_FriendlyName (Functiondiscoverykeys \_ devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7590e9254e336bf9dbfe0fdeb3349bf19c0b8c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110006"
---
# <a name="pkey_deviceinterface_friendlyname"></a><span data-ttu-id="a4f24-103">\_Deviceinterface \_ FriendlyName FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a4f24-103">PKEY\_DeviceInterface\_FriendlyName</span></span>

<span data-ttu-id="a4f24-104">La **propriété \_ hyperDeviceInterface \_ FriendlyName FriendlyName** contient le nom convivial de la carte audio à laquelle l’appareil de point de terminaison est attaché (par exemple, « carte audio XYZ »).</span><span class="sxs-lookup"><span data-stu-id="a4f24-104">The **PKEY\_DeviceInterface\_FriendlyName** property contains the friendly name of the audio adapter to which the endpoint device is attached (for example, "XYZ Audio Adapter").</span></span>

<span data-ttu-id="a4f24-105">Le membre **VT** de la structure **PROPVARIANT** est défini sur VT \_ LPWStr.</span><span class="sxs-lookup"><span data-stu-id="a4f24-105">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="a4f24-106">Le membre **pwszVal** de la structure **PROPVARIANT** pointe vers une chaîne de caractères larges se terminant par un caractère null qui contient le nom convivial.</span><span class="sxs-lookup"><span data-stu-id="a4f24-106">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains the friendly name.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4f24-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4f24-107">Requirements</span></span>



| <span data-ttu-id="a4f24-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4f24-108">Requirement</span></span> | <span data-ttu-id="a4f24-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4f24-109">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4f24-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4f24-110">Minimum supported client</span></span><br/> | <span data-ttu-id="a4f24-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a4f24-111">Windows Vista \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a4f24-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4f24-112">Minimum supported server</span></span><br/> | <span data-ttu-id="a4f24-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a4f24-113">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="a4f24-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="a4f24-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4f24-115"><dt>Functiondiscoverykeys \_ devpkey. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4f24-115"><dt>Functiondiscoverykeys\_devpkey.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4f24-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4f24-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4f24-117">Propriétés audio principales</span><span class="sxs-lookup"><span data-stu-id="a4f24-117">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> <dt>

[<span data-ttu-id="a4f24-118">Propriétés de l’appareil</span><span class="sxs-lookup"><span data-stu-id="a4f24-118">Device Properties</span></span>](device-properties.md)
</dt> </dl>

 

 




