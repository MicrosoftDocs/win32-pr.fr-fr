---
description: La méthode Set définit la valeur d’une propriété de qualité de flux donnée.
ms.assetid: 57029d1c-ac63-45c0-9d07-43c7b46a27b1
title: 'ITStreamQualityControl :: Set, méthode (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61deed4d6edc9b08d7c11fcc8d44d8cf91e11f99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540303"
---
# <a name="itstreamqualitycontrolset-method"></a><span data-ttu-id="8c3d9-103">ITStreamQualityControl :: Set, méthode</span><span class="sxs-lookup"><span data-stu-id="8c3d9-103">ITStreamQualityControl::Set method</span></span>

<span data-ttu-id="8c3d9-104">\[ Cette méthode n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="8c3d9-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8c3d9-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="8c3d9-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8c3d9-106">La méthode **Set** définit la valeur d’une [**propriété de qualité de flux**](streamqualityproperty.md)donnée.</span><span class="sxs-lookup"><span data-stu-id="8c3d9-106">The **Set** method sets the value of a given [**stream quality property**](streamqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8c3d9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c3d9-107">Syntax</span></span>


```C++
HRESULT Set(
  [in] StreamQualityProperty Property,
  [in] long                  lValue,
  [in] TAPIControlFlags      lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="8c3d9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c3d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c3d9-109">*Propriété* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8c3d9-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c3d9-110">Membre de l’énumération [**StreamQualityProperty**](streamqualityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="8c3d9-110">Member of the [**StreamQualityProperty**](streamqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="8c3d9-111">*lValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8c3d9-111">*lValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c3d9-112">Valeur souhaitée pour la *propriété* d’entrée.</span><span class="sxs-lookup"><span data-stu-id="8c3d9-112">Desired value for the input *Property*.</span></span>

</dd> <dt>

<span data-ttu-id="8c3d9-113">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8c3d9-113">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c3d9-114">Valeur de l’énumération [**TAPIControlFlags**](tapicontrolflags.md) indiquant comment la valeur de la *propriété* doit être contrôlée.</span><span class="sxs-lookup"><span data-stu-id="8c3d9-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is to be controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c3d9-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8c3d9-115">Return value</span></span>

<span data-ttu-id="8c3d9-116">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="8c3d9-116">This method can return one of these values.</span></span>



| <span data-ttu-id="8c3d9-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c3d9-117">Value</span></span>                                                                                         | <span data-ttu-id="8c3d9-118">Signification</span><span class="sxs-lookup"><span data-stu-id="8c3d9-118">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="8c3d9-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8c3d9-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8c3d9-120">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="8c3d9-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8c3d9-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="8c3d9-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8c3d9-122">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="8c3d9-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8c3d9-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c3d9-123">Requirements</span></span>



| <span data-ttu-id="8c3d9-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c3d9-124">Requirement</span></span> | <span data-ttu-id="8c3d9-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c3d9-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8c3d9-126">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="8c3d9-126">TAPI version</span></span><br/> | <span data-ttu-id="8c3d9-127">Nécessite TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="8c3d9-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="8c3d9-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c3d9-128">Header</span></span><br/>       | <dl> <span data-ttu-id="8c3d9-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c3d9-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8c3d9-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8c3d9-130">Library</span></span><br/>      | <dl> <span data-ttu-id="8c3d9-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c3d9-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="8c3d9-132">DLL</span><span class="sxs-lookup"><span data-stu-id="8c3d9-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="8c3d9-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c3d9-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c3d9-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c3d9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c3d9-135">**ITStreamQualityControl**</span><span class="sxs-lookup"><span data-stu-id="8c3d9-135">**ITStreamQualityControl**</span></span>](itstreamqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="8c3d9-136">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="8c3d9-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="8c3d9-137">**StreamQualityProperty**</span><span class="sxs-lookup"><span data-stu-id="8c3d9-137">**StreamQualityProperty**</span></span>](streamqualityproperty.md)
</dt> </dl>

 

 




