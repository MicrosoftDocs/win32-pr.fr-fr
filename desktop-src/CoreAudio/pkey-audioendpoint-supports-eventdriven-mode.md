---
description: Le AudioEndpoint de la valeur de la propriété du jeu de la \_ \_ valeur prend en charge le \_ \_ mode EventDriven.
ms.assetid: 9cffd9ae-710b-4d41-aa02-3ab1a065e544
title: PKEY_AudioEndpoint_Supports_EventDriven_Mode (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2707de83721d546040ac878b337faea12f533bb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950784"
---
# <a name="pkey_audioendpoint_supports_eventdriven_mode"></a><span data-ttu-id="ca5b9-103">Le AudioEndpoint de la- \_ \_ prend en charge le \_ \_ mode EventDriven</span><span class="sxs-lookup"><span data-stu-id="ca5b9-103">PKEY\_AudioEndpoint\_Supports\_EventDriven\_Mode</span></span>

<span data-ttu-id="ca5b9-104">Le AudioEndpoint de la valeur de la propriété du jeu de la valeur **\_ \_ prend en charge le \_ \_ mode EventDriven** .</span><span class="sxs-lookup"><span data-stu-id="ca5b9-104">The **PKEY\_AudioEndpoint\_Supports\_EventDriven\_Mode** property indicates whether the endpoint supports the event-driven mode.</span></span>

<span data-ttu-id="ca5b9-105">Le membre **VT** de la structure **PROPVARIANT** est défini sur VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="ca5b9-105">The **vt** member of the **PROPVARIANT** structure is set to VT\_UI4.</span></span>

<span data-ttu-id="ca5b9-106">Le membre **uintVal** de la structure **PROPVARIANT** est une **valeur DWORD** qui indique si le point de terminaison prend en charge le mode piloté par les événements.</span><span class="sxs-lookup"><span data-stu-id="ca5b9-106">The **uintVal** member of the **PROPVARIANT** structure is a **DWORD** that indicates if the endpoint supports the event-driven mode.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca5b9-107">Notes</span><span class="sxs-lookup"><span data-stu-id="ca5b9-107">Remarks</span></span>

<span data-ttu-id="ca5b9-108">Cette valeur de propriété est remplie par un OEM audio dans un fichier. inf pour indiquer que le matériel HDAudio prend en charge le mode piloté par les événements conformément aux exigences du WHQL.</span><span class="sxs-lookup"><span data-stu-id="ca5b9-108">This property value is populated by an audio OEM in an .inf file to indicate that the HDAudio hardware supports event driven mode as per the WHQL requirement.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca5b9-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca5b9-109">Requirements</span></span>



| <span data-ttu-id="ca5b9-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca5b9-110">Requirement</span></span> | <span data-ttu-id="ca5b9-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca5b9-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca5b9-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca5b9-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ca5b9-113">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca5b9-113">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ca5b9-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca5b9-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ca5b9-115">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca5b9-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ca5b9-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="ca5b9-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca5b9-117"><dt>MMDeviceAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca5b9-117"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca5b9-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca5b9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca5b9-119">**Propriétés du point de terminaison audio**</span><span class="sxs-lookup"><span data-stu-id="ca5b9-119">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="ca5b9-120">Propriétés audio principales</span><span class="sxs-lookup"><span data-stu-id="ca5b9-120">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




