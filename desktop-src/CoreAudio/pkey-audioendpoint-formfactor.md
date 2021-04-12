---
description: La \_ propriété AudioEndpoint de la \_ propriété de type FormFactor spécifie le facteur de forme du périphérique de point de terminaison audio. Le facteur de forme indique les attributs physiques du périphérique de point de terminaison audio manipulé par l’utilisateur.
ms.assetid: f49cb7da-3b50-47e2-90b4-1a885001b5d7
title: PKEY_AudioEndpoint_FormFactor (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5833470e2a2848f9454f3b5eefbf852f452f033
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483681"
---
# <a name="pkey_audioendpoint_formfactor"></a><span data-ttu-id="9635c-104">\_AudioEndpoint \_ FormFactor</span><span class="sxs-lookup"><span data-stu-id="9635c-104">PKEY\_AudioEndpoint\_FormFactor</span></span>

<span data-ttu-id="9635c-105">La **propriété \_ AudioEndpoint \_** de la propriété de type FormFactor spécifie le facteur de forme du périphérique de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="9635c-105">The **PKEY\_AudioEndpoint\_FormFactor** property specifies the form factor of the audio endpoint device.</span></span> <span data-ttu-id="9635c-106">Le facteur de forme indique les attributs physiques du périphérique de point de terminaison audio manipulé par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9635c-106">The form factor indicates the physical attributes of the audio endpoint device that the user manipulates.</span></span>

<span data-ttu-id="9635c-107">Le membre **VT** de la structure **PROPVARIANT** est défini sur VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="9635c-107">The **vt** member of the **PROPVARIANT** structure is set to VT\_UI4.</span></span>

<span data-ttu-id="9635c-108">Le membre **uintVal** de la structure **PROPVARIANT** contient une valeur d’énumération qui est castée en type uint.</span><span class="sxs-lookup"><span data-stu-id="9635c-108">The **uintVal** member of the **PROPVARIANT** structure contains an enumeration value that is cast to type UINT.</span></span> <span data-ttu-id="9635c-109">Elle est définie sur l’une des valeurs d’énumération [**EndpointFormFactor**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-endpointformfactor) suivantes :</span><span class="sxs-lookup"><span data-stu-id="9635c-109">It is set to one of the following [**EndpointFormFactor**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-endpointformfactor) enumeration values:</span></span>

-   <span data-ttu-id="9635c-110">RemoteNetworkDevice</span><span class="sxs-lookup"><span data-stu-id="9635c-110">RemoteNetworkDevice</span></span>
-   <span data-ttu-id="9635c-111">Haut-parleurs</span><span class="sxs-lookup"><span data-stu-id="9635c-111">Speakers</span></span>
-   <span data-ttu-id="9635c-112">LineLevel</span><span class="sxs-lookup"><span data-stu-id="9635c-112">LineLevel</span></span>
-   <span data-ttu-id="9635c-113">Un casque</span><span class="sxs-lookup"><span data-stu-id="9635c-113">Headphones</span></span>
-   <span data-ttu-id="9635c-114">Microphone</span><span class="sxs-lookup"><span data-stu-id="9635c-114">Microphone</span></span>
-   <span data-ttu-id="9635c-115">Casque</span><span class="sxs-lookup"><span data-stu-id="9635c-115">Headset</span></span>
-   <span data-ttu-id="9635c-116">Téléphone</span><span class="sxs-lookup"><span data-stu-id="9635c-116">Handset</span></span>
-   <span data-ttu-id="9635c-117">UnknownDigitalPassthrough</span><span class="sxs-lookup"><span data-stu-id="9635c-117">UnknownDigitalPassthrough</span></span>
-   <span data-ttu-id="9635c-118">SPDIF</span><span class="sxs-lookup"><span data-stu-id="9635c-118">SPDIF</span></span>
-   <span data-ttu-id="9635c-119">HDMI</span><span class="sxs-lookup"><span data-stu-id="9635c-119">HDMI</span></span>
-   <span data-ttu-id="9635c-120">UnknownFormFactor</span><span class="sxs-lookup"><span data-stu-id="9635c-120">UnknownFormFactor</span></span>

## <a name="requirements"></a><span data-ttu-id="9635c-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9635c-121">Requirements</span></span>



| <span data-ttu-id="9635c-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9635c-122">Requirement</span></span> | <span data-ttu-id="9635c-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="9635c-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9635c-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9635c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9635c-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9635c-125">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9635c-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9635c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9635c-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9635c-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9635c-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="9635c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9635c-129"><dt>MMDeviceAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="9635c-129"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9635c-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9635c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9635c-131">**Propriétés du point de terminaison audio**</span><span class="sxs-lookup"><span data-stu-id="9635c-131">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="9635c-132">Propriétés audio principales</span><span class="sxs-lookup"><span data-stu-id="9635c-132">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




