---
title: IWMDRMNonSilentLicenseAquisition GetURL, méthode (wmdrmsdk. h)
description: La méthode GetURL récupère l’URL vers laquelle la demande de licence doit être publiée.
ms.assetid: f65f1984-74bc-4cd0-957e-930aa6a6f6a5
keywords:
- GetURL, méthode Windows Media format
- GetURL, méthode Windows Media format, interface IWMDRMNonSilentLicenseAquisition
- Interface IWMDRMNonSilentLicenseAquisition Windows Media format, GetURL, méthode
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition.GetURL
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79212d19d7dbf4a66e2b72dcbdeba9262a9aeddd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537389"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongeturl-method"></a><span data-ttu-id="e5887-106">IWMDRMNonSilentLicenseAquisition :: GetURL, méthode</span><span class="sxs-lookup"><span data-stu-id="e5887-106">IWMDRMNonSilentLicenseAquisition::GetURL method</span></span>

<span data-ttu-id="e5887-107">La méthode **getURL** récupère l’URL vers laquelle la demande de licence doit être publiée.</span><span class="sxs-lookup"><span data-stu-id="e5887-107">The **GetURL** method retrieves the URL to which the license challenge should be posted.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5887-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5887-108">Syntax</span></span>


```C++
HRESULT GetURL(
  [out] BSTR *pbstrURL
);
```



## <a name="parameters"></a><span data-ttu-id="e5887-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5887-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5887-110">*pbstrURL* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e5887-110">*pbstrURL* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5887-111">Adresse d’une variable qui reçoit l’URL.</span><span class="sxs-lookup"><span data-stu-id="e5887-111">Address of a variable that receives the URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5887-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e5887-112">Return value</span></span>

<span data-ttu-id="e5887-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e5887-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e5887-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e5887-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e5887-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e5887-115">Return code</span></span>                                                                          | <span data-ttu-id="e5887-116">Description</span><span class="sxs-lookup"><span data-stu-id="e5887-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e5887-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e5887-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e5887-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="e5887-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e5887-119">Notes</span><span class="sxs-lookup"><span data-stu-id="e5887-119">Remarks</span></span>

<span data-ttu-id="e5887-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e5887-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5887-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e5887-121">Requirements</span></span>



| <span data-ttu-id="e5887-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e5887-122">Requirement</span></span> | <span data-ttu-id="e5887-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5887-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5887-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="e5887-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e5887-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5887-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="e5887-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e5887-126">Library</span></span><br/> | <dl> <span data-ttu-id="e5887-127"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5887-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5887-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5887-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5887-129">**Interface IWMDRMNonSilentLicenseAquisition**</span><span class="sxs-lookup"><span data-stu-id="e5887-129">**IWMDRMNonSilentLicenseAquisition Interface**</span></span>](iwmdrmnonsilentlicenseaquisition.md)
</dt> </dl>

 

 





