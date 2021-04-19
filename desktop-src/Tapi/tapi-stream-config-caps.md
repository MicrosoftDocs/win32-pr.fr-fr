---
description: La structure d’embouts de la configuration de \_ flux TAPI contient des \_ \_ informations de configuration de flux vidéo ou audio.
ms.assetid: 83b39751-b00f-4762-830b-13cafbcb1cfd
title: Structure TAPI_STREAM_CONFIG_CAPS (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379ca481d3bebaf8ceb11bfc2dbdab6642ca20b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530970"
---
# <a name="tapi_stream_config_caps-structure"></a><span data-ttu-id="fb3e4-103">\_Structure d' \_ \_ embouts de la configuration de flux TAPI</span><span class="sxs-lookup"><span data-stu-id="fb3e4-103">TAPI\_STREAM\_CONFIG\_CAPS structure</span></span>

<span data-ttu-id="fb3e4-104">\[ Cette structure n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="fb3e4-104">\[ This structure is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fb3e4-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="fb3e4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="fb3e4-106">La structure d' **\_ \_ \_ embouts** de la configuration de flux TAPI contient des informations de configuration de flux vidéo ou audio.</span><span class="sxs-lookup"><span data-stu-id="fb3e4-106">The **TAPI\_STREAM\_CONFIG\_CAPS** structure contains either video or audio stream configuration information.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb3e4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb3e4-107">Syntax</span></span>


```C++
} TAPI_STREAM_CONFIG_CAPS, *PTAPI_STREAM_CONFIG_CAPS;
```



## <a name="members"></a><span data-ttu-id="fb3e4-108">Membres</span><span class="sxs-lookup"><span data-stu-id="fb3e4-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="fb3e4-109">**CapsType**</span><span class="sxs-lookup"><span data-stu-id="fb3e4-109">**CapsType**</span></span>
</dt> <dd>

<span data-ttu-id="fb3e4-110">Définit si le membre d’Union contient des informations vidéo ou audio.</span><span class="sxs-lookup"><span data-stu-id="fb3e4-110">Defines whether the union member contains video or audio information.</span></span>

</dd> <dt>

<span data-ttu-id="fb3e4-111">**VideoCap**</span><span class="sxs-lookup"><span data-stu-id="fb3e4-111">**VideoCap**</span></span>
</dt> <dd>

<span data-ttu-id="fb3e4-112">Structure de la [**\_ \_ \_ configuration \_ de flux vidéo TAPI**](tapi-video-stream-config-caps.md) contenant les fonctionnalités du flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="fb3e4-112">A [**TAPI\_VIDEO\_STREAM\_CONFIG\_CAPS**](tapi-video-stream-config-caps.md) structure containing the video stream capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="fb3e4-113">**AudioCap**</span><span class="sxs-lookup"><span data-stu-id="fb3e4-113">**AudioCap**</span></span>
</dt> <dd>

<span data-ttu-id="fb3e4-114">Structure [**d' \_ \_ \_ \_ embouts de configuration de flux audio TAPI**](tapi-audio-stream-config-caps.md) contenant les fonctionnalités de flux audio.</span><span class="sxs-lookup"><span data-stu-id="fb3e4-114">A [**TAPI\_AUDIO\_STREAM\_CONFIG\_CAPS**](tapi-audio-stream-config-caps.md) structure containing the audio stream capabilities.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fb3e4-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb3e4-115">Requirements</span></span>



| <span data-ttu-id="fb3e4-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb3e4-116">Requirement</span></span> | <span data-ttu-id="fb3e4-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb3e4-117">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fb3e4-118">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="fb3e4-118">TAPI version</span></span><br/> | <span data-ttu-id="fb3e4-119">Nécessite TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="fb3e4-119">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="fb3e4-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="fb3e4-120">Header</span></span><br/>       | <dl> <span data-ttu-id="fb3e4-121"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb3e4-121"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb3e4-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb3e4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb3e4-123">**ITFormatControl::GetStreamCaps**</span><span class="sxs-lookup"><span data-stu-id="fb3e4-123">**ITFormatControl::GetStreamCaps**</span></span>](itformatcontrol-getstreamcaps.md)
</dt> <dt>

[<span data-ttu-id="fb3e4-124">**StreamConfigCapsType**</span><span class="sxs-lookup"><span data-stu-id="fb3e4-124">**StreamConfigCapsType**</span></span>](streamconfigcapstype.md)
</dt> <dt>

[<span data-ttu-id="fb3e4-125">**extrémités de la \_ \_ configuration du flux vidéo \_ TAPI \_**</span><span class="sxs-lookup"><span data-stu-id="fb3e4-125">**TAPI\_VIDEO\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-video-stream-config-caps.md)
</dt> <dt>

[<span data-ttu-id="fb3e4-126">**extrémités de la \_ \_ configuration du flux audio \_ TAPI \_**</span><span class="sxs-lookup"><span data-stu-id="fb3e4-126">**TAPI\_AUDIO\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-audio-stream-config-caps.md)
</dt> </dl>

 

 




