---
title: IBackgroundCopyFile5 GetProperty, méthode (Deliveryoptimization. h)
description: Obtient une propriété générique d’un transfert de fichiers d’optimisation de la remise.
ms.assetid: E2E96A0F-5670-4DE7-9DF8-A215AFAD0E8A
keywords:
- GetProperty, méthode
- Méthode GetProperty, interface IBackgroundCopyFile5
- Interface IBackgroundCopyFile5, méthode GetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 84c6a9f96fc332bda940573bde78d7dd05efeeb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103508"
---
# <a name="ibackgroundcopyfile5getproperty-method"></a><span data-ttu-id="f4e83-106">IBackgroundCopyFile5 :: GetProperty, méthode</span><span class="sxs-lookup"><span data-stu-id="f4e83-106">IBackgroundCopyFile5::GetProperty method</span></span>

<span data-ttu-id="f4e83-107">Obtient une propriété générique d’un transfert de fichiers d’optimisation de la remise.</span><span class="sxs-lookup"><span data-stu-id="f4e83-107">Gets a generic property of a Delivery Optimization (DO) file transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4e83-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4e83-108">Syntax</span></span>


```C++
HRESULT GetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *PropertyValue
);
```



## <a name="parameters"></a><span data-ttu-id="f4e83-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f4e83-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4e83-110">*PropertyId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f4e83-110">*PropertyId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4e83-111">Spécifie la propriété de fichier dont la valeur doit être récupérée.</span><span class="sxs-lookup"><span data-stu-id="f4e83-111">Specifies the file property whose value is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="f4e83-112">*PropertyValue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f4e83-112">*PropertyValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4e83-113">Valeur de la propriété, retournée en tant que pointeur vers une BITS_FILE_PROPERTY_VALUE Union.</span><span class="sxs-lookup"><span data-stu-id="f4e83-113">The property value, returned as a pointer to a BITS_FILE_PROPERTY_VALUE union.</span></span> <span data-ttu-id="f4e83-114">Utilisez le champ Union correspondant à la valeur de l’ID de propriété passée.</span><span class="sxs-lookup"><span data-stu-id="f4e83-114">Use the union field appropriate for the property ID value passed in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4e83-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f4e83-115">Return value</span></span>

<span data-ttu-id="f4e83-116">Si cette méthode est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="f4e83-116">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="f4e83-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f4e83-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4e83-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4e83-118">Requirements</span></span>



| <span data-ttu-id="f4e83-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4e83-119">Requirement</span></span> | <span data-ttu-id="f4e83-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4e83-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4e83-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4e83-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f4e83-122">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f4e83-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f4e83-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4e83-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f4e83-124">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f4e83-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f4e83-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="f4e83-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4e83-126"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4e83-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="f4e83-127">MIDL</span><span class="sxs-lookup"><span data-stu-id="f4e83-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f4e83-128"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f4e83-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="f4e83-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f4e83-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="f4e83-130"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f4e83-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="f4e83-131">DLL</span><span class="sxs-lookup"><span data-stu-id="f4e83-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4e83-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4e83-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="f4e83-133">IID</span><span class="sxs-lookup"><span data-stu-id="f4e83-133">IID</span></span><br/>                      | <span data-ttu-id="f4e83-134">IID_IBackgroundCopyFile5 est défini en tant que 85C1657F-DAFC-40E8-8834-DF18EA25717E</span><span class="sxs-lookup"><span data-stu-id="f4e83-134">IID_IBackgroundCopyFile5 is defined as 85C1657F-DAFC-40E8-8834-DF18EA25717E</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="f4e83-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4e83-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4e83-136">**IBackgroundCopyFile5**</span><span class="sxs-lookup"><span data-stu-id="f4e83-136">**IBackgroundCopyFile5**</span></span>](ibackgroundcopyfile5.md)
</dt> <dt>

[<span data-ttu-id="f4e83-137">**IBackgroundCopyFile5. SetProperty**</span><span class="sxs-lookup"><span data-stu-id="f4e83-137">**IBackgroundCopyFile5.SetProperty**</span></span>](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





