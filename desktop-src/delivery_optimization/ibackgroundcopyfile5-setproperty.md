---
title: IBackgroundCopyFile5 SetProperty, méthode (Deliveryoptimization. h)
description: Définit une propriété générique d’un transfert de fichiers d’optimisation de la remise.
ms.assetid: 63B6806E-47D6-49B0-9867-628C110540D0
keywords:
- SetProperty (méthode)
- SetProperty, méthode, interface IBackgroundCopyFile5
- Interface IBackgroundCopyFile5, méthode SetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f519ee77af0ae6e0c3d1d036aeeb6a8ad712870
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942035"
---
# <a name="ibackgroundcopyfile5setproperty-method"></a><span data-ttu-id="d7e6e-106">IBackgroundCopyFile5 :: SetProperty, méthode</span><span class="sxs-lookup"><span data-stu-id="d7e6e-106">IBackgroundCopyFile5::SetProperty method</span></span>

<span data-ttu-id="d7e6e-107">Définit une propriété générique d’un transfert de fichiers d’optimisation de la remise.</span><span class="sxs-lookup"><span data-stu-id="d7e6e-107">Sets a generic property of a Delivery Optimization (DO) file transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7e6e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7e6e-108">Syntax</span></span>


```C++
HRESULT SetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *ProertyValue
);
```



## <a name="parameters"></a><span data-ttu-id="d7e6e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7e6e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7e6e-110">*PropertyId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d7e6e-110">*PropertyId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7e6e-111">Spécifie la propriété à définir.</span><span class="sxs-lookup"><span data-stu-id="d7e6e-111">Specifies the property to be set.</span></span>

</dd> <dt>

<span data-ttu-id="d7e6e-112">*ProertyValue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d7e6e-112">*ProertyValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7e6e-113">Pointeur vers une Union qui spécifie la valeur à définir.</span><span class="sxs-lookup"><span data-stu-id="d7e6e-113">A pointer to a union that specifies the value to be set.</span></span> <span data-ttu-id="d7e6e-114">Le membre d’Union approprié pour l’ID de propriété est utilisé.</span><span class="sxs-lookup"><span data-stu-id="d7e6e-114">The union member appropriate for the property ID is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7e6e-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d7e6e-115">Return value</span></span>

<span data-ttu-id="d7e6e-116">Si cette méthode est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="d7e6e-116">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="d7e6e-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d7e6e-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7e6e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7e6e-118">Requirements</span></span>



| <span data-ttu-id="d7e6e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7e6e-119">Requirement</span></span> | <span data-ttu-id="d7e6e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7e6e-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7e6e-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7e6e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d7e6e-122">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7e6e-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d7e6e-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7e6e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d7e6e-124">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7e6e-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d7e6e-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7e6e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7e6e-126"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7e6e-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="d7e6e-127">MIDL</span><span class="sxs-lookup"><span data-stu-id="d7e6e-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d7e6e-128"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d7e6e-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="d7e6e-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d7e6e-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="d7e6e-130"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7e6e-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="d7e6e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d7e6e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7e6e-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7e6e-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="d7e6e-133">IID</span><span class="sxs-lookup"><span data-stu-id="d7e6e-133">IID</span></span><br/>                      | <span data-ttu-id="d7e6e-134">IID_IBackgroundCopyFile5 est défini en tant que 85C1657F-DAFC-40E8-8834-DF18EA25717E</span><span class="sxs-lookup"><span data-stu-id="d7e6e-134">IID_IBackgroundCopyFile5 is defined as 85C1657F-DAFC-40E8-8834-DF18EA25717E</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="d7e6e-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7e6e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7e6e-136">**IBackgroundCopyFile5**</span><span class="sxs-lookup"><span data-stu-id="d7e6e-136">**IBackgroundCopyFile5**</span></span>](ibackgroundcopyfile5.md)
</dt> <dt>

[<span data-ttu-id="d7e6e-137">**IBackgroundCopyFile5. GetProperty**</span><span class="sxs-lookup"><span data-stu-id="d7e6e-137">**IBackgroundCopyFile5.GetProperty**</span></span>](ibackgroundcopyfile5-getproperty.md)
</dt> </dl>

 

 





