---
title: Méthode IWMDRMLicenseManagement StoreLicense (wmdrmsdk. h)
description: La méthode StoreLicense comprend une licence générée en dehors du sous-système local DRM dans le magasin de licences local.
ms.assetid: 2190ff8c-8969-4f03-9f90-331bff8f4da2
keywords:
- Méthode StoreLicense format Windows Media
- Méthode StoreLicense format Windows Media, interface IWMDRMLicenseManagement
- Interface IWMDRMLicenseManagement Windows Media format, méthode StoreLicense
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.StoreLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcfde6347e099ceb9fc168e1183cbd62c90f9b9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543591"
---
# <a name="iwmdrmlicensemanagementstorelicense-method"></a><span data-ttu-id="02ca4-106">IWMDRMLicenseManagement :: StoreLicense, méthode</span><span class="sxs-lookup"><span data-stu-id="02ca4-106">IWMDRMLicenseManagement::StoreLicense method</span></span>

<span data-ttu-id="02ca4-107">La méthode **StoreLicense** comprend une licence générée en dehors du sous-système local DRM dans le magasin de licences local.</span><span class="sxs-lookup"><span data-stu-id="02ca4-107">The **StoreLicense** method includes a license that was generated outside of the local DRM subsystem in the local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="02ca4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02ca4-108">Syntax</span></span>


```C++
HRESULT StoreLicense(
  [in] BSTR bstrLicenseResponse
);
```



## <a name="parameters"></a><span data-ttu-id="02ca4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02ca4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02ca4-110">*bstrLicenseResponse* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02ca4-110">*bstrLicenseResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02ca4-111">Chaîne de réponse de licence à décoder et à ajouter au magasin de licences local.</span><span class="sxs-lookup"><span data-stu-id="02ca4-111">License response string to be decoded and added to the local license store.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02ca4-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="02ca4-112">Return value</span></span>

<span data-ttu-id="02ca4-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="02ca4-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="02ca4-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="02ca4-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="02ca4-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="02ca4-115">Return code</span></span>                                                                          | <span data-ttu-id="02ca4-116">Description</span><span class="sxs-lookup"><span data-stu-id="02ca4-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="02ca4-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="02ca4-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="02ca4-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="02ca4-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="02ca4-119">Notes</span><span class="sxs-lookup"><span data-stu-id="02ca4-119">Remarks</span></span>

<span data-ttu-id="02ca4-120">Vous pouvez utiliser cette méthode pour ajouter des licences XMR que vous avez créées dans le magasin de licences local.</span><span class="sxs-lookup"><span data-stu-id="02ca4-120">You can use this method to add XMR licenses that you have created to the local license store.</span></span>

## <a name="requirements"></a><span data-ttu-id="02ca4-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02ca4-121">Requirements</span></span>



| <span data-ttu-id="02ca4-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02ca4-122">Requirement</span></span> | <span data-ttu-id="02ca4-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="02ca4-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02ca4-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="02ca4-124">Header</span></span><br/>  | <dl> <span data-ttu-id="02ca4-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="02ca4-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="02ca4-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="02ca4-126">Library</span></span><br/> | <dl> <span data-ttu-id="02ca4-127"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02ca4-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02ca4-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02ca4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02ca4-129">**Interface IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="02ca4-129">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





