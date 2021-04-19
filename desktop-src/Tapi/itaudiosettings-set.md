---
description: La méthode Set définit la valeur d’une propriété de paramètres audio donnée.
ms.assetid: 3132e004-5543-4b21-878d-35197f7077d6
title: 'ITAudioSettings :: Set, méthode (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf947c28d3b5270b3c5dabd4196d0e6b71f57911
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533183"
---
# <a name="itaudiosettingsset-method"></a><span data-ttu-id="8b021-103">ITAudioSettings :: Set, méthode</span><span class="sxs-lookup"><span data-stu-id="8b021-103">ITAudioSettings::Set method</span></span>

<span data-ttu-id="8b021-104">\[ Cette méthode n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="8b021-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8b021-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="8b021-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8b021-106">La méthode **Set** définit la valeur d’une [**propriété de paramètres audio**](audiosettingsproperty.md)donnée.</span><span class="sxs-lookup"><span data-stu-id="8b021-106">The **Set** method sets the value of a given [**audio settings property**](audiosettingsproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8b021-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b021-107">Syntax</span></span>


```C++
HRESULT get_Error(
  [out] HRESULT *phrErrorCode
);
```



## <a name="parameters"></a><span data-ttu-id="8b021-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b021-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b021-109">*Propriété* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8b021-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b021-110">Membre de l’énumération [**AudioSettingsProperty**](audiosettingsproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="8b021-110">Member of the [**AudioSettingsProperty**](audiosettingsproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="8b021-111">*lValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8b021-111">*lValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b021-112">Valeur souhaitée pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="8b021-112">Desired value for the property.</span></span>

</dd> <dt>

<span data-ttu-id="8b021-113">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8b021-113">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b021-114">Valeur de l’énumération [**TAPIControlFlags**](tapicontrolflags.md) indiquant comment la valeur de la *propriété* doit être contrôlée.</span><span class="sxs-lookup"><span data-stu-id="8b021-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is to be controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b021-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8b021-115">Return value</span></span>

<span data-ttu-id="8b021-116">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="8b021-116">This method can return one of these values.</span></span>



| <span data-ttu-id="8b021-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8b021-117">Return code</span></span>                                                                                   | <span data-ttu-id="8b021-118">Description</span><span class="sxs-lookup"><span data-stu-id="8b021-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="8b021-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8b021-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8b021-120">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="8b021-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8b021-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="8b021-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8b021-122">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="8b021-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8b021-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b021-123">Requirements</span></span>



| <span data-ttu-id="8b021-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b021-124">Requirement</span></span> | <span data-ttu-id="8b021-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b021-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8b021-126">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="8b021-126">TAPI version</span></span><br/> | <span data-ttu-id="8b021-127">Nécessite TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="8b021-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="8b021-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="8b021-128">Header</span></span><br/>       | <dl> <span data-ttu-id="8b021-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b021-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8b021-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8b021-130">Library</span></span><br/>      | <dl> <span data-ttu-id="8b021-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b021-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="8b021-132">DLL</span><span class="sxs-lookup"><span data-stu-id="8b021-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="8b021-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b021-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b021-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b021-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b021-135">**ITAudioSettings**</span><span class="sxs-lookup"><span data-stu-id="8b021-135">**ITAudioSettings**</span></span>](itaudiosettings.md)
</dt> <dt>

[<span data-ttu-id="8b021-136">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="8b021-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="8b021-137">**AudioSettingsProperty**</span><span class="sxs-lookup"><span data-stu-id="8b021-137">**AudioSettingsProperty**</span></span>](audiosettingsproperty.md)
</dt> </dl>

 

 




