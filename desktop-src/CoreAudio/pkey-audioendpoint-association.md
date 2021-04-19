---
description: La \_ \_ propriété d’association AudioEndpoint de la pièce multidiffusion associe une catégorie de code confidentiel de diffusion en continu (KS) à un périphérique de point de terminaison audio.
ms.assetid: a20e082c-eddb-4b81-b851-49350b87e69a
title: PKEY_AudioEndpoint_Association (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe2a7ec4f979e12dd6b548d27e0112c784105074
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514759"
---
# <a name="pkey_audioendpoint_association"></a><span data-ttu-id="33fcb-103">Association de AudioEndpoint de la \_ \_</span><span class="sxs-lookup"><span data-stu-id="33fcb-103">PKEY\_AudioEndpoint\_Association</span></span>

<span data-ttu-id="33fcb-104">La propriété d' **\_ \_ Association AudioEndpoint** de la pièce multidiffusion associe une catégorie de code confidentiel de diffusion en continu (KS) à un périphérique de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="33fcb-104">The **PKEY\_AudioEndpoint\_Association** property associates a kernel-streaming (KS) pin category with an audio endpoint device.</span></span> <span data-ttu-id="33fcb-105">Le fichier. inf qui installe un adaptateur audio affecte une catégorie de code confidentiel à chaque code confidentiel KS de l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="33fcb-105">The .inf file that installs an audio adapter assigns a pin category to each KS pin in the adapter.</span></span> <span data-ttu-id="33fcb-106">Un code PIN KS sur un appareil d’adaptateur représente le point auquel un flux audio entre ou quitte l’appareil.</span><span class="sxs-lookup"><span data-stu-id="33fcb-106">A KS pin on an adapter device represents the point at which an audio stream enters or leaves the device.</span></span> <span data-ttu-id="33fcb-107">Une catégorie de code confidentiel est un GUID qui spécifie le type de fonction effectuée par un code confidentiel KS.</span><span class="sxs-lookup"><span data-stu-id="33fcb-107">A pin category is a GUID that specifies the type of function performed by a KS pin.</span></span> <span data-ttu-id="33fcb-108">Par exemple, le fichier d’en-tête Ksmedia. h définit le microphone KSNODETYPE GUID de catégorie pin \_ pour indiquer un code confidentiel KS qui se connecte à un microphone, et KSNODETYPE \_ casque pour indiquer un code confidentiel KS qui se connecte au casque.</span><span class="sxs-lookup"><span data-stu-id="33fcb-108">For example, header file Ksmedia.h defines pin-category GUID KSNODETYPE\_MICROPHONE to indicate a KS pin that connects to a microphone, and KSNODETYPE\_HEADPHONES to indicate a KS pin that connects to headphones.</span></span> <span data-ttu-id="33fcb-109">Pour plus d’informations, consultez la description des propriétés de catégorie de code confidentiel dans la documentation de Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="33fcb-109">For more information, see the description of pin category properties in the Windows DDK documentation.</span></span>

<span data-ttu-id="33fcb-110">Le membre **VT** de la structure **PROPVARIANT** est défini sur VT \_ LPWStr.</span><span class="sxs-lookup"><span data-stu-id="33fcb-110">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="33fcb-111">Le membre **pwszVal** de la structure **PROPVARIANT** pointe vers une chaîne de caractères larges se terminant par un caractère null qui contient un GUID de catégorie de code confidentiel KS.</span><span class="sxs-lookup"><span data-stu-id="33fcb-111">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains a KS pin category GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="33fcb-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33fcb-112">Requirements</span></span>



| <span data-ttu-id="33fcb-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33fcb-113">Requirement</span></span> | <span data-ttu-id="33fcb-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="33fcb-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="33fcb-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33fcb-115">Minimum supported client</span></span><br/> | <span data-ttu-id="33fcb-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33fcb-116">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="33fcb-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33fcb-117">Minimum supported server</span></span><br/> | <span data-ttu-id="33fcb-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33fcb-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="33fcb-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="33fcb-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="33fcb-120"><dt>MMDeviceAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="33fcb-120"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33fcb-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33fcb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33fcb-122">**Propriétés du point de terminaison audio**</span><span class="sxs-lookup"><span data-stu-id="33fcb-122">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="33fcb-123">Propriétés audio principales</span><span class="sxs-lookup"><span data-stu-id="33fcb-123">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




