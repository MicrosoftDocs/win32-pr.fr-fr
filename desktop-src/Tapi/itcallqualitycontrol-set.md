---
description: La méthode Set définit la valeur d’une propriété de contrôle de qualité d’appel donnée.
ms.assetid: e83ed9d7-0a53-4555-ae44-737ab3dfb749
title: 'ITCallQualityControl :: Set, méthode (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0c0a83702ba0dd4d04eb129eeed95c46d2a79a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532224"
---
# <a name="itcallqualitycontrolset-method"></a><span data-ttu-id="237ee-103">ITCallQualityControl :: Set, méthode</span><span class="sxs-lookup"><span data-stu-id="237ee-103">ITCallQualityControl::Set method</span></span>

<span data-ttu-id="237ee-104">\[ Cette méthode n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="237ee-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="237ee-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="237ee-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="237ee-106">La méthode **Set** définit la valeur d’une [propriété de contrôle de qualité d’appel](callqualityproperty.md)donnée.</span><span class="sxs-lookup"><span data-stu-id="237ee-106">The **Set** method sets the value of a given [call quality control property](callqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="237ee-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="237ee-107">Syntax</span></span>


```C++
HRESULT Set(
  [in] CallQualityProperty Property,
  [in] long                lValue,
  [in] TAPIControlFlags    lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="237ee-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="237ee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="237ee-109">*Propriété* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="237ee-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="237ee-110">Membre de l’énumération [**CallQualityProperty**](callqualityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="237ee-110">Member of the [**CallQualityProperty**](callqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="237ee-111">*lValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="237ee-111">*lValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="237ee-112">Valeur souhaitée pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="237ee-112">Desired value for the property.</span></span>

</dd> <dt>

<span data-ttu-id="237ee-113">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="237ee-113">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="237ee-114">Valeur de l’énumération [**TAPIControlFlags**](tapicontrolflags.md) indiquant comment la valeur de la *propriété* doit être contrôlée.</span><span class="sxs-lookup"><span data-stu-id="237ee-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is to be controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="237ee-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="237ee-115">Return value</span></span>

<span data-ttu-id="237ee-116">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="237ee-116">This method can return one of these values.</span></span>



| <span data-ttu-id="237ee-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="237ee-117">Return code</span></span>                                                                                   | <span data-ttu-id="237ee-118">Description</span><span class="sxs-lookup"><span data-stu-id="237ee-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="237ee-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="237ee-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="237ee-120">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="237ee-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="237ee-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="237ee-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="237ee-122">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="237ee-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="237ee-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="237ee-123">Requirements</span></span>



| <span data-ttu-id="237ee-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="237ee-124">Requirement</span></span> | <span data-ttu-id="237ee-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="237ee-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="237ee-126">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="237ee-126">TAPI version</span></span><br/> | <span data-ttu-id="237ee-127">Nécessite TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="237ee-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="237ee-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="237ee-128">Header</span></span><br/>       | <dl> <span data-ttu-id="237ee-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="237ee-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="237ee-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="237ee-130">Library</span></span><br/>      | <dl> <span data-ttu-id="237ee-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="237ee-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="237ee-132">DLL</span><span class="sxs-lookup"><span data-stu-id="237ee-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="237ee-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="237ee-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="237ee-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="237ee-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="237ee-135">**ITCallQualityControl**</span><span class="sxs-lookup"><span data-stu-id="237ee-135">**ITCallQualityControl**</span></span>](itcallqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="237ee-136">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="237ee-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="237ee-137">**CallQualityProperty**</span><span class="sxs-lookup"><span data-stu-id="237ee-137">**CallQualityProperty**</span></span>](callqualityproperty.md)
</dt> </dl>

 

 




