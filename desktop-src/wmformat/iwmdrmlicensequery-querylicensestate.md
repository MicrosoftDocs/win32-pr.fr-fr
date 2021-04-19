---
title: Méthode IWMDRMLicenseQuery QueryLicenseState (wmdrmsdk. h)
description: La méthode QueryLicenseState interroge le magasin de licences local pour obtenir les informations de licence qui s’appliquent à un ID de clé pour un ou plusieurs droits spécifiques.
ms.assetid: 17f40c56-2266-4c94-9e95-a33a92ddef74
keywords:
- Méthode QueryLicenseState format Windows Media
- Méthode QueryLicenseState format Windows Media, interface IWMDRMLicenseQuery
- Interface IWMDRMLicenseQuery Windows Media format, méthode QueryLicenseState
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.QueryLicenseState
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e101d4ad9b5405906d05ba5e5f230326a1a3f13a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541023"
---
# <a name="iwmdrmlicensequeryquerylicensestate-method"></a><span data-ttu-id="3a6bc-106">IWMDRMLicenseQuery :: QueryLicenseState, méthode</span><span class="sxs-lookup"><span data-stu-id="3a6bc-106">IWMDRMLicenseQuery::QueryLicenseState method</span></span>

<span data-ttu-id="3a6bc-107">La méthode **QueryLicenseState** interroge le magasin de licences local pour obtenir les informations de licence qui s’appliquent à un ID de clé pour un ou plusieurs droits spécifiques.</span><span class="sxs-lookup"><span data-stu-id="3a6bc-107">The **QueryLicenseState** method queries the local license store for license information that applies to a Key ID for one or more specific rights.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a6bc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a6bc-108">Syntax</span></span>


```C++
HRESULT QueryLicenseState(
  [in]  BSTR                   bstrKID,
  [in]  DWORD                  cActionsToQuery,
  [in]  BSTR                   rgbstrActionsToQuery[],
  [out] DRM_LICENSE_STATE_DATA rgResultStateData[]
);
```



## <a name="parameters"></a><span data-ttu-id="3a6bc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3a6bc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a6bc-110">*bstrKID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3a6bc-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a6bc-111">ID de clé à interroger.</span><span class="sxs-lookup"><span data-stu-id="3a6bc-111">Key ID for which to query.</span></span> <span data-ttu-id="3a6bc-112">Seules les licences qui s’appliquent à cet ID de clé sont évaluées.</span><span class="sxs-lookup"><span data-stu-id="3a6bc-112">Only licenses that apply to this Key ID will be evaluated.</span></span>

</dd> <dt>

<span data-ttu-id="3a6bc-113">*cActionsToQuery* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3a6bc-113">*cActionsToQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a6bc-114">Nombre d’actions à interroger.</span><span class="sxs-lookup"><span data-stu-id="3a6bc-114">The number of actions for which to query.</span></span> <span data-ttu-id="3a6bc-115">Cette valeur doit être définie sur le nombre d’éléments dans les tableaux passés pour les paramètres *rgbstrActionsToQuery* et *rgResultStateData* .</span><span class="sxs-lookup"><span data-stu-id="3a6bc-115">This value must be set to the number of elements in the arrays passed for the *rgbstrActionsToQuery* and *rgResultStateData* parameters.</span></span>

</dd> <dt>

<span data-ttu-id="3a6bc-116">*\[ rgbstrActionsToQuery \]* \[dans\]</span><span class="sxs-lookup"><span data-stu-id="3a6bc-116">*rgbstrActionsToQuery\[\]* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a6bc-117">Tableau d’un ou de plusieurs droits à interroger.</span><span class="sxs-lookup"><span data-stu-id="3a6bc-117">Array of one or more rights for which to query.</span></span> <span data-ttu-id="3a6bc-118">Ce tableau doit contenir autant d’éléments que ce qui est spécifié par *cActionsToQuery*.</span><span class="sxs-lookup"><span data-stu-id="3a6bc-118">This array must contain as many elements as specified by *cActionsToQuery*.</span></span> <span data-ttu-id="3a6bc-119">Chaque élément doit être défini sur l’une des constantes suivantes.</span><span class="sxs-lookup"><span data-stu-id="3a6bc-119">Each element must be set to one of the following constants.</span></span>



| <span data-ttu-id="3a6bc-120">Constante</span><span class="sxs-lookup"><span data-stu-id="3a6bc-120">Constant</span></span>                                        | <span data-ttu-id="3a6bc-121">Description</span><span class="sxs-lookup"><span data-stu-id="3a6bc-121">Description</span></span>                                                                                                                                        |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a6bc-122">c \_ wszWMDRM \_ LicenseState \_ sauvegarde</span><span class="sxs-lookup"><span data-stu-id="3a6bc-122">g\_wszWMDRM\_LicenseState\_Backup</span></span>               | <span data-ttu-id="3a6bc-123">Incluez pour demander les détails sur le droit de sauvegarder et de restaurer la licence.</span><span class="sxs-lookup"><span data-stu-id="3a6bc-123">Include to query for the details about the right to back up and restore the license.</span></span>                                                               |
| <span data-ttu-id="3a6bc-124">g \_ wszWMDRM \_ LicenseState \_ CollaborativePlay</span><span class="sxs-lookup"><span data-stu-id="3a6bc-124">g\_wszWMDRM\_LicenseState\_CollaborativePlay</span></span>    | <span data-ttu-id="3a6bc-125">Incluez pour demander les détails sur le droit de partager le contenu avec un groupe d’utilisateurs dans le cadre d’un scénario de lecture collaborative.</span><span class="sxs-lookup"><span data-stu-id="3a6bc-125">Include to query for the details about the right to share the content with a group of users as part of a collaborative playback scenario.</span></span>          |
| <span data-ttu-id="3a6bc-126">\_wszWMDRM g \_ LicenseState \_ copie</span><span class="sxs-lookup"><span data-stu-id="3a6bc-126">g\_wszWMDRM\_LicenseState\_Copy</span></span>                 | <span data-ttu-id="3a6bc-127">Include pour rechercher les détails sur le droit de copier le contenu vers des périphériques ou des médias externes.</span><span class="sxs-lookup"><span data-stu-id="3a6bc-127">Include to query for the details about the right to copy the content to external devices or media.</span></span>                                                 |
| <span data-ttu-id="3a6bc-128">g \_ wszWMDRM \_ LicenseState \_ CopyToCD</span><span class="sxs-lookup"><span data-stu-id="3a6bc-128">g\_wszWMDRM\_LicenseState\_CopyToCD</span></span>             | <span data-ttu-id="3a6bc-129">Incluez pour demander les détails sur le droit de copier le contenu sur CD.</span><span class="sxs-lookup"><span data-stu-id="3a6bc-129">Include to query for the details about the right to copy the content to CD.</span></span>                                                                        |
| <span data-ttu-id="3a6bc-130">g \_ wszWMDRM \_ LicenseState \_ CopyToNonSDMIDevice</span><span class="sxs-lookup"><span data-stu-id="3a6bc-130">g\_wszWMDRM\_LicenseState\_CopyToNonSDMIDevice</span></span>  | <span data-ttu-id="3a6bc-131">Incluez pour demander les détails sur le droit de copier le contenu sur un appareil qui ne prend pas en charge l’initiative de support numérique sécurisé (SDMI).</span><span class="sxs-lookup"><span data-stu-id="3a6bc-131">Include to query for the details about the right to copy the content to a device that does not support the secure digital media initiative (SDMI).</span></span> |
| <span data-ttu-id="3a6bc-132">g \_ wszWMDRM \_ LicenseState \_ CopyToSDMIDevice</span><span class="sxs-lookup"><span data-stu-id="3a6bc-132">g\_wszWMDRM\_LicenseState\_CopyToSDMIDevice</span></span>     | <span data-ttu-id="3a6bc-133">Inclure pour demander les détails sur le droit de copier le contenu sur un appareil qui prend en charge le périphérique SDMI.</span><span class="sxs-lookup"><span data-stu-id="3a6bc-133">Include to query for the details about the right to copy the content to a device that supports the SDMI.</span></span>                                           |
| <span data-ttu-id="3a6bc-134">g \_ wszWMDRM \_ LicenseState \_ CreateThumbnailImage</span><span class="sxs-lookup"><span data-stu-id="3a6bc-134">g\_wszWMDRM\_LicenseState\_CreateThumbnailImage</span></span> | <span data-ttu-id="3a6bc-135">Include pour rechercher les détails sur le droit de créer une image miniature à partir du contenu.</span><span class="sxs-lookup"><span data-stu-id="3a6bc-135">Include to query for the details about the right to create a thumbnail image from the content.</span></span>                                                     |
| <span data-ttu-id="3a6bc-136">\_lecture wszWMDRM \_ LicenseState \_ g</span><span class="sxs-lookup"><span data-stu-id="3a6bc-136">g\_wszWMDRM\_LicenseState\_Playback</span></span>             | <span data-ttu-id="3a6bc-137">Include pour rechercher les détails sur le droit de lire le contenu.</span><span class="sxs-lookup"><span data-stu-id="3a6bc-137">Include to query for the details about the right to play the content.</span></span>                                                                              |
| <span data-ttu-id="3a6bc-138">g \_ wszWMDRM \_ LicenseState \_ PlaylistBurn</span><span class="sxs-lookup"><span data-stu-id="3a6bc-138">g\_wszWMDRM\_LicenseState\_PlaylistBurn</span></span>         | <span data-ttu-id="3a6bc-139">Inclure pour demander les détails sur le droit de copier le contenu sur CD dans le cadre d’une sélection.</span><span class="sxs-lookup"><span data-stu-id="3a6bc-139">Include to query for the details about the right to copy the content to CD as part of a playlist.</span></span>                                                  |



 

</dd> <dt>

<span data-ttu-id="3a6bc-140">*\[ rgResultStateData \]* en \[ sortie\]</span><span class="sxs-lookup"><span data-stu-id="3a6bc-140">*rgResultStateData\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a6bc-141">Tableau d’une ou de plusieurs structures de [**données d' \_ État de licence \_ \_ DRM**](drmdrm-license-state-data.md) qui reçoivent les informations d’état de licence qui s’appliquent à droite dans l’élément correspondant du paramètre *rgbstrActionsToQuery* .</span><span class="sxs-lookup"><span data-stu-id="3a6bc-141">Array of one or more [**DRM\_LICENSE\_STATE\_DATA**](drmdrm-license-state-data.md) structures that receive the license state information that applies to the right in the corresponding element of the *rgbstrActionsToQuery* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a6bc-142">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3a6bc-142">Return value</span></span>

<span data-ttu-id="3a6bc-143">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3a6bc-143">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3a6bc-144">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3a6bc-144">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3a6bc-145">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3a6bc-145">Return code</span></span>                                                                          | <span data-ttu-id="3a6bc-146">Description</span><span class="sxs-lookup"><span data-stu-id="3a6bc-146">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3a6bc-147"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3a6bc-147"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3a6bc-148">S_OK</span><span class="sxs-lookup"><span data-stu-id="3a6bc-148">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3a6bc-149">Notes</span><span class="sxs-lookup"><span data-stu-id="3a6bc-149">Remarks</span></span>

<span data-ttu-id="3a6bc-150">Toutes les licences qui s’appliquent à l’ID de clé spécifié seront recherchées et évaluées.</span><span class="sxs-lookup"><span data-stu-id="3a6bc-150">All licenses that apply to the specified Key ID will be searched and evaluated.</span></span> <span data-ttu-id="3a6bc-151">Les résultats sont agrégés, de sorte que chaque structure de **\_ données d' \_ état \_ de licence DRM** peut contenir des informations provenant de plusieurs licences.</span><span class="sxs-lookup"><span data-stu-id="3a6bc-151">The results are aggregated, so each **DRM\_LICENSE\_STATE\_DATA** structure may contain information from multiple licenses.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a6bc-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a6bc-152">Requirements</span></span>



| <span data-ttu-id="3a6bc-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a6bc-153">Requirement</span></span> | <span data-ttu-id="3a6bc-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a6bc-154">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a6bc-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="3a6bc-155">Header</span></span><br/>  | <dl> <span data-ttu-id="3a6bc-156"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a6bc-156"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="3a6bc-157">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3a6bc-157">Library</span></span><br/> | <dl> <span data-ttu-id="3a6bc-158"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a6bc-158"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a6bc-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a6bc-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a6bc-160">**Interface IWMDRMLicenseQuery**</span><span class="sxs-lookup"><span data-stu-id="3a6bc-160">**IWMDRMLicenseQuery Interface**</span></span>](iwmdrmlicensequery.md)
</dt> </dl>

 

 





