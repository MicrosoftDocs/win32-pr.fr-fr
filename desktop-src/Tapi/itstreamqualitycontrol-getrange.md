---
description: La méthode GetRange obtient la plage de valeurs valides pour une propriété de qualité de flux donnée.
ms.assetid: 8c5e4652-1a40-4d7d-aa89-606e979dc03d
title: 'ITStreamQualityControl :: GetRange, méthode (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bea8b20c2617eb0fe54ccc4603997464fca25f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538773"
---
# <a name="itstreamqualitycontrolgetrange-method"></a><span data-ttu-id="3a0fb-103">ITStreamQualityControl :: GetRange, méthode</span><span class="sxs-lookup"><span data-stu-id="3a0fb-103">ITStreamQualityControl::GetRange method</span></span>

<span data-ttu-id="3a0fb-104">\[ Cette méthode n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="3a0fb-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3a0fb-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="3a0fb-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="3a0fb-106">La méthode **GetRange** obtient la plage de valeurs valides pour une [**propriété de qualité de flux**](streamqualityproperty.md)donnée.</span><span class="sxs-lookup"><span data-stu-id="3a0fb-106">The **GetRange** method gets the range of valid values for a given [**stream quality property**](streamqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3a0fb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a0fb-107">Syntax</span></span>


```C++
HRESULT GetRange(
  [in]  StreamQualityProperty Property,
  [out] long                  *plMin,
  [out] long                  *plMax,
  [out] long                  *plSteppingDelta,
  [out] long                  *plDefault,
  [out] TAPIControlFlags      *plFlags
);
```



## <a name="parameters"></a><span data-ttu-id="3a0fb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3a0fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a0fb-109">*Propriété* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3a0fb-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a0fb-110">Membre de l’énumération [**StreamQualityProperty**](streamqualityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="3a0fb-110">Member of the [**StreamQualityProperty**](streamqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="3a0fb-111">*plMin* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3a0fb-111">*plMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a0fb-112">Valeur minimale valide pour la propriété d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3a0fb-112">Minimum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="3a0fb-113">*plMax* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3a0fb-113">*plMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a0fb-114">Valeur maximale valide pour la propriété d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3a0fb-114">Maximum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="3a0fb-115">*plSteppingDelta* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3a0fb-115">*plSteppingDelta* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a0fb-116">Incrément par lequel la valeur de la propriété peut être augmentée ou diminuée.</span><span class="sxs-lookup"><span data-stu-id="3a0fb-116">Increment by which the property value can be increased or decreased.</span></span>

</dd> <dt>

<span data-ttu-id="3a0fb-117">*plDefault* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3a0fb-117">*plDefault* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a0fb-118">Valeur par défaut du paramètre de *propriété* .</span><span class="sxs-lookup"><span data-stu-id="3a0fb-118">Default value for the *Property* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3a0fb-119">*plFlags* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3a0fb-119">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a0fb-120">Valeur de l’énumération [**TAPIControlFlags**](tapicontrolflags.md) indiquant comment la valeur de la *propriété* est contrôlée.</span><span class="sxs-lookup"><span data-stu-id="3a0fb-120">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a0fb-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3a0fb-121">Return value</span></span>

<span data-ttu-id="3a0fb-122">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="3a0fb-122">This method can return one of these values.</span></span>



| <span data-ttu-id="3a0fb-123">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3a0fb-123">Return code</span></span>                                                                                   | <span data-ttu-id="3a0fb-124">Description</span><span class="sxs-lookup"><span data-stu-id="3a0fb-124">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="3a0fb-125"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3a0fb-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3a0fb-126">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="3a0fb-126">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3a0fb-127"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="3a0fb-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3a0fb-128">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="3a0fb-128">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3a0fb-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a0fb-129">Requirements</span></span>



| <span data-ttu-id="3a0fb-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a0fb-130">Requirement</span></span> | <span data-ttu-id="3a0fb-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a0fb-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3a0fb-132">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="3a0fb-132">TAPI version</span></span><br/> | <span data-ttu-id="3a0fb-133">Nécessite TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="3a0fb-133">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="3a0fb-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="3a0fb-134">Header</span></span><br/>       | <dl> <span data-ttu-id="3a0fb-135"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a0fb-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3a0fb-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3a0fb-136">Library</span></span><br/>      | <dl> <span data-ttu-id="3a0fb-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a0fb-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="3a0fb-138">DLL</span><span class="sxs-lookup"><span data-stu-id="3a0fb-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="3a0fb-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a0fb-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a0fb-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a0fb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a0fb-141">**ITStreamQualityControl**</span><span class="sxs-lookup"><span data-stu-id="3a0fb-141">**ITStreamQualityControl**</span></span>](itstreamqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="3a0fb-142">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="3a0fb-142">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="3a0fb-143">**StreamQualityProperty**</span><span class="sxs-lookup"><span data-stu-id="3a0fb-143">**StreamQualityProperty**</span></span>](streamqualityproperty.md)
</dt> </dl>

 

 




