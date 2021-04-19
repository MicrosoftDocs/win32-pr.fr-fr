---
description: La méthode obtenir récupère la valeur d’une propriété de qualité de flux donnée.
ms.assetid: a8b5b8c7-47c9-4561-be96-af8416d854dc
title: 'ITStreamQualityControl :: méthode d’extraction (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6758678dfacc8e0fe169189beaa8e890e801c907
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544019"
---
# <a name="itstreamqualitycontrolget-method"></a><span data-ttu-id="97fba-103">ITStreamQualityControl :: méthode d’extraction</span><span class="sxs-lookup"><span data-stu-id="97fba-103">ITStreamQualityControl::Get method</span></span>

<span data-ttu-id="97fba-104">\[ Cette méthode n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="97fba-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="97fba-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="97fba-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="97fba-106">La méthode **obtenir** récupère la valeur d’une propriété de [**qualité de flux**](streamqualityproperty.md)donnée.</span><span class="sxs-lookup"><span data-stu-id="97fba-106">The **Get** method retrieves the value of a given [**stream quality property**](streamqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="97fba-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97fba-107">Syntax</span></span>


```C++
HRESULT Get(
  [in]  StreamQualityProperty Property,
  [out] long                  *plValue,
  [out] TAPIControlFlags      *plFlags
);
```



## <a name="parameters"></a><span data-ttu-id="97fba-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97fba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97fba-109">*Propriété* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97fba-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97fba-110">Membre de l’énumération [**StreamQualityProperty**](streamqualityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="97fba-110">Member of the [**StreamQualityProperty**](streamqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="97fba-111">*plValue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="97fba-111">*plValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97fba-112">Valeur de la *propriété* d’entrée.</span><span class="sxs-lookup"><span data-stu-id="97fba-112">Value of the input *Property*.</span></span>

</dd> <dt>

<span data-ttu-id="97fba-113">*plFlags* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="97fba-113">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97fba-114">Valeur de l’énumération [**TAPIControlFlags**](tapicontrolflags.md) indiquant comment la valeur de la *propriété* est contrôlée.</span><span class="sxs-lookup"><span data-stu-id="97fba-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97fba-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="97fba-115">Return value</span></span>

<span data-ttu-id="97fba-116">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="97fba-116">This method can return one of these values.</span></span>



| <span data-ttu-id="97fba-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="97fba-117">Return code</span></span>                                                                                   | <span data-ttu-id="97fba-118">Description</span><span class="sxs-lookup"><span data-stu-id="97fba-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="97fba-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="97fba-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="97fba-120">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="97fba-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="97fba-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="97fba-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="97fba-122">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="97fba-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="97fba-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97fba-123">Requirements</span></span>



| <span data-ttu-id="97fba-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97fba-124">Requirement</span></span> | <span data-ttu-id="97fba-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="97fba-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="97fba-126">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="97fba-126">TAPI version</span></span><br/> | <span data-ttu-id="97fba-127">Nécessite TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="97fba-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="97fba-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="97fba-128">Header</span></span><br/>       | <dl> <span data-ttu-id="97fba-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="97fba-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="97fba-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="97fba-130">Library</span></span><br/>      | <dl> <span data-ttu-id="97fba-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="97fba-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="97fba-132">DLL</span><span class="sxs-lookup"><span data-stu-id="97fba-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="97fba-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97fba-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97fba-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97fba-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97fba-135">**ITStreamQualityControl**</span><span class="sxs-lookup"><span data-stu-id="97fba-135">**ITStreamQualityControl**</span></span>](itstreamqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="97fba-136">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="97fba-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="97fba-137">**StreamQualityProperty**</span><span class="sxs-lookup"><span data-stu-id="97fba-137">**StreamQualityProperty**</span></span>](streamqualityproperty.md)
</dt> </dl>

 

 




