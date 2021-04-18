---
description: L' \_ énumération des capacités h245 décrit la prise en charge des formats audio et vidéo.
ms.assetid: 76aeb3a1-3233-4425-b9db-efacbedc309e
title: Énumération H245_CAPABILITY (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae7a6f81f87480f221f87680d9cf086120deb2de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526662"
---
# <a name="h245_capability-enumeration"></a><span data-ttu-id="6155e-103">\_Énumération des fonctionnalités h245</span><span class="sxs-lookup"><span data-stu-id="6155e-103">H245\_CAPABILITY enumeration</span></span>

<span data-ttu-id="6155e-104">\[**H245 \_ La fonctionnalité** n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="6155e-104">\[**H245\_CAPABILITY** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6155e-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="6155e-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="6155e-106">L’énumération des **\_ capacités h245** décrit la prise en charge des formats audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="6155e-106">The **H245\_CAPABILITY** enum describes audio and video format support.</span></span>

## <a name="syntax"></a><span data-ttu-id="6155e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6155e-107">Syntax</span></span>


```C++
} H245_CAPABILITY;
```



## <a name="constants"></a><span data-ttu-id="6155e-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="6155e-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6155e-109"><span id="HC_G711"></span><span id="hc_g711"></span>**\_G711 hc**</span><span class="sxs-lookup"><span data-stu-id="6155e-109"><span id="HC_G711"></span><span id="hc_g711"></span>**HC\_G711**</span></span>
</dt> <dd>

<span data-ttu-id="6155e-110">Le protocole audio G. 711 est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6155e-110">The G.711 audio protocol is supported.</span></span>

</dd> <dt>

<span data-ttu-id="6155e-111"><span id="HC_G723"></span><span id="hc_g723"></span>**\_G723 hc**</span><span class="sxs-lookup"><span data-stu-id="6155e-111"><span id="HC_G723"></span><span id="hc_g723"></span>**HC\_G723**</span></span>
</dt> <dd>

<span data-ttu-id="6155e-112">Le protocole audio G. 723 est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6155e-112">The G.723 audio protocol is supported.</span></span>

</dd> <dt>

<span data-ttu-id="6155e-113"><span id="HC_H263QCIF"></span><span id="hc_h263qcif"></span>**\_H263QCIF hc**</span><span class="sxs-lookup"><span data-stu-id="6155e-113"><span id="HC_H263QCIF"></span><span id="hc_h263qcif"></span>**HC\_H263QCIF**</span></span>
</dt> <dd>

<span data-ttu-id="6155e-114">Le protocole vidéo H. 263 est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6155e-114">The H.263 video protocol is supported.</span></span>

</dd> <dt>

<span data-ttu-id="6155e-115"><span id="HC_H261QCIF"></span><span id="hc_h261qcif"></span>**\_H261QCIF hc**</span><span class="sxs-lookup"><span data-stu-id="6155e-115"><span id="HC_H261QCIF"></span><span id="hc_h261qcif"></span>**HC\_H261QCIF**</span></span>
</dt> <dd>

<span data-ttu-id="6155e-116">Le protocole vidéo H. 263 est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6155e-116">The H.263 video protocol is supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6155e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6155e-117">Requirements</span></span>



| <span data-ttu-id="6155e-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6155e-118">Requirement</span></span> | <span data-ttu-id="6155e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="6155e-119">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6155e-120">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="6155e-120">TAPI version</span></span><br/> | <span data-ttu-id="6155e-121">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="6155e-121">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="6155e-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="6155e-122">Header</span></span><br/>       | <dl> <span data-ttu-id="6155e-123"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="6155e-123"><dt>H323priv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6155e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6155e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6155e-125">**IH323LineEx::SetDefaultCapabilityPreferrence**</span><span class="sxs-lookup"><span data-stu-id="6155e-125">**IH323LineEx::SetDefaultCapabilityPreferrence**</span></span>](ih323lineex-setdefaultcapabilitypreferrence.md)
</dt> </dl>

 

 




