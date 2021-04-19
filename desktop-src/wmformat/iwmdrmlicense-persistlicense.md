---
title: Méthode IWMDRMLicense PersistLicense (wmdrmsdk. h)
description: La méthode PersistLicense enregistre la licence actuelle du magasin temporaire dans le magasin de licences local permanent.
ms.assetid: 80a0f932-2800-416b-9dfe-97654a76c19b
keywords:
- Méthode PersistLicense format Windows Media
- Méthode PersistLicense format Windows Media, interface IWMDRMLicense
- Interface IWMDRMLicense Windows Media format, méthode PersistLicense
topic_type:
- apiref
api_name:
- IWMDRMLicense.PersistLicense
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f41b61cdf448d757d13917ca22af0c3d9d9d390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534981"
---
# <a name="iwmdrmlicensepersistlicense-method"></a><span data-ttu-id="8632d-106">IWMDRMLicense ::P méthode ersistLicense</span><span class="sxs-lookup"><span data-stu-id="8632d-106">IWMDRMLicense::PersistLicense method</span></span>

<span data-ttu-id="8632d-107">La méthode **PersistLicense** enregistre la licence actuelle du magasin temporaire dans le magasin de licences local permanent.</span><span class="sxs-lookup"><span data-stu-id="8632d-107">The **PersistLicense** method saves the current license from the temporary store into the permanent local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="8632d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8632d-108">Syntax</span></span>


```C++
HRESULT PersistLicense();
```



## <a name="parameters"></a><span data-ttu-id="8632d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8632d-109">Parameters</span></span>

<span data-ttu-id="8632d-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="8632d-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8632d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8632d-111">Return value</span></span>

<span data-ttu-id="8632d-112">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8632d-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8632d-113">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8632d-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8632d-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8632d-114">Return code</span></span>                                                                          | <span data-ttu-id="8632d-115">Description</span><span class="sxs-lookup"><span data-stu-id="8632d-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8632d-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8632d-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8632d-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="8632d-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8632d-118">Notes</span><span class="sxs-lookup"><span data-stu-id="8632d-118">Remarks</span></span>

<span data-ttu-id="8632d-119">Si la licence actuelle ne se trouve pas dans le magasin temporaire, cette méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="8632d-119">If the current license is not in the temporary store, this method will fail.</span></span>

<span data-ttu-id="8632d-120">Vous pouvez appeler [**CanPersist**](iwmdrmlicense-canpersist.md) pour demander si la licence est autorisée à être persistante.</span><span class="sxs-lookup"><span data-stu-id="8632d-120">You can call [**CanPersist**](iwmdrmlicense-canpersist.md) to query whether the license is allowed to be persisted.</span></span>

## <a name="requirements"></a><span data-ttu-id="8632d-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8632d-121">Requirements</span></span>



| <span data-ttu-id="8632d-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8632d-122">Requirement</span></span> | <span data-ttu-id="8632d-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="8632d-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8632d-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="8632d-124">Header</span></span><br/> | <dl> <span data-ttu-id="8632d-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="8632d-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8632d-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8632d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8632d-127">**Interface IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="8632d-127">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





