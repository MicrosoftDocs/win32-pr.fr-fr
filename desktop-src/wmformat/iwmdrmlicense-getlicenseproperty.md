---
title: Méthode IWMDRMLicense GetLicenseProperty (wmdrmsdk. h)
description: La méthode GetLicenseProperty récupère une propriété de la licence actuelle.
ms.assetid: 5431f849-b37e-40b7-8bdb-ee30948aeff1
keywords:
- Méthode GetLicenseProperty format Windows Media
- Méthode GetLicenseProperty format Windows Media, interface IWMDRMLicense
- Interface IWMDRMLicense Windows Media format, méthode GetLicenseProperty
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetLicenseProperty
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf7fe91c57b9c69934f093cdd504b5e6d35efb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528655"
---
# <a name="iwmdrmlicensegetlicenseproperty-method"></a><span data-ttu-id="edb09-106">IWMDRMLicense :: GetLicenseProperty, méthode</span><span class="sxs-lookup"><span data-stu-id="edb09-106">IWMDRMLicense::GetLicenseProperty method</span></span>

<span data-ttu-id="edb09-107">La méthode **GetLicenseProperty** récupère une propriété de la licence actuelle.</span><span class="sxs-lookup"><span data-stu-id="edb09-107">The **GetLicenseProperty** method retrieves a property from the current license.</span></span>

## <a name="syntax"></a><span data-ttu-id="edb09-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="edb09-108">Syntax</span></span>


```C++
HRESULT GetLicenseProperty(
  [in]  BSTR        bstrName,
  [out] PROPVARIANT *ppropVariant
);
```



## <a name="parameters"></a><span data-ttu-id="edb09-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="edb09-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edb09-110">*bstrName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="edb09-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edb09-111">Nom de la propriété à récupérer.</span><span class="sxs-lookup"><span data-stu-id="edb09-111">Name of the property to retrieve.</span></span> <span data-ttu-id="edb09-112">Définissez l’une des constantes dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="edb09-112">Set to one of the constants in the following table:</span></span>



| <span data-ttu-id="edb09-113">Constante</span><span class="sxs-lookup"><span data-stu-id="edb09-113">Constant</span></span>                   | <span data-ttu-id="edb09-114">Description</span><span class="sxs-lookup"><span data-stu-id="edb09-114">Description</span></span>                                                                                                          |
|----------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edb09-115">révocation de \_ wszWMDRMNet g \_</span><span class="sxs-lookup"><span data-stu-id="edb09-115">g\_wszWMDRMNet\_Revocation</span></span> | <span data-ttu-id="edb09-116">Utilisez pour obtenir la liste de révocation de Windows Media DRM pour les périphériques réseau pour la licence actuelle.</span><span class="sxs-lookup"><span data-stu-id="edb09-116">Use to get the Windows Media DRM for Network Devices revocation list for the current license.</span></span>                        |
| <span data-ttu-id="edb09-117">g \_ wszWMDRM \_ SAPLEVEL</span><span class="sxs-lookup"><span data-stu-id="edb09-117">g\_wszWMDRM\_SAPLEVEL</span></span>      | <span data-ttu-id="edb09-118">Utilisez pour obtenir le niveau de chemin d’accès audio sécurisé (SAP) requis pour lire le contenu couvert par la licence actuelle.</span><span class="sxs-lookup"><span data-stu-id="edb09-118">Use to get the Secure Audio Path (SAP) level required to play content covered by the current license.</span></span>                |
| <span data-ttu-id="edb09-119">g \_ wszWMDRM \_ SAPRequired</span><span class="sxs-lookup"><span data-stu-id="edb09-119">g\_wszWMDRM\_SAPRequired</span></span>   | <span data-ttu-id="edb09-120">Utilisez pour vérifier si la licence actuelle requiert que SAP soit utilisé pour lire le contenu.</span><span class="sxs-lookup"><span data-stu-id="edb09-120">Use to ascertain whether the current license requires SAP be used to play the content.</span></span>                               |
| <span data-ttu-id="edb09-121">\_wszWMDRM \_ SOURCEID</span><span class="sxs-lookup"><span data-stu-id="edb09-121">g\_wszWMDRM\_SOURCEID</span></span>      | <span data-ttu-id="edb09-122">Utilisez pour obtenir l’identificateur source de la licence actuelle.</span><span class="sxs-lookup"><span data-stu-id="edb09-122">Use to get the source identifier for the current license.</span></span>                                                            |
| <span data-ttu-id="edb09-123">\_priorité wszWMDRM \_ g</span><span class="sxs-lookup"><span data-stu-id="edb09-123">g\_wszWMDRM\_PRIORITY</span></span>      | <span data-ttu-id="edb09-124">Utilisez pour connaître la priorité de la licence actuelle.</span><span class="sxs-lookup"><span data-stu-id="edb09-124">Use to get the priority of the current license.</span></span> <span data-ttu-id="edb09-125">Les licences de priorité plus élevée sont appliquées avant les licences de faible priorité.</span><span class="sxs-lookup"><span data-stu-id="edb09-125">Higher priority licenses are applied before lower priority licenses.</span></span> |
| <span data-ttu-id="edb09-126">g \_ wszWMDRM \_</span><span class="sxs-lookup"><span data-stu-id="edb09-126">g\_wszWMDRM\_UplinkID</span></span>      | <span data-ttu-id="edb09-127">Utilisez pour récupérer l’ID de clé de la licence racine dans la chaîne de licences à laquelle la licence actuelle appartient.</span><span class="sxs-lookup"><span data-stu-id="edb09-127">Use to get the key ID of the root license in the license chain that the current license belongs to.</span></span>                  |



 

</dd> <dt>

<span data-ttu-id="edb09-128">*ppropVariant* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="edb09-128">*ppropVariant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="edb09-129">Reçoit la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="edb09-129">Receives the property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edb09-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="edb09-130">Return value</span></span>

<span data-ttu-id="edb09-131">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="edb09-131">The method returns an **HRESULT**.</span></span> <span data-ttu-id="edb09-132">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="edb09-132">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="edb09-133">Code de retour</span><span class="sxs-lookup"><span data-stu-id="edb09-133">Return code</span></span>                                                                          | <span data-ttu-id="edb09-134">Description</span><span class="sxs-lookup"><span data-stu-id="edb09-134">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="edb09-135"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="edb09-135"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="edb09-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="edb09-136">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="edb09-137">Notes</span><span class="sxs-lookup"><span data-stu-id="edb09-137">Remarks</span></span>

<span data-ttu-id="edb09-138">Aucun.</span><span class="sxs-lookup"><span data-stu-id="edb09-138">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="edb09-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="edb09-139">Requirements</span></span>



| <span data-ttu-id="edb09-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="edb09-140">Requirement</span></span> | <span data-ttu-id="edb09-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="edb09-141">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="edb09-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="edb09-142">Header</span></span><br/>  | <dl> <span data-ttu-id="edb09-143"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="edb09-143"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="edb09-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="edb09-144">Library</span></span><br/> | <dl> <span data-ttu-id="edb09-145"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="edb09-145"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edb09-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="edb09-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edb09-147">**GetLicense**</span><span class="sxs-lookup"><span data-stu-id="edb09-147">**GetLicense**</span></span>](iwmdrmlicense-getlicense.md)
</dt> <dt>

[<span data-ttu-id="edb09-148">**Interface IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="edb09-148">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





