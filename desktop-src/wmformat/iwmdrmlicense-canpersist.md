---
title: Méthode IWMDRMLicense CanPersist (wmdrmsdk. h)
description: La méthode CanPersist interroge si la licence peut être rendue persistante dans un magasin de licences local.
ms.assetid: 040b30d8-4e47-44a3-8b09-e81cc30e8a53
keywords:
- Méthode CanPersist format Windows Media
- Méthode CanPersist format Windows Media, interface IWMDRMLicense
- Interface IWMDRMLicense Windows Media format, méthode CanPersist
topic_type:
- apiref
api_name:
- IWMDRMLicense.CanPersist
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7772dac73b99443626b1eeec6f5e90851f92c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540296"
---
# <a name="iwmdrmlicensecanpersist-method"></a><span data-ttu-id="404a9-106">IWMDRMLicense :: CanPersist, méthode</span><span class="sxs-lookup"><span data-stu-id="404a9-106">IWMDRMLicense::CanPersist method</span></span>

<span data-ttu-id="404a9-107">La méthode **CanPersist** interroge si la licence peut être rendue persistante dans un magasin de licences local.</span><span class="sxs-lookup"><span data-stu-id="404a9-107">The **CanPersist** method queries whether the license can be persisted on in a local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="404a9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="404a9-108">Syntax</span></span>


```C++
HRESULT CanPersist(
  [out] BOOL *pfCanPersist
);
```



## <a name="parameters"></a><span data-ttu-id="404a9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="404a9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="404a9-110">*pfCanPersist* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="404a9-110">*pfCanPersist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="404a9-111">La valeur TRUE indique que la licence peut être persistante.</span><span class="sxs-lookup"><span data-stu-id="404a9-111">TRUE indicates that the license can be persisted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="404a9-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="404a9-112">Return value</span></span>

<span data-ttu-id="404a9-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="404a9-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="404a9-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="404a9-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="404a9-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="404a9-115">Return code</span></span>                                                                          | <span data-ttu-id="404a9-116">Description</span><span class="sxs-lookup"><span data-stu-id="404a9-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="404a9-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="404a9-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="404a9-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="404a9-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="404a9-119">Notes</span><span class="sxs-lookup"><span data-stu-id="404a9-119">Remarks</span></span>

<span data-ttu-id="404a9-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="404a9-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="404a9-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="404a9-121">Requirements</span></span>



| <span data-ttu-id="404a9-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="404a9-122">Requirement</span></span> | <span data-ttu-id="404a9-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="404a9-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="404a9-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="404a9-124">Header</span></span><br/> | <dl> <span data-ttu-id="404a9-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="404a9-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="404a9-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="404a9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="404a9-127">**Interface IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="404a9-127">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





