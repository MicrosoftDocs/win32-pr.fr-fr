---
description: 'L’énumération CallQualityProperty est utilisée par les méthodes ITCallQualityControl :: GetRange, ITCallQualityControl :: obten et ITCallQualityControl :: Set pour indiquer que la propriété de qualité d’appel est traitée.'
ms.assetid: d9a04cc4-9b7d-4b01-918f-e4938c172b8e
title: Énumération CallQualityProperty (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2ca3af31e0b85a443bb34ac1992b3d3b5c89bfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537539"
---
# <a name="callqualityproperty-enumeration"></a><span data-ttu-id="8f168-103">Énumération CallQualityProperty</span><span class="sxs-lookup"><span data-stu-id="8f168-103">CallQualityProperty enumeration</span></span>

<span data-ttu-id="8f168-104">\[ Cette énumération n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="8f168-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8f168-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="8f168-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8f168-106">L’énumération **CallQualityProperty** est utilisée par les méthodes [**ITCallQualityControl :: GetRange**](itcallqualitycontrol-getrange.md), [**ITCallQualityControl :: obten**](itcallqualitycontrol-get.md)et [**ITCallQualityControl :: Set**](itcallqualitycontrol-set.md) pour indiquer que la propriété de qualité d’appel est traitée.</span><span class="sxs-lookup"><span data-stu-id="8f168-106">The **CallQualityProperty** enum is used by the [**ITCallQualityControl::GetRange**](itcallqualitycontrol-getrange.md), [**ITCallQualityControl::Get**](itcallqualitycontrol-get.md), and [**ITCallQualityControl::Set**](itcallqualitycontrol-set.md) methods to indicate the call quality property being addressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f168-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8f168-107">Syntax</span></span>


```C++
} CallQualityProperty;
```



## <a name="constants"></a><span data-ttu-id="8f168-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="8f168-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8f168-109"><span id="CallQuality_ControlInterval"></span><span id="callquality_controlinterval"></span><span id="CALLQUALITY_CONTROLINTERVAL"></span>**CallQuality \_ ControlInterval**</span><span class="sxs-lookup"><span data-stu-id="8f168-109"><span id="CallQuality_ControlInterval"></span><span id="callquality_controlinterval"></span><span id="CALLQUALITY_CONTROLINTERVAL"></span>**CallQuality\_ControlInterval**</span></span>
</dt> <dd>

<span data-ttu-id="8f168-110">Intervalle de contrôle.</span><span class="sxs-lookup"><span data-stu-id="8f168-110">Control interval.</span></span>

</dd> <dt>

<span data-ttu-id="8f168-111"><span id="CallQuality_ConfBitrate"></span><span id="callquality_confbitrate"></span><span id="CALLQUALITY_CONFBITRATE"></span>**CallQuality \_ ConfBitrate**</span><span class="sxs-lookup"><span data-stu-id="8f168-111"><span id="CallQuality_ConfBitrate"></span><span id="callquality_confbitrate"></span><span id="CALLQUALITY_CONFBITRATE"></span>**CallQuality\_ConfBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="8f168-112">Vitesse de transmission de la Conférence.</span><span class="sxs-lookup"><span data-stu-id="8f168-112">Bit rate for conference.</span></span>

</dd> <dt>

<span data-ttu-id="8f168-113"><span id="CallQuality_MaxInputBitrate"></span><span id="callquality_maxinputbitrate"></span><span id="CALLQUALITY_MAXINPUTBITRATE"></span>**CallQuality \_ MaxInputBitrate**</span><span class="sxs-lookup"><span data-stu-id="8f168-113"><span id="CallQuality_MaxInputBitrate"></span><span id="callquality_maxinputbitrate"></span><span id="CALLQUALITY_MAXINPUTBITRATE"></span>**CallQuality\_MaxInputBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="8f168-114">Débit d’entrée maximal.</span><span class="sxs-lookup"><span data-stu-id="8f168-114">Maximum input bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="8f168-115"><span id="CallQuality_CurrInputBitrate"></span><span id="callquality_currinputbitrate"></span><span id="CALLQUALITY_CURRINPUTBITRATE"></span>**CallQuality \_ CurrInputBitrate**</span><span class="sxs-lookup"><span data-stu-id="8f168-115"><span id="CallQuality_CurrInputBitrate"></span><span id="callquality_currinputbitrate"></span><span id="CALLQUALITY_CURRINPUTBITRATE"></span>**CallQuality\_CurrInputBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="8f168-116">Vitesse d’entrée actuelle.</span><span class="sxs-lookup"><span data-stu-id="8f168-116">Current input bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="8f168-117"><span id="CallQuality_MaxOutputBitrate"></span><span id="callquality_maxoutputbitrate"></span><span id="CALLQUALITY_MAXOUTPUTBITRATE"></span>**CallQuality \_ MaxOutputBitrate**</span><span class="sxs-lookup"><span data-stu-id="8f168-117"><span id="CallQuality_MaxOutputBitrate"></span><span id="callquality_maxoutputbitrate"></span><span id="CALLQUALITY_MAXOUTPUTBITRATE"></span>**CallQuality\_MaxOutputBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="8f168-118">Vitesse de transmission maximale.</span><span class="sxs-lookup"><span data-stu-id="8f168-118">Maximum output bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="8f168-119"><span id="CallQuality_CurrOutputBitrate"></span><span id="callquality_curroutputbitrate"></span><span id="CALLQUALITY_CURROUTPUTBITRATE"></span>**CallQuality \_ CurrOutputBitrate**</span><span class="sxs-lookup"><span data-stu-id="8f168-119"><span id="CallQuality_CurrOutputBitrate"></span><span id="callquality_curroutputbitrate"></span><span id="CALLQUALITY_CURROUTPUTBITRATE"></span>**CallQuality\_CurrOutputBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="8f168-120">Vitesse de transmission en sortie actuelle.</span><span class="sxs-lookup"><span data-stu-id="8f168-120">Current output bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="8f168-121"><span id="CallQuality_MaxCPULoad"></span><span id="callquality_maxcpuload"></span><span id="CALLQUALITY_MAXCPULOAD"></span>**CallQuality \_ MaxCPULoad**</span><span class="sxs-lookup"><span data-stu-id="8f168-121"><span id="CallQuality_MaxCPULoad"></span><span id="callquality_maxcpuload"></span><span id="CALLQUALITY_MAXCPULOAD"></span>**CallQuality\_MaxCPULoad**</span></span>
</dt> <dd>

<span data-ttu-id="8f168-122">Charge de l’UC maximale.</span><span class="sxs-lookup"><span data-stu-id="8f168-122">Maximum CPU load.</span></span>

</dd> <dt>

<span data-ttu-id="8f168-123"><span id="CallQuality_CurrCPULoad"></span><span id="callquality_currcpuload"></span><span id="CALLQUALITY_CURRCPULOAD"></span>**CallQuality \_ CurrCPULoad**</span><span class="sxs-lookup"><span data-stu-id="8f168-123"><span id="CallQuality_CurrCPULoad"></span><span id="callquality_currcpuload"></span><span id="CALLQUALITY_CURRCPULOAD"></span>**CallQuality\_CurrCPULoad**</span></span>
</dt> <dd>

<span data-ttu-id="8f168-124">Charge de l’UC actuelle.</span><span class="sxs-lookup"><span data-stu-id="8f168-124">Current CPU load.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8f168-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f168-125">Requirements</span></span>



| <span data-ttu-id="8f168-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f168-126">Requirement</span></span> | <span data-ttu-id="8f168-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f168-127">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8f168-128">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="8f168-128">TAPI version</span></span><br/> | <span data-ttu-id="8f168-129">Nécessite TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="8f168-129">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="8f168-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="8f168-130">Header</span></span><br/>       | <dl> <span data-ttu-id="8f168-131"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f168-131"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f168-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f168-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f168-133">**ITCallQualityControl :: GetRange**</span><span class="sxs-lookup"><span data-stu-id="8f168-133">**ITCallQualityControl::GetRange**</span></span>](itcallqualitycontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="8f168-134">**ITCallQualityControl :: obtient**</span><span class="sxs-lookup"><span data-stu-id="8f168-134">**ITCallQualityControl::Get**</span></span>](itcallqualitycontrol-get.md)
</dt> <dt>

[<span data-ttu-id="8f168-135">**ITCallQualityControl :: Set**</span><span class="sxs-lookup"><span data-stu-id="8f168-135">**ITCallQualityControl::Set**</span></span>](itcallqualitycontrol-set.md)
</dt> </dl>

 

 




