---
description: L’énumération TAPIControlFlags est utilisée par un certain nombre de méthodes pour indiquer si une propriété donnée est contrôlée automatiquement ou manuellement.
ms.assetid: 48259444-bf7b-4f0e-9068-2bdf89dde694
title: Énumération TAPIControlFlags (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07cc3e931c69a408d996fa28e6002b6c53c9df87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526412"
---
# <a name="tapicontrolflags-enumeration"></a><span data-ttu-id="c0364-103">Énumération TAPIControlFlags</span><span class="sxs-lookup"><span data-stu-id="c0364-103">TAPIControlFlags enumeration</span></span>

<span data-ttu-id="c0364-104">\[ Cette énumération n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="c0364-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c0364-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="c0364-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c0364-106">L’énumération **TAPIControlFlags** est utilisée par un certain nombre de méthodes pour indiquer si une propriété donnée est contrôlée automatiquement ou manuellement.</span><span class="sxs-lookup"><span data-stu-id="c0364-106">The **TAPIControlFlags** enum is used by a number of methods to indicate whether a given property is controlled automatically or manually.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0364-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0364-107">Syntax</span></span>


```C++
} TAPIControlFlags;
```



## <a name="constants"></a><span data-ttu-id="c0364-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="c0364-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c0364-109"><span id="TAPIControl_Flags_None"></span><span id="tapicontrol_flags_none"></span><span id="TAPICONTROL_FLAGS_NONE"></span>**\_Indicateurs TAPIControl \_ aucun**</span><span class="sxs-lookup"><span data-stu-id="c0364-109"><span id="TAPIControl_Flags_None"></span><span id="tapicontrol_flags_none"></span><span id="TAPICONTROL_FLAGS_NONE"></span>**TAPIControl\_Flags\_None**</span></span>
</dt> <dd>

<span data-ttu-id="c0364-110">L’interface TAPI n’a aucun indicateur de contrôle pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="c0364-110">TAPI has no control flags for the property.</span></span>

</dd> <dt>

<span data-ttu-id="c0364-111"><span id="TAPIControl_Flags_Auto"></span><span id="tapicontrol_flags_auto"></span><span id="TAPICONTROL_FLAGS_AUTO"></span>**TAPIControl les \_ indicateurs \_ automatiquement**</span><span class="sxs-lookup"><span data-stu-id="c0364-111"><span id="TAPIControl_Flags_Auto"></span><span id="tapicontrol_flags_auto"></span><span id="TAPICONTROL_FLAGS_AUTO"></span>**TAPIControl\_Flags\_Auto**</span></span>
</dt> <dd>

<span data-ttu-id="c0364-112">La propriété est contrôlée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="c0364-112">The property is controlled automatically.</span></span>

</dd> <dt>

<span data-ttu-id="c0364-113"><span id="TAPIControl_Flags_Manual"></span><span id="tapicontrol_flags_manual"></span><span id="TAPICONTROL_FLAGS_MANUAL"></span>**\_Manuel des indicateurs TAPIControl \_**</span><span class="sxs-lookup"><span data-stu-id="c0364-113"><span id="TAPIControl_Flags_Manual"></span><span id="tapicontrol_flags_manual"></span><span id="TAPICONTROL_FLAGS_MANUAL"></span>**TAPIControl\_Flags\_Manual**</span></span>
</dt> <dd>

<span data-ttu-id="c0364-114">La propriété est contrôlée manuellement.</span><span class="sxs-lookup"><span data-stu-id="c0364-114">The property is controlled manually.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c0364-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0364-115">Requirements</span></span>



| <span data-ttu-id="c0364-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0364-116">Requirement</span></span> | <span data-ttu-id="c0364-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0364-117">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c0364-118">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="c0364-118">TAPI version</span></span><br/> | <span data-ttu-id="c0364-119">Nécessite TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="c0364-119">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="c0364-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="c0364-120">Header</span></span><br/>       | <dl> <span data-ttu-id="c0364-121"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0364-121"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0364-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0364-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0364-123">**ITAudioDeviceControl :: GetRange**</span><span class="sxs-lookup"><span data-stu-id="c0364-123">**ITAudioDeviceControl::GetRange**</span></span>](itaudiodevicecontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="c0364-124">**ITAudioDeviceControl :: obtient**</span><span class="sxs-lookup"><span data-stu-id="c0364-124">**ITAudioDeviceControl::Get**</span></span>](itaudiodevicecontrol-get.md)
</dt> <dt>

[<span data-ttu-id="c0364-125">**ITAudioDeviceControl :: Set**</span><span class="sxs-lookup"><span data-stu-id="c0364-125">**ITAudioDeviceControl::Set**</span></span>](itaudiodevicecontrol-set.md)
</dt> <dt>

[<span data-ttu-id="c0364-126">**ITAudioSettings :: GetRange**</span><span class="sxs-lookup"><span data-stu-id="c0364-126">**ITAudioSettings::GetRange**</span></span>](itaudiosettings-getrange.md)
</dt> <dt>

[<span data-ttu-id="c0364-127">**ITAudioSettings :: obtient**</span><span class="sxs-lookup"><span data-stu-id="c0364-127">**ITAudioSettings::Get**</span></span>](itaudiosettings-get.md)
</dt> <dt>

[<span data-ttu-id="c0364-128">**ITAudioSettings :: Set**</span><span class="sxs-lookup"><span data-stu-id="c0364-128">**ITAudioSettings::Set**</span></span>](itaudiosettings-set.md)
</dt> <dt>

[<span data-ttu-id="c0364-129">**ITCallQualityControl :: GetRange**</span><span class="sxs-lookup"><span data-stu-id="c0364-129">**ITCallQualityControl::GetRange**</span></span>](itcallqualitycontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="c0364-130">**ITCallQualityControl :: obtient**</span><span class="sxs-lookup"><span data-stu-id="c0364-130">**ITCallQualityControl::Get**</span></span>](itcallqualitycontrol-get.md)
</dt> <dt>

[<span data-ttu-id="c0364-131">**ITCallQualityControl :: Set**</span><span class="sxs-lookup"><span data-stu-id="c0364-131">**ITCallQualityControl::Set**</span></span>](itcallqualitycontrol-set.md)
</dt> <dt>

[<span data-ttu-id="c0364-132">**ITStreamQualityControl :: GetRange**</span><span class="sxs-lookup"><span data-stu-id="c0364-132">**ITStreamQualityControl::GetRange**</span></span>](itstreamqualitycontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="c0364-133">**ITStreamQualityControl :: obtient**</span><span class="sxs-lookup"><span data-stu-id="c0364-133">**ITStreamQualityControl::Get**</span></span>](itstreamqualitycontrol-get.md)
</dt> <dt>

[<span data-ttu-id="c0364-134">**ITStreamQualityControl :: Set**</span><span class="sxs-lookup"><span data-stu-id="c0364-134">**ITStreamQualityControl::Set**</span></span>](itstreamqualitycontrol-set.md)
</dt> </dl>

 

 




