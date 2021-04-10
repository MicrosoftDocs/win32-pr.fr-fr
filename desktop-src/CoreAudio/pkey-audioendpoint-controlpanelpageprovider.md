---
description: La \_ propriété hyperAudioEndpoint \_ ControlPanelPageProvider spécifie le CLSID du fournisseur inscrit de l’extension Device-Properties pour l’appareil de point de terminaison audio.
ms.assetid: 429a7572-b609-46fd-946e-ee34ddd6cc5e
title: PKEY_AudioEndpoint_ControlPanelPageProvider (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 205ccdfba799652d9b09af21eefbedd3c3049533
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861153"
---
# <a name="pkey_audioendpoint_controlpanelpageprovider"></a><span data-ttu-id="1d293-103">\_AudioEndpoint \_ ControlPanelPageProvider</span><span class="sxs-lookup"><span data-stu-id="1d293-103">PKEY\_AudioEndpoint\_ControlPanelPageProvider</span></span>

<span data-ttu-id="1d293-104">La **propriété \_ hyperAudioEndpoint \_ ControlPanelPageProvider** spécifie le CLSID du fournisseur inscrit de l’extension Device-Properties pour l’appareil de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="1d293-104">The **PKEY\_AudioEndpoint\_ControlPanelPageProvider** property specifies the CLSID of the registered provider of the device-properties extension for the audio endpoint device.</span></span> <span data-ttu-id="1d293-105">L’extension fournit les propriétés de point de terminaison audio qui sont affichées dans la page Propriétés de l’appareil du panneau de configuration multimédia Windows, Mmsys.cpl.</span><span class="sxs-lookup"><span data-stu-id="1d293-105">The extension supplies the audio endpoint properties that are displayed in the device-properties page of the Windows multimedia control panel, Mmsys.cpl.</span></span> <span data-ttu-id="1d293-106">Pour plus d’informations sur Mmsys.cpl, consultez la documentation de Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="1d293-106">For more information about Mmsys.cpl, see the Windows DDK documentation.</span></span>

<span data-ttu-id="1d293-107">Le membre **VT** de la structure **PROPVARIANT** est défini sur VT \_ LPWStr.</span><span class="sxs-lookup"><span data-stu-id="1d293-107">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="1d293-108">Le membre **pwszVal** de la structure **PROPVARIANT** pointe vers une chaîne de caractères larges se terminant par un caractère null qui contient un GUID qui identifie le fournisseur de l’extension du panneau de contrôle.</span><span class="sxs-lookup"><span data-stu-id="1d293-108">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains a GUID that identifies the provider of the control-panel extension.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d293-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d293-109">Requirements</span></span>



| <span data-ttu-id="1d293-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d293-110">Requirement</span></span> | <span data-ttu-id="1d293-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d293-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d293-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d293-112">Minimum supported client</span></span><br/> | <span data-ttu-id="1d293-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1d293-113">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1d293-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d293-114">Minimum supported server</span></span><br/> | <span data-ttu-id="1d293-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1d293-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1d293-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="1d293-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d293-117"><dt>MMDeviceAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d293-117"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d293-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d293-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d293-119">**Propriétés du point de terminaison audio**</span><span class="sxs-lookup"><span data-stu-id="1d293-119">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="1d293-120">Propriétés audio principales</span><span class="sxs-lookup"><span data-stu-id="1d293-120">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




