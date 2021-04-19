---
title: Méthode IWMDRMLicenseManagement DeleteLicense (wmdrmsdk. h)
description: La méthode DeleteLicense supprime une licence du magasin de licences local temporaire.
ms.assetid: 0aa7143a-845a-41a4-8b3c-a04c68ee280a
keywords:
- Méthode DeleteLicense format Windows Media
- Méthode DeleteLicense format Windows Media, interface IWMDRMLicenseManagement
- Interface IWMDRMLicenseManagement Windows Media format, méthode DeleteLicense
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.DeleteLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d5b52f6277459f147285f46fc791669e56061a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542417"
---
# <a name="iwmdrmlicensemanagementdeletelicense-method"></a><span data-ttu-id="c9649-106">IWMDRMLicenseManagement ::D méthode eleteLicense</span><span class="sxs-lookup"><span data-stu-id="c9649-106">IWMDRMLicenseManagement::DeleteLicense method</span></span>

<span data-ttu-id="c9649-107">La méthode **DeleteLicense** supprime une licence du magasin de licences local temporaire.</span><span class="sxs-lookup"><span data-stu-id="c9649-107">The **DeleteLicense** method removes a license from the temporary local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9649-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9649-108">Syntax</span></span>


```C++
HRESULT DeleteLicense(
  [in] BSTR  bstrKID,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="c9649-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9649-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9649-110">*bstrKID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9649-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9649-111">ID de clé (KID) de la licence à supprimer.</span><span class="sxs-lookup"><span data-stu-id="c9649-111">Key ID (KID) of the license to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="c9649-112">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9649-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9649-113">Indicateurs d’option de suppression de licence.</span><span class="sxs-lookup"><span data-stu-id="c9649-113">License deletion option flags.</span></span> <span data-ttu-id="c9649-114">Définissez l’une des valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c9649-114">Set to one of the values in the following table.</span></span>



| <span data-ttu-id="c9649-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9649-115">Value</span></span>                                    | <span data-ttu-id="c9649-116">Description</span><span class="sxs-lookup"><span data-stu-id="c9649-116">Description</span></span>                                                                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9649-117">\_Supprimer la \_ licence WMDRM \_ immédiatement</span><span class="sxs-lookup"><span data-stu-id="c9649-117">WMDRM\_DELETE\_LICENSE\_IMMEDIATELY</span></span>      | <span data-ttu-id="c9649-118">Spécifie que la licence doit être supprimée immédiatement du magasin.</span><span class="sxs-lookup"><span data-stu-id="c9649-118">Specifies that the license should be removed from the store immediately.</span></span>                                                                                                                              |
| <span data-ttu-id="c9649-119">\_suppression \_ de la \_ marque de licence WMDRM \_ pour la \_ purge</span><span class="sxs-lookup"><span data-stu-id="c9649-119">WMDRM\_DELETE\_LICENSE\_MARK\_FOR\_PURGE</span></span> | <span data-ttu-id="c9649-120">Spécifie que la licence doit être marquée pour suppression, mais ne doit pas être supprimée du magasin tant que la méthode [**CleanLicenseStore**](iwmdrmlicensemanagement-cleanlicensestore.md) n’est pas appelée.</span><span class="sxs-lookup"><span data-stu-id="c9649-120">Specifies that the license should be marked for deletion, but should not be removed from the store until the [**CleanLicenseStore**](iwmdrmlicensemanagement-cleanlicensestore.md) method is called.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9649-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c9649-121">Return value</span></span>

<span data-ttu-id="c9649-122">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c9649-122">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c9649-123">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c9649-123">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c9649-124">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c9649-124">Return code</span></span>                                                                                            | <span data-ttu-id="c9649-125">Description</span><span class="sxs-lookup"><span data-stu-id="c9649-125">Description</span></span>                                                                                                         |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c9649-126"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c9649-126"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="c9649-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="c9649-127">The method succeeded.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="c9649-128"><dt>**\_LICENSENOTFOUND DRM E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c9649-128"><dt>**DRM\_E\_LICENSENOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="c9649-129">La licence spécifiée n’existe pas dans le magasin.</span><span class="sxs-lookup"><span data-stu-id="c9649-129">The specified license does not exist in the store.</span></span><br/> <span data-ttu-id="c9649-130">- OU -</span><span class="sxs-lookup"><span data-stu-id="c9649-130">- OR -</span></span><br/> <span data-ttu-id="c9649-131">Le magasin est introuvable.</span><span class="sxs-lookup"><span data-stu-id="c9649-131">The store was not found.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c9649-132">Notes</span><span class="sxs-lookup"><span data-stu-id="c9649-132">Remarks</span></span>

<span data-ttu-id="c9649-133">Pour supprimer des licences du magasin de licences local permanent, vous devez utiliser la révocation de licence.</span><span class="sxs-lookup"><span data-stu-id="c9649-133">To delete licenses from the permanent local license store, you must use license revocation.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9649-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9649-134">Requirements</span></span>



| <span data-ttu-id="c9649-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9649-135">Requirement</span></span> | <span data-ttu-id="c9649-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9649-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9649-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9649-137">Header</span></span><br/>  | <dl> <span data-ttu-id="c9649-138"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9649-138"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="c9649-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c9649-139">Library</span></span><br/> | <dl> <span data-ttu-id="c9649-140"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9649-140"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9649-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9649-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9649-142">**Interface IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="c9649-142">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





