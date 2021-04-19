---
title: Méthode IWMPMediaCollection2 getStringCollectionByQuery
description: La méthode getStringCollectionByQuery retourne une interface IWMPStringCollection qui fournit l’accès à l’ensemble de toutes les valeurs de chaîne pour un attribut spécifié qui correspondent aux conditions de la requête.
ms.assetid: 2d3b29af-0b6c-4405-8334-9a47a30ff6de
keywords:
- méthode getStringCollectionByQuery lecteur Windows Media
- méthode getStringCollectionByQuery lecteur Windows Media, interface IWMPMediaCollection2
- Interface IWMPMediaCollection2 lecteur Windows Media, méthode getStringCollectionByQuery
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getStringCollectionByQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 322781bc9ddec3e6f8d74d7229f16ce38e519f05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535254"
---
# <a name="iwmpmediacollection2getstringcollectionbyquery-method"></a><span data-ttu-id="eb1e7-106">IWMPMediaCollection2 :: getStringCollectionByQuery, méthode</span><span class="sxs-lookup"><span data-stu-id="eb1e7-106">IWMPMediaCollection2::getStringCollectionByQuery method</span></span>

<span data-ttu-id="eb1e7-107">La `getStringCollectionByQuery` méthode retourne une interface **IWMPStringCollection** qui fournit l’accès à l’ensemble de toutes les valeurs de chaîne pour un attribut spécifié qui correspondent aux conditions de la requête.</span><span class="sxs-lookup"><span data-stu-id="eb1e7-107">The `getStringCollectionByQuery` method returns an **IWMPStringCollection** interface that provides access to the set of all string values for a specified attribute that match the query conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb1e7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb1e7-108">Syntax</span></span>


```CSharp
public IWMPStringCollection getStringCollectionByQuery(
  System.String bstrAttribute,
  IWMPQuery pQuery,
  System.String bstrMediaType,
  System.String bstrSortAttribute,
  System.Boolean fSortAscending
);
```


```VB

Public Function getStringCollectionByQuery( _
  ByVal bstrAttribute As System.String, _
  ByVal pQuery As IWMPQuery, _
  ByVal bstrMediaType As System.String, _
  ByVal bstrSortAttribute As System.String, _
  ByVal fSortAscending As System.Boolean _
) As IWMPStringCollection
Implements IWMPMediaCollection2.getStringCollectionByQuery
```





## <a name="parameters"></a><span data-ttu-id="eb1e7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb1e7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb1e7-110">*bstrAttribute* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb1e7-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb1e7-111">**System. String** qui est le nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="eb1e7-111">The **System.String** that is the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="eb1e7-112">*pQuery* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb1e7-112">*pQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb1e7-113">Interface **wmplib. IWMPQuery** qui correspond à la requête qui définit les conditions utilisées pour récupérer la collection de chaînes.</span><span class="sxs-lookup"><span data-stu-id="eb1e7-113">The **WMPLib.IWMPQuery** interface that is the query that defines the conditions used to retrieve the string collection.</span></span>

</dd> <dt>

<span data-ttu-id="eb1e7-114">*bstrMediaType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb1e7-114">*bstrMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb1e7-115">**System. String** qui est le type de média.</span><span class="sxs-lookup"><span data-stu-id="eb1e7-115">The **System.String** that is the media type.</span></span> <span data-ttu-id="eb1e7-116">Doit contenir l’une des valeurs suivantes : « audio », « Video », « photo », « playlist » ou « other ».</span><span class="sxs-lookup"><span data-stu-id="eb1e7-116">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> <dt>

<span data-ttu-id="eb1e7-117">*bstrSortAttribute* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb1e7-117">*bstrSortAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb1e7-118">**System. String** qui est le nom d’attribut utilisé pour le tri.</span><span class="sxs-lookup"><span data-stu-id="eb1e7-118">The **System.String** that is the attribute name used for sorting.</span></span> <span data-ttu-id="eb1e7-119">Une chaîne de longueur nulle ("") signifie qu’aucun tri n’est appliqué.</span><span class="sxs-lookup"><span data-stu-id="eb1e7-119">A zero-length string ("") means no sorting is applied.</span></span>

</dd> <dt>

<span data-ttu-id="eb1e7-120">*fSortAscending* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb1e7-120">*fSortAscending* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb1e7-121">Valeur **System. Boolean** qui indique si l’ensemble de valeurs de chaîne doit être trié par ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="eb1e7-121">The **System.Boolean** value that indicates whether the set of string values must be sorted in ascending order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb1e7-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb1e7-122">Return value</span></span>

<span data-ttu-id="eb1e7-123">Interface **wmplib. IWMPStringCollection** pour le jeu récupéré de valeurs de chaîne.</span><span class="sxs-lookup"><span data-stu-id="eb1e7-123">A **WMPLib.IWMPStringCollection** interface for the retrieved set of string values.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb1e7-124">Notes</span><span class="sxs-lookup"><span data-stu-id="eb1e7-124">Remarks</span></span>

<span data-ttu-id="eb1e7-125">Les requêtes composées utilisant **IWMPQuery** ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="eb1e7-125">Compound queries using **IWMPQuery** are not case sensitive.</span></span>

<span data-ttu-id="eb1e7-126">Lorsque la requête composée spécifiée par le paramètre *pQuery* contient une condition construite sur l’attribut **MediaType** , cette condition est ignorée.</span><span class="sxs-lookup"><span data-stu-id="eb1e7-126">When the compound query specified by the *pQuery* parameter contains a condition built on the **MediaType** attribute, that condition is ignored.</span></span> <span data-ttu-id="eb1e7-127">La valeur du paramètre *bstrMediaType* est toujours utilisée.</span><span class="sxs-lookup"><span data-stu-id="eb1e7-127">The value for the *bstrMediaType* parameter is always used.</span></span> <span data-ttu-id="eb1e7-128">Par exemple, si la requête composée contient la condition « MediaType est égal à audio » et que la valeur du paramètre *bstrMediaType* est « Video », la sélection résultante contiendra uniquement les éléments vidéo.</span><span class="sxs-lookup"><span data-stu-id="eb1e7-128">For example, if the compound query contains the condition "MediaType Equals audio" and the value for the *bstrMediaType* parameter is "video", the resulting playlist will contain only video items.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb1e7-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb1e7-129">Requirements</span></span>



| <span data-ttu-id="eb1e7-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb1e7-130">Requirement</span></span> | <span data-ttu-id="eb1e7-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb1e7-131">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb1e7-132">Version</span><span class="sxs-lookup"><span data-stu-id="eb1e7-132">Version</span></span><br/>   | <span data-ttu-id="eb1e7-133">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="eb1e7-133">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="eb1e7-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="eb1e7-134">Namespace</span></span><br/> | <span data-ttu-id="eb1e7-135">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="eb1e7-135">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="eb1e7-136">Assembly</span><span class="sxs-lookup"><span data-stu-id="eb1e7-136">Assembly</span></span><br/>  | <dl> <span data-ttu-id="eb1e7-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="eb1e7-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb1e7-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb1e7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb1e7-139">**Interface IWMPMediaCollection2 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="eb1e7-139">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="eb1e7-140">**Interface IWMPQuery (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="eb1e7-140">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="eb1e7-141">**Interface IWMPStringCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="eb1e7-141">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="eb1e7-142">**MediaType (attribut)**</span><span class="sxs-lookup"><span data-stu-id="eb1e7-142">**MediaType Attribute**</span></span>](mediatype-attribute.md)
</dt> </dl>

 

 





