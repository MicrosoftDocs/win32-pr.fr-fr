---
title: Méthode IWMDRMNonSilentLicenseAquisition GetChallenge (wmdrmsdk. h)
description: La méthode GetChallenge récupère la demande de licence qui doit être publiée sur le serveur de licences.
ms.assetid: f2ff8484-8fe2-4c74-82c1-9bc14f8197e0
keywords:
- Méthode GetChallenge format Windows Media
- Méthode GetChallenge format Windows Media, interface IWMDRMNonSilentLicenseAquisition
- Interface IWMDRMNonSilentLicenseAquisition Windows Media format, méthode GetChallenge
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition.GetChallenge
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa0dc63c63e5d7a62c06cbe791d9a5e5e8d09c5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534979"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongetchallenge-method"></a><span data-ttu-id="5d882-106">IWMDRMNonSilentLicenseAquisition :: GetChallenge, méthode</span><span class="sxs-lookup"><span data-stu-id="5d882-106">IWMDRMNonSilentLicenseAquisition::GetChallenge method</span></span>

<span data-ttu-id="5d882-107">La méthode **GetChallenge** récupère la demande de licence qui doit être publiée sur le serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="5d882-107">The **GetChallenge** method retrieves the license challenge that should be posted to the license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d882-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d882-108">Syntax</span></span>


```C++
HRESULT GetChallenge(
  [out] BSTR *pbstrChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="5d882-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d882-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d882-110">*pbstrChallenge* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5d882-110">*pbstrChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d882-111">Adresse d’une variable qui reçoit la demande de licence.</span><span class="sxs-lookup"><span data-stu-id="5d882-111">Address of a variable that receives the license challenge.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d882-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5d882-112">Return value</span></span>

<span data-ttu-id="5d882-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="5d882-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5d882-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="5d882-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5d882-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5d882-115">Return code</span></span>                                                                          | <span data-ttu-id="5d882-116">Description</span><span class="sxs-lookup"><span data-stu-id="5d882-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="5d882-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5d882-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5d882-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="5d882-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5d882-119">Notes</span><span class="sxs-lookup"><span data-stu-id="5d882-119">Remarks</span></span>

<span data-ttu-id="5d882-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="5d882-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d882-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d882-121">Requirements</span></span>



| <span data-ttu-id="5d882-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d882-122">Requirement</span></span> | <span data-ttu-id="5d882-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d882-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d882-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d882-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5d882-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d882-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="5d882-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5d882-126">Library</span></span><br/> | <dl> <span data-ttu-id="5d882-127"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d882-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d882-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d882-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d882-129">**Interface IWMDRMNonSilentLicenseAquisition**</span><span class="sxs-lookup"><span data-stu-id="5d882-129">**IWMDRMNonSilentLicenseAquisition Interface**</span></span>](iwmdrmnonsilentlicenseaquisition.md)
</dt> </dl>

 

 





