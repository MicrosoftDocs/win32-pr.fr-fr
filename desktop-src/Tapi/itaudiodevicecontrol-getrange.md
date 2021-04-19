---
description: La méthode GetRange récupère la plage de valeurs valides pour une propriété de périphérique audio donnée.
ms.assetid: df8985f4-8153-4f32-a90c-a5eb7c76b3c7
title: 'ITAudioDeviceControl :: GetRange, méthode (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cbf5bf36d4ec754440e1612f2e228c495d165c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532768"
---
# <a name="itaudiodevicecontrolgetrange-method"></a><span data-ttu-id="17f63-103">ITAudioDeviceControl :: GetRange, méthode</span><span class="sxs-lookup"><span data-stu-id="17f63-103">ITAudioDeviceControl::GetRange method</span></span>

<span data-ttu-id="17f63-104">\[ Cette méthode n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="17f63-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="17f63-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="17f63-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="17f63-106">La méthode **GetRange** récupère la plage de valeurs valides pour une [**propriété de périphérique audio**](audiodeviceproperty.md)donnée.</span><span class="sxs-lookup"><span data-stu-id="17f63-106">The **GetRange** method retrieves the range of valid values for a given [**audio device property**](audiodeviceproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="17f63-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17f63-107">Syntax</span></span>


```C++
HRESULT get_Terminal(
  [out] ITTerminal **ppTerminal
);
```



## <a name="parameters"></a><span data-ttu-id="17f63-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17f63-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17f63-109">*Propriété* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="17f63-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17f63-110">Membre de l’énumération [**AudioDeviceProperty**](audiodeviceproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="17f63-110">Member of the [**AudioDeviceProperty**](audiodeviceproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="17f63-111">*plMin* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="17f63-111">*plMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17f63-112">Valeur minimale valide pour la propriété d’entrée.</span><span class="sxs-lookup"><span data-stu-id="17f63-112">Minimum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="17f63-113">*plMax* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="17f63-113">*plMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17f63-114">Valeur maximale valide pour la propriété d’entrée.</span><span class="sxs-lookup"><span data-stu-id="17f63-114">Maximum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="17f63-115">*plSteppingDelta* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="17f63-115">*plSteppingDelta* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17f63-116">Incrément par lequel la valeur de la propriété peut être augmentée ou diminuée.</span><span class="sxs-lookup"><span data-stu-id="17f63-116">Increment by which the property value can be increased or decreased.</span></span>

</dd> <dt>

<span data-ttu-id="17f63-117">*plDefault* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="17f63-117">*plDefault* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17f63-118">Valeur par défaut du paramètre de *propriété* .</span><span class="sxs-lookup"><span data-stu-id="17f63-118">Default value for the *Property* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="17f63-119">*plFlags* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="17f63-119">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17f63-120">Valeur de l’énumération [**TAPIControlFlags**](tapicontrolflags.md) indiquant comment la valeur de la *propriété* est contrôlée.</span><span class="sxs-lookup"><span data-stu-id="17f63-120">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17f63-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="17f63-121">Return value</span></span>

<span data-ttu-id="17f63-122">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="17f63-122">This method can return one of these values.</span></span>



| <span data-ttu-id="17f63-123">Code de retour</span><span class="sxs-lookup"><span data-stu-id="17f63-123">Return code</span></span>                                                                                   | <span data-ttu-id="17f63-124">Description</span><span class="sxs-lookup"><span data-stu-id="17f63-124">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="17f63-125"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="17f63-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="17f63-126">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="17f63-126">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="17f63-127"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="17f63-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="17f63-128">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="17f63-128">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="17f63-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17f63-129">Requirements</span></span>



| <span data-ttu-id="17f63-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17f63-130">Requirement</span></span> | <span data-ttu-id="17f63-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="17f63-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="17f63-132">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="17f63-132">TAPI version</span></span><br/> | <span data-ttu-id="17f63-133">Nécessite TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="17f63-133">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="17f63-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="17f63-134">Header</span></span><br/>       | <dl> <span data-ttu-id="17f63-135"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="17f63-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="17f63-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="17f63-136">Library</span></span><br/>      | <dl> <span data-ttu-id="17f63-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17f63-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="17f63-138">DLL</span><span class="sxs-lookup"><span data-stu-id="17f63-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="17f63-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17f63-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17f63-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17f63-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17f63-141">**ITAudioDeviceControl**</span><span class="sxs-lookup"><span data-stu-id="17f63-141">**ITAudioDeviceControl**</span></span>](itaudiodevicecontrol.md)
</dt> <dt>

[<span data-ttu-id="17f63-142">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="17f63-142">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="17f63-143">**AudioDeviceProperty**</span><span class="sxs-lookup"><span data-stu-id="17f63-143">**AudioDeviceProperty**</span></span>](audiodeviceproperty.md)
</dt> </dl>

 

 




