---
title: Méthode IWMDRMLicenseQuery QueryActionAllowed (wmdrmsdk. h)
description: La méthode QueryActionAllowed exécute une requête sur le magasin de licences local pour récupérer l’état de la licence pour une ou plusieurs actions DRM qui s’appliquent à un ID de clé spécifié.
ms.assetid: 814c2850-c036-4c44-a64e-861e88f16fb1
keywords:
- Méthode QueryActionAllowed format Windows Media
- Méthode QueryActionAllowed format Windows Media, interface IWMDRMLicenseQuery
- Interface IWMDRMLicenseQuery Windows Media format, méthode QueryActionAllowed
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.QueryActionAllowed
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6564062fc9f76a840b37f6e134e960480d67a2ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533304"
---
# <a name="iwmdrmlicensequeryqueryactionallowed-method"></a><span data-ttu-id="fd26d-106">IWMDRMLicenseQuery :: QueryActionAllowed, méthode</span><span class="sxs-lookup"><span data-stu-id="fd26d-106">IWMDRMLicenseQuery::QueryActionAllowed method</span></span>

<span data-ttu-id="fd26d-107">La méthode **QueryActionAllowed** exécute une requête sur le magasin de licences local pour récupérer l’état de la licence pour une ou plusieurs actions DRM qui s’appliquent à un ID de clé spécifié.</span><span class="sxs-lookup"><span data-stu-id="fd26d-107">The **QueryActionAllowed** method performs a query on the local license store to retrieve the license status for one or more DRM actions that apply to a specified Key ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd26d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd26d-108">Syntax</span></span>


```C++
HRESULT QueryActionAllowed(
  [in]  BSTR  bstrKID,
  [in]  BSTR  bstrMinReqIndivVersion,
  [in]  DWORD cActionsToQuery,
  [in]  BSTR  rgbstrActionsToQuery[],
  [out] DWORD rgdwQueryResult[]
);
```



## <a name="parameters"></a><span data-ttu-id="fd26d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd26d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd26d-110">*bstrKID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd26d-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd26d-111">ID de clé à interroger.</span><span class="sxs-lookup"><span data-stu-id="fd26d-111">Key ID for which to query.</span></span> <span data-ttu-id="fd26d-112">Seules les licences qui s’appliquent à cet ID de clé sont évaluées.</span><span class="sxs-lookup"><span data-stu-id="fd26d-112">Only licenses that apply to this Key ID will be evaluated.</span></span>

</dd> <dt>

<span data-ttu-id="fd26d-113">*bstrMinReqIndivVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd26d-113">*bstrMinReqIndivVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd26d-114">Version de sécurité minimale spécifiée dans l’en-tête du fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="fd26d-114">The minimum security version specified in the header of the ASF file.</span></span> <span data-ttu-id="fd26d-115">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="fd26d-115">This parameter is optional.</span></span> <span data-ttu-id="fd26d-116">Transmettez la **valeur null** pour exécuter la requête sans ces informations.</span><span class="sxs-lookup"><span data-stu-id="fd26d-116">Pass **NULL** to perform the query without this information.</span></span>

</dd> <dt>

<span data-ttu-id="fd26d-117">*cActionsToQuery* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd26d-117">*cActionsToQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd26d-118">Nombre d’actions à interroger.</span><span class="sxs-lookup"><span data-stu-id="fd26d-118">The number of actions for which to query.</span></span> <span data-ttu-id="fd26d-119">Cette valeur doit être définie sur le nombre d’éléments dans les tableaux passés pour les paramètres *rgbstrActionsToQuery* et *rgdwQueryResult* .</span><span class="sxs-lookup"><span data-stu-id="fd26d-119">This value must be set to the number of elements in the arrays passed for the *rgbstrActionsToQuery* and *rgdwQueryResult* parameters.</span></span>

</dd> <dt>

<span data-ttu-id="fd26d-120">*\[ rgbstrActionsToQuery \]* \[dans\]</span><span class="sxs-lookup"><span data-stu-id="fd26d-120">*rgbstrActionsToQuery\[\]* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd26d-121">Tableau d’un ou de plusieurs droits à interroger.</span><span class="sxs-lookup"><span data-stu-id="fd26d-121">Array of one or more rights for which to query.</span></span> <span data-ttu-id="fd26d-122">Ce tableau doit contenir autant d’éléments que ce qui est spécifié par *cActionsToQuery*.</span><span class="sxs-lookup"><span data-stu-id="fd26d-122">This array must contain as many elements as specified by *cActionsToQuery*.</span></span> <span data-ttu-id="fd26d-123">Chaque élément doit être défini sur l’une des constantes suivantes :</span><span class="sxs-lookup"><span data-stu-id="fd26d-123">Each element must be set to one of the following constants:</span></span>



| <span data-ttu-id="fd26d-124">Constante</span><span class="sxs-lookup"><span data-stu-id="fd26d-124">Constant</span></span>                                         | <span data-ttu-id="fd26d-125">Description</span><span class="sxs-lookup"><span data-stu-id="fd26d-125">Description</span></span>                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fd26d-126">\_lecture wszWMDRM \_ ActionAllowed \_ g</span><span class="sxs-lookup"><span data-stu-id="fd26d-126">g\_wszWMDRM\_ActionAllowed\_Playback</span></span>             | <span data-ttu-id="fd26d-127">Inclure pour demander le droit de lire le contenu.</span><span class="sxs-lookup"><span data-stu-id="fd26d-127">Include to query for the right to play the content.</span></span>                              |
| <span data-ttu-id="fd26d-128">\_wszWMDRM g \_ ActionAllowed \_ copie</span><span class="sxs-lookup"><span data-stu-id="fd26d-128">g\_wszWMDRM\_ActionAllowed\_Copy</span></span>                 | <span data-ttu-id="fd26d-129">Inclure pour demander le droit de copier le contenu vers des périphériques ou des médias externes.</span><span class="sxs-lookup"><span data-stu-id="fd26d-129">Include to query for the right to copy the content to external devices or media.</span></span> |
| <span data-ttu-id="fd26d-130">g \_ wszWMDRM \_ ActionAllowed \_ PlaylistBurn</span><span class="sxs-lookup"><span data-stu-id="fd26d-130">g\_wszWMDRM\_ActionAllowed\_PlaylistBurn</span></span>         | <span data-ttu-id="fd26d-131">Inclure pour demander le droit de copier le contenu sur CD dans le cadre d’une sélection.</span><span class="sxs-lookup"><span data-stu-id="fd26d-131">Include to query for the right to copy the content to CD as part of a playlist.</span></span>  |
| <span data-ttu-id="fd26d-132">g \_ wszWMDRM \_ ActionAllowed \_ CreateThumbnailImage</span><span class="sxs-lookup"><span data-stu-id="fd26d-132">g\_wszWMDRM\_ActionAllowed\_CreateThumbnailImage</span></span> | <span data-ttu-id="fd26d-133">Inclure pour demander le droit de créer une image miniature à partir du contenu.</span><span class="sxs-lookup"><span data-stu-id="fd26d-133">Include to query for the right to create a thumbnail image from the content.</span></span>     |
| <span data-ttu-id="fd26d-134">g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD</span><span class="sxs-lookup"><span data-stu-id="fd26d-134">g\_wszWMDRM\_ActionAllowed\_CopyToCD</span></span>             | <span data-ttu-id="fd26d-135">Inclure pour demander le droit de copier le contenu sur CD.</span><span class="sxs-lookup"><span data-stu-id="fd26d-135">Include to query for the right to copy the content to CD.</span></span>                        |



 

</dd> <dt>

<span data-ttu-id="fd26d-136">*\[ rgdwQueryResult \]* en \[ sortie\]</span><span class="sxs-lookup"><span data-stu-id="fd26d-136">*rgdwQueryResult\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd26d-137">Tableau d’une ou plusieurs variables DWORD qui reçoivent les résultats de la requête pour les droits spécifiés par *rgbstrActionsToQuery*.</span><span class="sxs-lookup"><span data-stu-id="fd26d-137">Array of one or more DWORD variables that receive the results of the query for the rights specified by *rgbstrActionsToQuery*.</span></span> <span data-ttu-id="fd26d-138">Si une action est autorisée, l’élément correspondant est défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="fd26d-138">If an action is allowed, the corresponding element is set to zero.</span></span> <span data-ttu-id="fd26d-139">Si une action n’est pas autorisée, l’élément est défini sur une ou plusieurs valeurs de l’énumération des [**\_ \_ \_ \_ résultats de requête autorisés par l’action DRM**](drm-action-allowed-query-results.md) combinées à l’aide de l’opération or au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="fd26d-139">If an action is not allowed, the element is set to one or more values of the [**DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS**](drm-action-allowed-query-results.md) enumeration combined by using the bitwise OR operation.</span></span> <span data-ttu-id="fd26d-140">Ce tableau doit contenir autant d’éléments que ce qui est spécifié par *cActionsToQuery*.</span><span class="sxs-lookup"><span data-stu-id="fd26d-140">This array must contain as many elements as specified by *cActionsToQuery*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd26d-141">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fd26d-141">Return value</span></span>

<span data-ttu-id="fd26d-142">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="fd26d-142">The method returns an **HRESULT**.</span></span> <span data-ttu-id="fd26d-143">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="fd26d-143">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="fd26d-144">Code de retour</span><span class="sxs-lookup"><span data-stu-id="fd26d-144">Return code</span></span>                                                                          | <span data-ttu-id="fd26d-145">Description</span><span class="sxs-lookup"><span data-stu-id="fd26d-145">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="fd26d-146"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fd26d-146"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="fd26d-147">S_OK</span><span class="sxs-lookup"><span data-stu-id="fd26d-147">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fd26d-148">Notes</span><span class="sxs-lookup"><span data-stu-id="fd26d-148">Remarks</span></span>

<span data-ttu-id="fd26d-149">Lorsque vous interrogez des droits de lecture et de copie, vous obtiendrez des résultats plus précis en définissant les paramètres environnementaux.</span><span class="sxs-lookup"><span data-stu-id="fd26d-149">When querying for play and copy rights, you will get more accurate results by first setting environmental parameters.</span></span> <span data-ttu-id="fd26d-150">Utilisez la méthode [**SetActionAllowedQueryParams**](iwmdrmlicensequery-setactionallowedqueryparams.md) pour définir les paramètres d’environnement.</span><span class="sxs-lookup"><span data-stu-id="fd26d-150">Use the [**SetActionAllowedQueryParams**](iwmdrmlicensequery-setactionallowedqueryparams.md) method to set the environmental parameters.</span></span> <span data-ttu-id="fd26d-151">Les résultats des requêtes pour le droit de gravure ne sont pas affectés par les paramètres environnementaux. vous pouvez utiliser les valeurs par défaut en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="fd26d-151">The results of queries for the burn right are unaffected by the environmental parameters; you can safely use the defaults.</span></span>

<span data-ttu-id="fd26d-152">Les résultats retournés par la méthode **QueryActionAllowed** sont agrégés à partir de zéro ou de plusieurs licences dans le magasin de licences local.</span><span class="sxs-lookup"><span data-stu-id="fd26d-152">The results returned by the **QueryActionAllowed** method are aggregated from zero or more licenses in the local license store.</span></span> <span data-ttu-id="fd26d-153">La méthode peut ne pas effectuer de recherche dans toutes les licences qui s’appliquent à l’ID de clé si elle rencontre un résultat activé.</span><span class="sxs-lookup"><span data-stu-id="fd26d-153">The method may not search all of the licenses that apply to the Key ID if it encounters an enabled result.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd26d-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd26d-154">Requirements</span></span>



| <span data-ttu-id="fd26d-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd26d-155">Requirement</span></span> | <span data-ttu-id="fd26d-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd26d-156">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd26d-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd26d-157">Header</span></span><br/>  | <dl> <span data-ttu-id="fd26d-158"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd26d-158"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="fd26d-159">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fd26d-159">Library</span></span><br/> | <dl> <span data-ttu-id="fd26d-160"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd26d-160"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd26d-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd26d-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd26d-162">**Interface IWMDRMLicenseQuery**</span><span class="sxs-lookup"><span data-stu-id="fd26d-162">**IWMDRMLicenseQuery Interface**</span></span>](iwmdrmlicensequery.md)
</dt> <dt>

[<span data-ttu-id="fd26d-163">**Interrogation des informations de droits simples**</span><span class="sxs-lookup"><span data-stu-id="fd26d-163">**Querying for Simple Rights Information**</span></span>](querying-for-simple-rights-information.md)
</dt> </dl>

 

 





