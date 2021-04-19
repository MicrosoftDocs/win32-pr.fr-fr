---
title: External. changeView, méthode
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La méthode changeView modifie la vue dans le lecteur Windows Media.
ms.assetid: bd9d7d4b-ee4c-4d7c-92ef-dd0b8ab46d9d
keywords:
- méthode changeView lecteur Windows Media
- méthode changeView lecteur Windows Media, classe externe
- Classe externe lecteur Windows Media, méthode changeView
topic_type:
- apiref
api_name:
- External.changeView
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35adb253d5dd14d755353c29f9278b1c122133d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532507"
---
# <a name="externalchangeview-method"></a><span data-ttu-id="e04cb-108">External. changeView, méthode</span><span class="sxs-lookup"><span data-stu-id="e04cb-108">External.changeView method</span></span>

> [!Note]  
> <span data-ttu-id="e04cb-109">Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="e04cb-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="e04cb-110">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="e04cb-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="e04cb-111">La méthode **changeView** modifie la vue dans le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e04cb-111">The **changeView** method changes the view in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="e04cb-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e04cb-112">Syntax</span></span>


```JScript
External.changeView(
  LibraryLocationType,
  LibraryLocationID,
  Filter,
  ViewParams
)
```



## <a name="parameters"></a><span data-ttu-id="e04cb-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e04cb-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e04cb-114">*LibraryLocationType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e04cb-114">*LibraryLocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e04cb-115">[Constante d’emplacement de bibliothèque](library-location-constants.md) qui spécifie le type de la nouvelle vue.</span><span class="sxs-lookup"><span data-stu-id="e04cb-115">A [library location constant](library-location-constants.md) that specifies the type of the new view.</span></span> <span data-ttu-id="e04cb-116">Par exemple, la constante CPGenreID spécifie que la nouvelle vue affichera un genre particulier.</span><span class="sxs-lookup"><span data-stu-id="e04cb-116">For example, the constant CPGenreID specifies that the new view will show a particular genre.</span></span>

</dd> <dt>

<span data-ttu-id="e04cb-117">*LibraryLocationID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e04cb-117">*LibraryLocationID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e04cb-118">**Chaîne** contenant l’ID de l’élément spécifique à afficher dans la nouvelle vue.</span><span class="sxs-lookup"><span data-stu-id="e04cb-118">**String** containing the ID of the specific item to show in the new view.</span></span> <span data-ttu-id="e04cb-119">Par exemple, si *LibraryLocationType* est CPGenreID, ce paramètre spécifie l’ID du genre à afficher dans la nouvelle vue.</span><span class="sxs-lookup"><span data-stu-id="e04cb-119">For example, if *LibraryLocationType* is CPGenreID, then this parameter specifies the ID of the genre to show in the new view.</span></span> <span data-ttu-id="e04cb-120">Cette chaîne peut être vide.</span><span class="sxs-lookup"><span data-stu-id="e04cb-120">This string can be empty.</span></span> <span data-ttu-id="e04cb-121">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="e04cb-121">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e04cb-122">*Filtre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e04cb-122">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e04cb-123">**Chaîne** contenant le filtre pour la nouvelle vue.</span><span class="sxs-lookup"><span data-stu-id="e04cb-123">**String** containing the filter for the new view.</span></span> <span data-ttu-id="e04cb-124">La vue sera filtrée comme si l’utilisateur avait entré ce texte dans le contrôle de roulette de mot du joueur.</span><span class="sxs-lookup"><span data-stu-id="e04cb-124">The view will be filtered as if the user had entered this text in the Player's word wheel control.</span></span> <span data-ttu-id="e04cb-125">Cette chaîne peut être vide.</span><span class="sxs-lookup"><span data-stu-id="e04cb-125">This string can be empty.</span></span>

</dd> <dt>

<span data-ttu-id="e04cb-126">*ViewParams* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e04cb-126">*ViewParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e04cb-127">**Chaîne** contenant les paramètres que le lecteur Windows Media met à disposition dans la nouvelle page de découverte qui s’affiche avec la nouvelle vue.</span><span class="sxs-lookup"><span data-stu-id="e04cb-127">**String** containing parameters that Windows Media Player makes available to the new discovery page that is displayed with the new view.</span></span> <span data-ttu-id="e04cb-128">Ces paramètres ne sont pas interprétés par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e04cb-128">These parameters are not interpreted by Windows Media Player.</span></span> <span data-ttu-id="e04cb-129">Ils sont créés par le magasin en ligne et ont une signification uniquement pour le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="e04cb-129">They are created by the online store and have meaning only to the online store.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e04cb-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e04cb-130">Return value</span></span>

<span data-ttu-id="e04cb-131">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e04cb-131">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e04cb-132">Notes</span><span class="sxs-lookup"><span data-stu-id="e04cb-132">Remarks</span></span>

<span data-ttu-id="e04cb-133">Dans certains cas, il est logique de définir le paramètre *LibraryLocationID* sur une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="e04cb-133">In some cases, it makes sense to set the *LibraryLocationID* parameter to the empty string.</span></span> <span data-ttu-id="e04cb-134">Par exemple, si vous définissez le paramètre *LibraryLocationType* sur AllCPAlbumIDs, la nouvelle vue représentera tous les albums.</span><span class="sxs-lookup"><span data-stu-id="e04cb-134">For example, if you set the *LibraryLocationType* parameter to AllCPAlbumIDs, the new view will represent all albums.</span></span> <span data-ttu-id="e04cb-135">Aucun album individuel n’est l’objectif de la nouvelle vue. il n’est donc pas nécessaire de fournir un ID d’album dans le paramètre *LibraryLocationID* .</span><span class="sxs-lookup"><span data-stu-id="e04cb-135">No individual album will be the focus of the new view, so there is no need to supply an album ID in the *LibraryLocationID* parameter.</span></span>

<span data-ttu-id="e04cb-136">Le paramètre *ViewParams* permet à une page de découverte de communiquer avec une autre page de découverte.</span><span class="sxs-lookup"><span data-stu-id="e04cb-136">The *ViewParams* parameter provides a way for a discovery page to communicate with another discovery page.</span></span> <span data-ttu-id="e04cb-137">Lorsque le script sur une page de découverte appelle **changeView**, le lecteur Windows Media ajuste son interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e04cb-137">When script on a discovery page calls **changeView**, Windows Media Player adjusts its user interface.</span></span> <span data-ttu-id="e04cb-138">Cet ajustement fait en sorte que le lecteur appelle la méthode [IWMPContentPartner :: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) du plug-in pour obtenir l’URL d’une nouvelle page de découverte.</span><span class="sxs-lookup"><span data-stu-id="e04cb-138">That adjustment causes the Player to call the plug-in's [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) method to get the URL of a new discovery page.</span></span> <span data-ttu-id="e04cb-139">La chaîne que la page de découverte d’origine transmet dans le paramètre *ViewParams* n’est pas passée à **GetTemplate**.</span><span class="sxs-lookup"><span data-stu-id="e04cb-139">The string that the original discovery page passes in the *ViewParams* parameter does not get passed to **GetTemplate**.</span></span> <span data-ttu-id="e04cb-140">Toutefois, la nouvelle page de découverte peut récupérer la chaîne *ViewParams* en appelant [External. viewParameters](external-viewparameters.md).</span><span class="sxs-lookup"><span data-stu-id="e04cb-140">However, the new discovery page can retrieve the *ViewParams* string by calling [External.viewParameters](external-viewparameters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e04cb-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e04cb-141">Requirements</span></span>



| <span data-ttu-id="e04cb-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e04cb-142">Requirement</span></span> | <span data-ttu-id="e04cb-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="e04cb-143">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e04cb-144">Version</span><span class="sxs-lookup"><span data-stu-id="e04cb-144">Version</span></span><br/> | <span data-ttu-id="e04cb-145">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="e04cb-145">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="e04cb-146">DLL</span><span class="sxs-lookup"><span data-stu-id="e04cb-146">DLL</span></span><br/>     | <dl> <span data-ttu-id="e04cb-147"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e04cb-147"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e04cb-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e04cb-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e04cb-149">**Objet externe pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="e04cb-149">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="e04cb-150">**External. changeViewOnlineList**</span><span class="sxs-lookup"><span data-stu-id="e04cb-150">**External.changeViewOnlineList**</span></span>](external-changeviewonlinelist.md)
</dt> <dt>

[<span data-ttu-id="e04cb-151">**External. libraryLocationID**</span><span class="sxs-lookup"><span data-stu-id="e04cb-151">**External.libraryLocationID**</span></span>](external-librarylocationid.md)
</dt> <dt>

[<span data-ttu-id="e04cb-152">**External. libraryLocationType**</span><span class="sxs-lookup"><span data-stu-id="e04cb-152">**External.libraryLocationType**</span></span>](external-librarylocationtype.md)
</dt> <dt>

[<span data-ttu-id="e04cb-153">**External. viewParameters**</span><span class="sxs-lookup"><span data-stu-id="e04cb-153">**External.viewParameters**</span></span>](external-viewparameters.md)
</dt> </dl>

 

 





