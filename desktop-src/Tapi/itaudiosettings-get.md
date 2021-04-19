---
description: La méthode obtenir récupère la valeur d’une propriété de paramètre audio donnée.
ms.assetid: 5ad9a4e8-c5b0-43e9-bf75-6460fd23501a
title: 'ITAudioSettings :: méthode d’extraction (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2773bf0f1a26978321ed0d02c3c30d8a96fef1c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540018"
---
# <a name="itaudiosettingsget-method"></a><span data-ttu-id="680c1-103">ITAudioSettings :: méthode d’extraction</span><span class="sxs-lookup"><span data-stu-id="680c1-103">ITAudioSettings::Get method</span></span>

<span data-ttu-id="680c1-104">\[ Cette méthode n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="680c1-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="680c1-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="680c1-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="680c1-106">La méthode **obtenir** récupère la valeur d’une propriété de [**paramètre audio**](audiosettingsproperty.md)donnée.</span><span class="sxs-lookup"><span data-stu-id="680c1-106">The **Get** method retrieves the value of a given [**audio setting property**](audiosettingsproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="680c1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="680c1-107">Syntax</span></span>


```C++
HRESULT get_Call(
  [out] ITCallInfo **ppCall
);
```



## <a name="parameters"></a><span data-ttu-id="680c1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="680c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="680c1-109">*Propriété* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="680c1-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="680c1-110">Membre de l’énumération [**AudioSettingsProperty**](audiosettingsproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="680c1-110">Member of the [**AudioSettingsProperty**](audiosettingsproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="680c1-111">*plValue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="680c1-111">*plValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="680c1-112">Valeur de la *propriété* d’entrée.</span><span class="sxs-lookup"><span data-stu-id="680c1-112">Value of the input *Property*.</span></span>

</dd> <dt>

<span data-ttu-id="680c1-113">*plFlags* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="680c1-113">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="680c1-114">Valeur de l’énumération [**TAPIControlFlags**](tapicontrolflags.md) indiquant comment la valeur de la *propriété* est contrôlée.</span><span class="sxs-lookup"><span data-stu-id="680c1-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="680c1-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="680c1-115">Return value</span></span>

<span data-ttu-id="680c1-116">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="680c1-116">This method can return one of these values.</span></span>



| <span data-ttu-id="680c1-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="680c1-117">Return code</span></span>                                                                                   | <span data-ttu-id="680c1-118">Description</span><span class="sxs-lookup"><span data-stu-id="680c1-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="680c1-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="680c1-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="680c1-120">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="680c1-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="680c1-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="680c1-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="680c1-122">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="680c1-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="680c1-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="680c1-123">Requirements</span></span>



| <span data-ttu-id="680c1-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="680c1-124">Requirement</span></span> | <span data-ttu-id="680c1-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="680c1-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="680c1-126">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="680c1-126">TAPI version</span></span><br/> | <span data-ttu-id="680c1-127">Nécessite TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="680c1-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="680c1-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="680c1-128">Header</span></span><br/>       | <dl> <span data-ttu-id="680c1-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="680c1-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="680c1-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="680c1-130">Library</span></span><br/>      | <dl> <span data-ttu-id="680c1-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="680c1-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="680c1-132">DLL</span><span class="sxs-lookup"><span data-stu-id="680c1-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="680c1-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="680c1-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="680c1-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="680c1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="680c1-135">**ITAudioSettings**</span><span class="sxs-lookup"><span data-stu-id="680c1-135">**ITAudioSettings**</span></span>](itaudiosettings.md)
</dt> <dt>

[<span data-ttu-id="680c1-136">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="680c1-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="680c1-137">**AudioSettingsProperty**</span><span class="sxs-lookup"><span data-stu-id="680c1-137">**AudioSettingsProperty**</span></span>](audiosettingsproperty.md)
</dt> </dl>

 

 




