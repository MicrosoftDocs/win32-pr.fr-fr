---
description: La méthode GetRange récupère la plage de valeurs valides pour une propriété de paramètres audio donnée.
ms.assetid: 09ee0c59-6ae6-47eb-a8cf-6b24e759d7fb
title: 'ITAudioSettings :: GetRange, méthode (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91dd4d7bed3134c17de9c5958c7e6184cd51918e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523503"
---
# <a name="itaudiosettingsgetrange-method"></a><span data-ttu-id="79746-103">ITAudioSettings :: GetRange, méthode</span><span class="sxs-lookup"><span data-stu-id="79746-103">ITAudioSettings::GetRange method</span></span>

<span data-ttu-id="79746-104">\[ Cette méthode n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="79746-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="79746-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="79746-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="79746-106">La méthode **GetRange** récupère la plage de valeurs valides pour une [**propriété de paramètres audio**](audiosettingsproperty.md)donnée.</span><span class="sxs-lookup"><span data-stu-id="79746-106">The **GetRange** method retrieves the range of valid values for a given [**audio settings property**](audiosettingsproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="79746-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79746-107">Syntax</span></span>


```C++
HRESULT get_Terminal(
  [out] ITTerminal **ppTerminal
);
```



## <a name="parameters"></a><span data-ttu-id="79746-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79746-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79746-109">*Propriété* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="79746-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79746-110">Membre de l’énumération [**AudioSettingsProperty**](audiosettingsproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="79746-110">Member of the [**AudioSettingsProperty**](audiosettingsproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="79746-111">*plMin* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="79746-111">*plMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79746-112">Valeur minimale valide pour la propriété d’entrée.</span><span class="sxs-lookup"><span data-stu-id="79746-112">Minimum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="79746-113">*plMax* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="79746-113">*plMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79746-114">Valeur maximale valide pour la propriété d’entrée.</span><span class="sxs-lookup"><span data-stu-id="79746-114">Maximum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="79746-115">*plSteppingDelta* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="79746-115">*plSteppingDelta* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79746-116">Incrément par lequel la valeur de la propriété peut être augmentée ou diminuée.</span><span class="sxs-lookup"><span data-stu-id="79746-116">Increment by which the property value can be increased or decreased.</span></span>

</dd> <dt>

<span data-ttu-id="79746-117">*plDefault* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="79746-117">*plDefault* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79746-118">Valeur par défaut du paramètre de *propriété* .</span><span class="sxs-lookup"><span data-stu-id="79746-118">Default value for the *Property* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="79746-119">*plFlags* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="79746-119">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79746-120">Valeur de l’énumération [**TAPIControlFlags**](tapicontrolflags.md) indiquant comment la valeur de la *propriété* est contrôlée.</span><span class="sxs-lookup"><span data-stu-id="79746-120">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79746-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="79746-121">Return value</span></span>

<span data-ttu-id="79746-122">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="79746-122">This method can return one of these values.</span></span>



| <span data-ttu-id="79746-123">Code de retour</span><span class="sxs-lookup"><span data-stu-id="79746-123">Return code</span></span>                                                                                   | <span data-ttu-id="79746-124">Description</span><span class="sxs-lookup"><span data-stu-id="79746-124">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="79746-125"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="79746-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="79746-126">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="79746-126">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="79746-127"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="79746-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="79746-128">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="79746-128">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="79746-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79746-129">Requirements</span></span>



| <span data-ttu-id="79746-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79746-130">Requirement</span></span> | <span data-ttu-id="79746-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="79746-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="79746-132">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="79746-132">TAPI version</span></span><br/> | <span data-ttu-id="79746-133">Nécessite TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="79746-133">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="79746-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="79746-134">Header</span></span><br/>       | <dl> <span data-ttu-id="79746-135"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="79746-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="79746-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="79746-136">Library</span></span><br/>      | <dl> <span data-ttu-id="79746-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79746-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="79746-138">DLL</span><span class="sxs-lookup"><span data-stu-id="79746-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="79746-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79746-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79746-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79746-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79746-141">**ITAudioSettings**</span><span class="sxs-lookup"><span data-stu-id="79746-141">**ITAudioSettings**</span></span>](itaudiosettings.md)
</dt> <dt>

[<span data-ttu-id="79746-142">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="79746-142">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="79746-143">**AudioSettingsProperty**</span><span class="sxs-lookup"><span data-stu-id="79746-143">**AudioSettingsProperty**</span></span>](audiosettingsproperty.md)
</dt> </dl>

 

 




