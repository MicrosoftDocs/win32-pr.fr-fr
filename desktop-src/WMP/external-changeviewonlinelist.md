---
title: External. changeViewOnlineList, méthode
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. changeViewOnlineList, méthode
ms.assetid: d7a45ced-431f-4d35-8c9c-c6eeba6fcbf3
keywords:
- méthode changeViewOnlineList lecteur Windows Media
- méthode changeViewOnlineList lecteur Windows Media, classe externe
- Classe externe lecteur Windows Media, méthode changeViewOnlineList
topic_type:
- apiref
api_name:
- External.changeViewOnlineList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75e36adfa79b62863c3de78acf2adbd65011417b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541673"
---
# <a name="externalchangeviewonlinelist-method"></a><span data-ttu-id="8ba54-107">External. changeViewOnlineList, méthode</span><span class="sxs-lookup"><span data-stu-id="8ba54-107">External.changeViewOnlineList method</span></span>

> [!Note]  
> <span data-ttu-id="8ba54-108">Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="8ba54-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="8ba54-109">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8ba54-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="8ba54-110">La méthode **changeViewOnlineList** modifie la vue dans le lecteur Windows Media pour afficher une liste générée dynamiquement par le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="8ba54-110">The **changeViewOnlineList** method changes the view in Windows Media Player to display a list generated dynamically by the online store.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ba54-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ba54-111">Syntax</span></span>


```JScript
External.changeViewOnlineList(
  LibraryLocationType,
  LibraryLocationID,
  Params,
  FriendlyName,
  ListType,
  ViewMode
)
```



## <a name="parameters"></a><span data-ttu-id="8ba54-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ba54-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ba54-113">*LibraryLocationType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8ba54-113">*LibraryLocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba54-114">[Constante d’emplacement de bibliothèque](library-location-constants.md) qui spécifie le type de la nouvelle vue.</span><span class="sxs-lookup"><span data-stu-id="8ba54-114">A [library location constant](library-location-constants.md) that specifies the type of the new view.</span></span> <span data-ttu-id="8ba54-115">Par exemple, la constante CPGenreID spécifie que la nouvelle vue affichera un genre particulier.</span><span class="sxs-lookup"><span data-stu-id="8ba54-115">For example, the constant CPGenreID specifies that the new view will show a particular genre.</span></span>

</dd> <dt>

<span data-ttu-id="8ba54-116">*LibraryLocationID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8ba54-116">*LibraryLocationID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba54-117">**Chaîne** contenant l’ID de l’élément spécifique à afficher dans la nouvelle vue.</span><span class="sxs-lookup"><span data-stu-id="8ba54-117">**String** containing the ID of the specific item to show in the new view.</span></span> <span data-ttu-id="8ba54-118">Par exemple, si *LibraryLocationType* est CPGenreID, ce paramètre spécifie l’ID du genre à afficher dans la nouvelle vue.</span><span class="sxs-lookup"><span data-stu-id="8ba54-118">For example, if *LibraryLocationType* is CPGenreID, then this parameter specifies the ID of the genre to show in the new view.</span></span> <span data-ttu-id="8ba54-119">Cette chaîne peut être vide.</span><span class="sxs-lookup"><span data-stu-id="8ba54-119">This string can be empty.</span></span>

</dd> <dt>

<span data-ttu-id="8ba54-120">*Paramètres* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8ba54-120">*Params* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba54-121">**Chaîne** contenant les paramètres transmis par le lecteur Windows Media au plug-in du magasin en ligne en appelant [IWMPContentPartner :: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate).</span><span class="sxs-lookup"><span data-stu-id="8ba54-121">**String** containing parameters that Windows Media Player passes along to the online store's plug-in by calling [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate).</span></span> <span data-ttu-id="8ba54-122">Ces paramètres ne sont pas interprétés par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8ba54-122">These parameters are not interpreted by Windows Media Player.</span></span> <span data-ttu-id="8ba54-123">Ils sont créés par le magasin en ligne et ont une signification uniquement pour le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="8ba54-123">They are created by the online store and have meaning only to the online store.</span></span> <span data-ttu-id="8ba54-124">Cette chaîne peut être vide</span><span class="sxs-lookup"><span data-stu-id="8ba54-124">This string can be empty</span></span>

</dd> <dt>

<span data-ttu-id="8ba54-125">*FriendlyName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8ba54-125">*FriendlyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba54-126">**Chaîne** contenant un nom convivial, à afficher par le lecteur Windows Media, pour la liste dynamique.</span><span class="sxs-lookup"><span data-stu-id="8ba54-126">**String** containing a friendly name, to be displayed by Windows Media Player, for the dynamic list.</span></span>

</dd> <dt>

<span data-ttu-id="8ba54-127">*ListType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8ba54-127">*ListType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba54-128">Constante d’emplacement de bibliothèque qui spécifie le type des éléments de la liste générée dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="8ba54-128">A library location constant that specifies the type of the items in the dynamically generated list.</span></span> <span data-ttu-id="8ba54-129">Par exemple, si la valeur de ce paramètre est CPTrackID, la liste dynamique contient des pistes.</span><span class="sxs-lookup"><span data-stu-id="8ba54-129">For example, if the value of this parameter is CPTrackID, then the dynamic list will contain tracks.</span></span>

</dd> <dt>

<span data-ttu-id="8ba54-130">*ViewMode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8ba54-130">*ViewMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba54-131">**Chaîne** qui spécifie le mode utilisé par le lecteur Windows Media pour afficher la liste dynamique.</span><span class="sxs-lookup"><span data-stu-id="8ba54-131">**String** that specifies the mode that Windows Media Player will use to display the dynamic list.</span></span> <span data-ttu-id="8ba54-132">L’appelant doit définir ce paramètre sur l’une des valeurs suivantes, qui sont définies dans contentpartner. h :</span><span class="sxs-lookup"><span data-stu-id="8ba54-132">The caller must set this parameter to one of the following values, which are defined in contentpartner.h:</span></span>

<span data-ttu-id="8ba54-133">ViewModeReport</span><span class="sxs-lookup"><span data-stu-id="8ba54-133">ViewModeReport</span></span>

<span data-ttu-id="8ba54-134">ViewModeDetails</span><span class="sxs-lookup"><span data-stu-id="8ba54-134">ViewModeDetails</span></span>

<span data-ttu-id="8ba54-135">ViewModeIcon</span><span class="sxs-lookup"><span data-stu-id="8ba54-135">ViewModeIcon</span></span>

<span data-ttu-id="8ba54-136">ViewModeTile</span><span class="sxs-lookup"><span data-stu-id="8ba54-136">ViewModeTile</span></span>

<span data-ttu-id="8ba54-137">ViewModeOrderedList</span><span class="sxs-lookup"><span data-stu-id="8ba54-137">ViewModeOrderedList</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ba54-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8ba54-138">Return value</span></span>

<span data-ttu-id="8ba54-139">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8ba54-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ba54-140">Notes</span><span class="sxs-lookup"><span data-stu-id="8ba54-140">Remarks</span></span>

<span data-ttu-id="8ba54-141">Lorsque le script sur une page de découverte appelle **changeViewOnlineList**, le lecteur Windows Media transmet certains des paramètres aux méthodes [IWMPContentPartner :: GetListContents](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents) et [IWMPContentPartner :: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) , qui sont implémentées par le plug-in du magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="8ba54-141">When script on a discovery page calls **changeViewOnlineList**, Windows Media Player passes some of the parameters along to the [IWMPContentPartner::GetListContents](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents) and [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) methods, which are implemented by the online store's plug-in.</span></span> <span data-ttu-id="8ba54-142">Le tableau suivant montre la correspondance entre les paramètres des trois méthodes.</span><span class="sxs-lookup"><span data-stu-id="8ba54-142">The following table shows the correspondence between the parameters of the three methods.</span></span>



| <span data-ttu-id="8ba54-143">paramètre changeViewOnlineList</span><span class="sxs-lookup"><span data-stu-id="8ba54-143">changeViewOnlineList parameter</span></span> | <span data-ttu-id="8ba54-144">Paramètre GetListContents</span><span class="sxs-lookup"><span data-stu-id="8ba54-144">GetListContents parameter</span></span> | <span data-ttu-id="8ba54-145">Paramètre GetTemplate</span><span class="sxs-lookup"><span data-stu-id="8ba54-145">GetTemplate parameter</span></span> |
|--------------------------------|---------------------------|-----------------------|
| <span data-ttu-id="8ba54-146">*LocationType (*</span><span class="sxs-lookup"><span data-stu-id="8ba54-146">*LocationType*</span></span>                 | <span data-ttu-id="8ba54-147">*location*</span><span class="sxs-lookup"><span data-stu-id="8ba54-147">*location*</span></span>                | <span data-ttu-id="8ba54-148">*location*</span><span class="sxs-lookup"><span data-stu-id="8ba54-148">*location*</span></span>            |
| <span data-ttu-id="8ba54-149">*LocationID*</span><span class="sxs-lookup"><span data-stu-id="8ba54-149">*LocationID*</span></span>                   | <span data-ttu-id="8ba54-150">*pContext*</span><span class="sxs-lookup"><span data-stu-id="8ba54-150">*pContext*</span></span>                | <span data-ttu-id="8ba54-151">*pContext*</span><span class="sxs-lookup"><span data-stu-id="8ba54-151">*pContext*</span></span>            |
| <span data-ttu-id="8ba54-152">*Params*</span><span class="sxs-lookup"><span data-stu-id="8ba54-152">*Params*</span></span>                       | <span data-ttu-id="8ba54-153">*bstrParams*</span><span class="sxs-lookup"><span data-stu-id="8ba54-153">*bstrParams*</span></span>              | <span data-ttu-id="8ba54-154">*bstrViewParams*</span><span class="sxs-lookup"><span data-stu-id="8ba54-154">*bstrViewParams*</span></span>      |
| <span data-ttu-id="8ba54-155">*Type*</span><span class="sxs-lookup"><span data-stu-id="8ba54-155">*ListType*</span></span>                     | <span data-ttu-id="8ba54-156">*bstrListType*</span><span class="sxs-lookup"><span data-stu-id="8ba54-156">*bstrListType*</span></span>            | <span data-ttu-id="8ba54-157">Non applicable</span><span class="sxs-lookup"><span data-stu-id="8ba54-157">not applicable</span></span>        |



 

<span data-ttu-id="8ba54-158">Étant donné que les trois méthodes indiquées dans le tableau précédent sont implémentées par le magasin en ligne, vous disposez d’une certaine flexibilité dans la façon dont vous utilisez les paramètres.</span><span class="sxs-lookup"><span data-stu-id="8ba54-158">Because all three of the methods shown in the preceding table are implemented by the online store, you have some flexibility in how you use the parameters.</span></span> <span data-ttu-id="8ba54-159">L’idée est que vous fournissez suffisamment d’informations pour que **GetListContents** détermine la liste qu’il doit récupérer et pour **GetTemplate** déterminer la page de découverte à afficher ensuite.</span><span class="sxs-lookup"><span data-stu-id="8ba54-159">The idea is that you provide enough information for **GetListContents** to determine which list it should retrieve and for **GetTemplate** to determine which discovery page should be displayed next.</span></span> <span data-ttu-id="8ba54-160">Les exemples suivants illustrent deux possibilités.</span><span class="sxs-lookup"><span data-stu-id="8ba54-160">The following examples illustrate two possibilities.</span></span>

<span data-ttu-id="8ba54-161">**Exemple 1 : liste dynamique figurant dans le catalogue du magasin en ligne**</span><span class="sxs-lookup"><span data-stu-id="8ba54-161">**Example 1: A dynamic list that is in the online store's catalog**</span></span>

<span data-ttu-id="8ba54-162">Supposons que vous souhaitiez que le plug-in récupère le contenu de la liste dynamique dont l’ID est 6 dans le catalogue du magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="8ba54-162">Suppose you want the plug-in to get the contents of the dynamic list that has an ID of 6 in the online store's catalog.</span></span> <span data-ttu-id="8ba54-163">Supposons que la liste 6 est une liste de pistes.</span><span class="sxs-lookup"><span data-stu-id="8ba54-163">Assume that list 6 is a list of tracks.</span></span> <span data-ttu-id="8ba54-164">Vous pouvez fournir le plug-in avec suffisamment d’informations en effectuant l’appel suivant.</span><span class="sxs-lookup"><span data-stu-id="8ba54-164">You could provide the plug-in with enough information by making the following call.</span></span>


```C++
external.changeViewOnlineList(
   "CPListID", 6, "", 
   "Songs for Today", "CPTrackID", "ViewModeDetails");
```



<span data-ttu-id="8ba54-165">Notez que le paramètre *params* est vide. le plug-in a suffisamment d’informations dans les autres paramètres.</span><span class="sxs-lookup"><span data-stu-id="8ba54-165">Note that the *Params* parameter is empty; the plug-in has enough information in the other parameters.</span></span>

<span data-ttu-id="8ba54-166">**Exemple 2 : liste dynamique qui ne figure pas dans le catalogue du magasin en ligne**</span><span class="sxs-lookup"><span data-stu-id="8ba54-166">**Example 2: A dynamic list that is not in the online store's catalog**</span></span>

<span data-ttu-id="8ba54-167">Supposons que vous souhaitiez que le plug-in récupère le contenu d’une liste dynamique qui ne figure pas dans le catalogue du magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="8ba54-167">Suppose that you want the plug-in to get the contents of a dynamic list that is not in the online store's catalog.</span></span> <span data-ttu-id="8ba54-168">Peut-être avez-vous décidé d’avoir une liste dynamique qui comprend des chansons sélectionnées par un artiste particulier.</span><span class="sxs-lookup"><span data-stu-id="8ba54-168">Perhaps you have decided to have a dynamic list that includes songs picked by a particular artist.</span></span> <span data-ttu-id="8ba54-169">Supposons que l’artiste a un ID de 2 dans le catalogue du magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="8ba54-169">Assume the artist has an ID of 2 in the online store's catalog.</span></span> <span data-ttu-id="8ba54-170">Vous pouvez effectuer l’appel suivant.</span><span class="sxs-lookup"><span data-stu-id="8ba54-170">You could make the following call.</span></span>


```C++
external.changeViewOnlineList(
   "CPArtistID", 2, "songs picked by Sally", 
   "Sally Picks", "CPTrackID", "ViewModeDetails");
```



<span data-ttu-id="8ba54-171">Notez que les paramètres *LocationType (* et *LocationID* ne spécifient pas la liste.</span><span class="sxs-lookup"><span data-stu-id="8ba54-171">Note that the *LocationType* and *LocationID* parameters do not specify the list.</span></span> <span data-ttu-id="8ba54-172">Au lieu de cela, le paramètre *params* spécifie la liste.</span><span class="sxs-lookup"><span data-stu-id="8ba54-172">Instead, the *Params* parameter specifies the list.</span></span> <span data-ttu-id="8ba54-173">Les paramètres *LocationType (* et *LocationID* sont passés à **IWMPContentPartner :: GetListContents**, mais dans ce cas, **GetListContents** peut les ignorer.</span><span class="sxs-lookup"><span data-stu-id="8ba54-173">The *LocationType* and *LocationID* parameters are passed to **IWMPContentPartner::GetListContents**, but in this case, **GetListContents** can ignore them.</span></span> <span data-ttu-id="8ba54-174">Les paramètres *LocationType (* et *LocationID* sont également passés à **IWMPContentPartner :: GetTemplate**, qui peuvent les utiliser pour déterminer quelle page de découverte doit être affichée avec la liste dynamique.</span><span class="sxs-lookup"><span data-stu-id="8ba54-174">The *LocationType* and *LocationID* parameters are also passed to **IWMPContentPartner::GetTemplate**, which can use them to determine which discovery page should be displayed with the dynamic list.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ba54-175">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ba54-175">Requirements</span></span>



| <span data-ttu-id="8ba54-176">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ba54-176">Requirement</span></span> | <span data-ttu-id="8ba54-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ba54-177">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8ba54-178">Version</span><span class="sxs-lookup"><span data-stu-id="8ba54-178">Version</span></span><br/> | <span data-ttu-id="8ba54-179">Lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="8ba54-179">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="8ba54-180">DLL</span><span class="sxs-lookup"><span data-stu-id="8ba54-180">DLL</span></span><br/>     | <dl> <span data-ttu-id="8ba54-181"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ba54-181"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ba54-182">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ba54-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ba54-183">**Objet externe pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="8ba54-183">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="8ba54-184">**IWMPContentPartner::GetListContents**</span><span class="sxs-lookup"><span data-stu-id="8ba54-184">**IWMPContentPartner::GetListContents**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents)
</dt> <dt>

[<span data-ttu-id="8ba54-185">**IWMPContentPartnerCallback::AddListContents**</span><span class="sxs-lookup"><span data-stu-id="8ba54-185">**IWMPContentPartnerCallback::AddListContents**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-addlistcontents)
</dt> <dt>

[<span data-ttu-id="8ba54-186">**IWMPContentPartner::GetTemplate**</span><span class="sxs-lookup"><span data-stu-id="8ba54-186">**IWMPContentPartner::GetTemplate**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)
</dt> <dt>

[<span data-ttu-id="8ba54-187">**Emplacement et élément sélectionné**</span><span class="sxs-lookup"><span data-stu-id="8ba54-187">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





