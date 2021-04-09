---
description: La \_ propriété AudioEndpoint \_ JackSubType contient un GUID de catégorie de sortie pour un périphérique de point de terminaison audio.
ms.assetid: 5d712823-73e3-4872-a1ea-c166ed41ffa0
title: PKEY_AudioEndpoint_JackSubType (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3546c9741dcfd6065372f0a88a3ce3a921daad8d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111322"
---
# <a name="pkey_audioendpoint_jacksubtype"></a><span data-ttu-id="1f05d-103">\_AudioEndpoint \_ JackSubType</span><span class="sxs-lookup"><span data-stu-id="1f05d-103">PKEY\_AudioEndpoint\_JackSubType</span></span>

<span data-ttu-id="1f05d-104">La **propriété \_ AudioEndpoint \_ JACKSUBTYPE** contient un GUID de catégorie de sortie pour un périphérique de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="1f05d-104">The **PKEY\_AudioEndpoint\_JackSubType** property contains an output category GUID for an audio endpoint device.</span></span> <span data-ttu-id="1f05d-105">Le fichier d’en-tête Ksmedia. h définit les GUID. chaque GUID spécifie le type de connexion.</span><span class="sxs-lookup"><span data-stu-id="1f05d-105">The header file Ksmedia.h defines the GUIDs; each GUID specifies the type of connection.</span></span> <span data-ttu-id="1f05d-106">Ces GUID ont également des catégories pin associées.</span><span class="sxs-lookup"><span data-stu-id="1f05d-106">These GUIDs also have associated pin categories.</span></span> <span data-ttu-id="1f05d-107">Par exemple, le fichier d’en-tête Ksmedia. h définit l' **\_ \_ interface GUID KSNODETYPE DisplayPort** pour un port d’affichage qui se connecte au code confidentiel KS défini par le GUID **PINNAME le \_ DisplayPort \_**.</span><span class="sxs-lookup"><span data-stu-id="1f05d-107">For example, header file Ksmedia.h defines the GUID **KSNODETYPE\_DISPLAYPORT\_INTERFACE** for a display port that connects with the KS pin defined by the GUID **PINNAME\_DISPLAYPORT\_OUT**.</span></span>

<span data-ttu-id="1f05d-108">Pour plus d’informations, consultez la description des propriétés de catégorie de code confidentiel dans la documentation de Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="1f05d-108">For more information, see the description of pin category properties in the Windows DDK documentation.</span></span>

<span data-ttu-id="1f05d-109">Le membre **VT** de la structure **PROPVARIANT** est défini sur **VT \_ LPWStr**.</span><span class="sxs-lookup"><span data-stu-id="1f05d-109">The **vt** member of the **PROPVARIANT** structure is set to **VT\_LPWSTR**.</span></span>

<span data-ttu-id="1f05d-110">Le membre **pwszVal** de la structure **PROPVARIANT** pointe vers une chaîne de caractères larges se terminant par un caractère null qui contient un GUID de catégorie.</span><span class="sxs-lookup"><span data-stu-id="1f05d-110">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains a category GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f05d-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f05d-111">Requirements</span></span>



| <span data-ttu-id="1f05d-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f05d-112">Requirement</span></span> | <span data-ttu-id="1f05d-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f05d-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f05d-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f05d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1f05d-115">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f05d-115">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1f05d-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f05d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1f05d-117">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f05d-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1f05d-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="1f05d-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f05d-119"><dt>MMDeviceAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f05d-119"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f05d-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f05d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f05d-121">**Propriétés du point de terminaison audio**</span><span class="sxs-lookup"><span data-stu-id="1f05d-121">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="1f05d-122">Propriétés audio principales</span><span class="sxs-lookup"><span data-stu-id="1f05d-122">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




