---
description: 'Énumération StreamQualityProperty utilisée par les méthodes ITStreamQualityControl :: GetRange, ITStreamQualityControl :: obten et ITStreamQualityControl :: Set pour indiquer la propriété de qualité du flux qui est adressé.'
ms.assetid: 28c9257f-6fbb-440f-9b84-c15a74229b5b
title: Énumération StreamQualityProperty (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f552641cd0847bb3ff8eec9d528a03171a78c2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523457"
---
# <a name="streamqualityproperty-enumeration"></a><span data-ttu-id="4fbb4-103">Énumération StreamQualityProperty</span><span class="sxs-lookup"><span data-stu-id="4fbb4-103">StreamQualityProperty enumeration</span></span>

<span data-ttu-id="4fbb4-104">\[ Cette énumération n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="4fbb4-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4fbb4-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="4fbb4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4fbb4-106">Énumération **StreamQualityProperty** utilisée par les méthodes [**ITStreamQualityControl :: GetRange**](itstreamqualitycontrol-getrange.md), [**ITStreamQualityControl :: obten**](itstreamqualitycontrol-get.md)et [**ITStreamQualityControl :: Set**](itstreamqualitycontrol-set.md) pour indiquer la propriété de qualité du flux qui est adressé.</span><span class="sxs-lookup"><span data-stu-id="4fbb4-106">The **StreamQualityProperty** enum used by the [**ITStreamQualityControl::GetRange**](itstreamqualitycontrol-getrange.md), [**ITStreamQualityControl::Get**](itstreamqualitycontrol-get.md), and [**ITStreamQualityControl::Set**](itstreamqualitycontrol-set.md) methods to indicate the stream quality property being addressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fbb4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4fbb4-107">Syntax</span></span>


```C++
} StreamQualityProperty;
```



## <a name="constants"></a><span data-ttu-id="4fbb4-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="4fbb4-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4fbb4-109"><span id="StreamQuality_MaxBitrate"></span><span id="streamquality_maxbitrate"></span><span id="STREAMQUALITY_MAXBITRATE"></span>**StreamQuality \_ MaxBitrate**</span><span class="sxs-lookup"><span data-stu-id="4fbb4-109"><span id="StreamQuality_MaxBitrate"></span><span id="streamquality_maxbitrate"></span><span id="STREAMQUALITY_MAXBITRATE"></span>**StreamQuality\_MaxBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="4fbb4-110">Vitesse de transmission maximale.</span><span class="sxs-lookup"><span data-stu-id="4fbb4-110">Maximum bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="4fbb4-111"><span id="StreamQuality_CurrBitrate"></span><span id="streamquality_currbitrate"></span><span id="STREAMQUALITY_CURRBITRATE"></span>**StreamQuality \_ CurrBitrate**</span><span class="sxs-lookup"><span data-stu-id="4fbb4-111"><span id="StreamQuality_CurrBitrate"></span><span id="streamquality_currbitrate"></span><span id="STREAMQUALITY_CURRBITRATE"></span>**StreamQuality\_CurrBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="4fbb4-112">Vitesse de transmission minimale.</span><span class="sxs-lookup"><span data-stu-id="4fbb4-112">Minimum bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="4fbb4-113"><span id="StreamQuality_MinFrameInterval"></span><span id="streamquality_minframeinterval"></span><span id="STREAMQUALITY_MINFRAMEINTERVAL"></span>**StreamQuality \_ MinFrameInterval**</span><span class="sxs-lookup"><span data-stu-id="4fbb4-113"><span id="StreamQuality_MinFrameInterval"></span><span id="streamquality_minframeinterval"></span><span id="STREAMQUALITY_MINFRAMEINTERVAL"></span>**StreamQuality\_MinFrameInterval**</span></span>
</dt> <dd>

<span data-ttu-id="4fbb4-114">Intervalle de trames maximal.</span><span class="sxs-lookup"><span data-stu-id="4fbb4-114">Maximum frame interval.</span></span>

</dd> <dt>

<span data-ttu-id="4fbb4-115"><span id="StreamQuality_AvgFrameInterval"></span><span id="streamquality_avgframeinterval"></span><span id="STREAMQUALITY_AVGFRAMEINTERVAL"></span>**StreamQuality \_ AvgFrameInterval**</span><span class="sxs-lookup"><span data-stu-id="4fbb4-115"><span id="StreamQuality_AvgFrameInterval"></span><span id="streamquality_avgframeinterval"></span><span id="STREAMQUALITY_AVGFRAMEINTERVAL"></span>**StreamQuality\_AvgFrameInterval**</span></span>
</dt> <dd>

<span data-ttu-id="4fbb4-116">Intervalle de frame minimal.</span><span class="sxs-lookup"><span data-stu-id="4fbb4-116">Minimum frame interval.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4fbb4-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4fbb4-117">Requirements</span></span>



| <span data-ttu-id="4fbb4-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4fbb4-118">Requirement</span></span> | <span data-ttu-id="4fbb4-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="4fbb4-119">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4fbb4-120">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="4fbb4-120">TAPI version</span></span><br/> | <span data-ttu-id="4fbb4-121">Nécessite TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="4fbb4-121">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="4fbb4-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="4fbb4-122">Header</span></span><br/>       | <dl> <span data-ttu-id="4fbb4-123"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fbb4-123"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fbb4-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fbb4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fbb4-125">**ITStreamQualityControl :: GetRange**</span><span class="sxs-lookup"><span data-stu-id="4fbb4-125">**ITStreamQualityControl::GetRange**</span></span>](itstreamqualitycontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="4fbb4-126">**ITStreamQualityControl :: obtient**</span><span class="sxs-lookup"><span data-stu-id="4fbb4-126">**ITStreamQualityControl::Get**</span></span>](itstreamqualitycontrol-get.md)
</dt> <dt>

[<span data-ttu-id="4fbb4-127">**ITStreamQualityControl :: Set**</span><span class="sxs-lookup"><span data-stu-id="4fbb4-127">**ITStreamQualityControl::Set**</span></span>](itstreamqualitycontrol-set.md)
</dt> </dl>

 

 




