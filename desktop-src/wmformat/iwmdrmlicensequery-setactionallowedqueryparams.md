---
title: Méthode IWMDRMLicenseQuery SetActionAllowedQueryParams (wmdrmsdk. h)
description: La méthode SetActionAllowedQueryParams définit des informations spécifiques à l’environnement pour obtenir des résultats de requête plus précis lors de l’utilisation de la méthode QueryActionAllowed.
ms.assetid: 1c8f9d4e-999d-4d7c-87fd-9d30e432350c
keywords:
- Méthode SetActionAllowedQueryParams format Windows Media
- Méthode SetActionAllowedQueryParams format Windows Media, interface IWMDRMLicenseQuery
- Interface IWMDRMLicenseQuery Windows Media format, méthode SetActionAllowedQueryParams
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.SetActionAllowedQueryParams
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a83a28c4d9f3758b711c43ddd83a509c58f8ea8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532956"
---
# <a name="iwmdrmlicensequerysetactionallowedqueryparams-method"></a><span data-ttu-id="adca1-106">IWMDRMLicenseQuery :: SetActionAllowedQueryParams, méthode</span><span class="sxs-lookup"><span data-stu-id="adca1-106">IWMDRMLicenseQuery::SetActionAllowedQueryParams method</span></span>

<span data-ttu-id="adca1-107">La méthode **SetActionAllowedQueryParams** définit des informations spécifiques à l’environnement pour obtenir des résultats de requête plus précis lors de l’utilisation de la méthode [**QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) .</span><span class="sxs-lookup"><span data-stu-id="adca1-107">The **SetActionAllowedQueryParams** method sets environment-specific information for more accurate query results when using the [**QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="adca1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="adca1-108">Syntax</span></span>


```C++
HRESULT SetActionAllowedQueryParams(
  [in] BOOL  fIsMF,
  [in] DWORD dwAppSecLevel,
  [in] BOOL  fHasSerialNumber,
  [in] BSTR  bstrDeviceCert
);
```



## <a name="parameters"></a><span data-ttu-id="adca1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="adca1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adca1-110">*fIsMF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="adca1-110">*fIsMF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adca1-111">Spécifie si le contenu sera rendu à l’aide des objets du kit de développement logiciel (SDK) Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="adca1-111">Specifies whether the content will be rendered by using the objects of the Microsoft Media Foundation SDK.</span></span> <span data-ttu-id="adca1-112">**False** indique le rendu par les objets du kit de développement logiciel (SDK) de format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="adca1-112">**FALSE** indicates rendering by the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="adca1-113">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="adca1-113">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="adca1-114">*dwAppSecLevel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="adca1-114">*dwAppSecLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adca1-115">Niveau de sécurité de l’application de requête.</span><span class="sxs-lookup"><span data-stu-id="adca1-115">Security level of the querying application.</span></span> <span data-ttu-id="adca1-116">Cette valeur n’est importante que si les objets du kit de développement logiciel (SDK) du format Windows Media sont utilisés, auquel cas *fIsMF* doit avoir la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="adca1-116">This value is only important if the objects of the Windows Media Format SDK will be used, in which case *fIsMF* should be set to **FALSE**.</span></span> <span data-ttu-id="adca1-117">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="adca1-117">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="adca1-118">*fHasSerialNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="adca1-118">*fHasSerialNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adca1-119">Spécifie si l’appareil cible pour une opération de copie a un numéro de série.</span><span class="sxs-lookup"><span data-stu-id="adca1-119">Specifies whether the target device for a copy operation has a serial number.</span></span> <span data-ttu-id="adca1-120">Ce paramètre est facultatif et s’applique uniquement aux requêtes pour les opérations de copie.</span><span class="sxs-lookup"><span data-stu-id="adca1-120">This parameter is optional and only applies to queries for copy operations.</span></span>

</dd> <dt>

<span data-ttu-id="adca1-121">*bstrDeviceCert* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="adca1-121">*bstrDeviceCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adca1-122">Certificat d’appareil de l’appareil cible lors de l’utilisation de Windows Media DRM pour les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="adca1-122">Device certificate of the target device when using Windows Media DRM for Portable Devices.</span></span> <span data-ttu-id="adca1-123">Ce paramètre est facultatif et s’applique uniquement aux requêtes pour les opérations de copie.</span><span class="sxs-lookup"><span data-stu-id="adca1-123">This parameter is optional and only applies to queries for copy operations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adca1-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="adca1-124">Return value</span></span>

<span data-ttu-id="adca1-125">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="adca1-125">The method returns an **HRESULT**.</span></span> <span data-ttu-id="adca1-126">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="adca1-126">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="adca1-127">Code de retour</span><span class="sxs-lookup"><span data-stu-id="adca1-127">Return code</span></span>                                                                          | <span data-ttu-id="adca1-128">Description</span><span class="sxs-lookup"><span data-stu-id="adca1-128">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="adca1-129"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="adca1-129"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="adca1-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="adca1-130">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="adca1-131">Notes</span><span class="sxs-lookup"><span data-stu-id="adca1-131">Remarks</span></span>

<span data-ttu-id="adca1-132">Aucun.</span><span class="sxs-lookup"><span data-stu-id="adca1-132">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="adca1-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="adca1-133">Requirements</span></span>



| <span data-ttu-id="adca1-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="adca1-134">Requirement</span></span> | <span data-ttu-id="adca1-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="adca1-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="adca1-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="adca1-136">Header</span></span><br/>  | <dl> <span data-ttu-id="adca1-137"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="adca1-137"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="adca1-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="adca1-138">Library</span></span><br/> | <dl> <span data-ttu-id="adca1-139"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="adca1-139"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adca1-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="adca1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adca1-141">**Interface IWMDRMLicenseQuery**</span><span class="sxs-lookup"><span data-stu-id="adca1-141">**IWMDRMLicenseQuery Interface**</span></span>](iwmdrmlicensequery.md)
</dt> <dt>

[<span data-ttu-id="adca1-142">**Interrogation pour obtenir des informations détaillées sur les droits**</span><span class="sxs-lookup"><span data-stu-id="adca1-142">**Querying for Detailed Rights Information**</span></span>](querying-for-detailed-rights-information.md)
</dt> </dl>

 

 





