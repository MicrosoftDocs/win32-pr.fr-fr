---
title: Méthode IWMPMediaCollection2 getPlaylistByQuery
description: La méthode getPlaylistByQuery retourne une interface IWMPPlaylist qui fournit l’accès aux éléments multimédias qui correspondent aux conditions de requête.
ms.assetid: ebbb631f-1faa-4c89-8c1d-cc2b128126b8
keywords:
- méthode getPlaylistByQuery lecteur Windows Media
- méthode getPlaylistByQuery lecteur Windows Media, interface IWMPMediaCollection2
- Interface IWMPMediaCollection2 lecteur Windows Media, méthode getPlaylistByQuery
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getPlaylistByQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109f6e49e77d1cfa8c6d3b45bef1d011faf21a8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525291"
---
# <a name="iwmpmediacollection2getplaylistbyquery-method"></a><span data-ttu-id="6b45a-106">IWMPMediaCollection2 :: getPlaylistByQuery, méthode</span><span class="sxs-lookup"><span data-stu-id="6b45a-106">IWMPMediaCollection2::getPlaylistByQuery method</span></span>

<span data-ttu-id="6b45a-107">La `getPlaylistByQuery` méthode retourne une interface **IWMPPlaylist** qui fournit l’accès aux éléments multimédias qui correspondent aux conditions de requête.</span><span class="sxs-lookup"><span data-stu-id="6b45a-107">The `getPlaylistByQuery` method returns an **IWMPPlaylist** interface that provides access to media items that match the query conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b45a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6b45a-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getPlaylistByQuery(
  IWMPQuery pQuery,
  System.String bstrMediaType,
  System.String bstrSortAttribute,
  System.Boolean fSortAscending
);
```


```VB

Public Function getPlaylistByQuery( _
  ByVal pQuery As IWMPQuery, _
  ByVal bstrMediaType As System.String, _
  ByVal bstrSortAttribute As System.String, _
  ByVal fSortAscending As System.Boolean _
) As IWMPPlaylist
Implements IWMPMediaCollection2.getPlaylistByQuery
```





## <a name="parameters"></a><span data-ttu-id="6b45a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6b45a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b45a-110">*pQuery* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6b45a-110">*pQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b45a-111">Interface **wmplib. IWMPQuery** qui représente la requête.</span><span class="sxs-lookup"><span data-stu-id="6b45a-111">The **WMPLib.IWMPQuery** interface that represents the query.</span></span>

</dd> <dt>

<span data-ttu-id="6b45a-112">*bstrMediaType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6b45a-112">*bstrMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b45a-113">**System. String** qui est le type de média.</span><span class="sxs-lookup"><span data-stu-id="6b45a-113">The **System.String** that is the media type.</span></span> <span data-ttu-id="6b45a-114">Doit contenir l’une des valeurs suivantes : « audio », « Video », « photo », « playlist » ou « other ».</span><span class="sxs-lookup"><span data-stu-id="6b45a-114">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> <dt>

<span data-ttu-id="6b45a-115">*bstrSortAttribute* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6b45a-115">*bstrSortAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b45a-116">**System. String** qui est le nom d’attribut utilisé pour le tri.</span><span class="sxs-lookup"><span data-stu-id="6b45a-116">The **System.String** that is the attribute name used for sorting.</span></span> <span data-ttu-id="6b45a-117">Une chaîne de longueur nulle ("") signifie qu’aucun tri n’est appliqué.</span><span class="sxs-lookup"><span data-stu-id="6b45a-117">A zero-length string ("") means no sorting is applied.</span></span>

</dd> <dt>

<span data-ttu-id="6b45a-118">*fSortAscending* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6b45a-118">*fSortAscending* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b45a-119">Valeur **System. Boolean** qui indique si la sélection doit être triée dans l’ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="6b45a-119">The **System.Boolean** value that indicates whether the playlist must be sorted in ascending order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b45a-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6b45a-120">Return value</span></span>

<span data-ttu-id="6b45a-121">Interface **wmplib. IWMPPlaylist** pour la sélection récupérée.</span><span class="sxs-lookup"><span data-stu-id="6b45a-121">A **WMPLib.IWMPPlaylist** interface for the retrieved playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b45a-122">Notes</span><span class="sxs-lookup"><span data-stu-id="6b45a-122">Remarks</span></span>

<span data-ttu-id="6b45a-123">Les requêtes composées utilisant **IWMPQuery** ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="6b45a-123">Compound queries using **IWMPQuery** are not case sensitive.</span></span>

<span data-ttu-id="6b45a-124">Lorsque la requête composée spécifiée par le paramètre *pQuery* contient une condition construite sur l’attribut **MediaType** , cette condition est ignorée.</span><span class="sxs-lookup"><span data-stu-id="6b45a-124">When the compound query specified by the *pQuery* parameter contains a condition built on the **MediaType** attribute, that condition is ignored.</span></span> <span data-ttu-id="6b45a-125">La valeur du paramètre *bstrMediaType* est toujours utilisée.</span><span class="sxs-lookup"><span data-stu-id="6b45a-125">The value for the *bstrMediaType* parameter is always used.</span></span> <span data-ttu-id="6b45a-126">Par exemple, si la requête composée contient la condition « MediaType est égal à audio » et que la valeur du paramètre *bstrMediaType* est « Video », la sélection résultante contiendra uniquement les éléments vidéo.</span><span class="sxs-lookup"><span data-stu-id="6b45a-126">For example, if the compound query contains the condition "MediaType Equals audio" and the value for the *bstrMediaType* parameter is "video", the resulting playlist will contain only video items.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b45a-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6b45a-127">Requirements</span></span>



| <span data-ttu-id="6b45a-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6b45a-128">Requirement</span></span> | <span data-ttu-id="6b45a-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b45a-129">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b45a-130">Version</span><span class="sxs-lookup"><span data-stu-id="6b45a-130">Version</span></span><br/>   | <span data-ttu-id="6b45a-131">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="6b45a-131">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="6b45a-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6b45a-132">Namespace</span></span><br/> | <span data-ttu-id="6b45a-133">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="6b45a-133">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6b45a-134">Assembly</span><span class="sxs-lookup"><span data-stu-id="6b45a-134">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6b45a-135"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6b45a-135"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b45a-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b45a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b45a-137">**Interface IWMPMediaCollection2 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="6b45a-137">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6b45a-138">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="6b45a-138">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6b45a-139">**Interface IWMPQuery (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="6b45a-139">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6b45a-140">**MediaType (attribut)**</span><span class="sxs-lookup"><span data-stu-id="6b45a-140">**MediaType Attribute**</span></span>](mediatype-attribute.md)
</dt> </dl>

 

 





