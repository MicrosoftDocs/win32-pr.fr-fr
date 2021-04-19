---
title: External. cancelNavigate, méthode
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. cancelNavigate, méthode
ms.assetid: e65d64fb-292c-4413-9727-b24609e78d68
keywords:
- méthode cancelNavigate lecteur Windows Media
- méthode cancelNavigate lecteur Windows Media, classe externe
- Classe externe lecteur Windows Media, méthode cancelNavigate
topic_type:
- apiref
api_name:
- External.cancelNavigate
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a6cbc0f749fd6ca33d78dfaed1d256634eb9c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541434"
---
# <a name="externalcancelnavigate-method"></a><span data-ttu-id="cbd42-107">External. cancelNavigate, méthode</span><span class="sxs-lookup"><span data-stu-id="cbd42-107">External.cancelNavigate method</span></span>

> [!Note]  
> <span data-ttu-id="cbd42-108">Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="cbd42-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="cbd42-109">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="cbd42-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="cbd42-110">La méthode **cancelNavigate** informe le lecteur Windows Media qu’il ne doit pas afficher de nouvelle page de découverte, même si la vue a été modifiée dans le lecteur.</span><span class="sxs-lookup"><span data-stu-id="cbd42-110">The **cancelNavigate** method informs Windows Media Player that it should not display a new discovery page even though the view has changed in the Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbd42-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cbd42-111">Syntax</span></span>


```JScript
External.cancelNavigate()
```



## <a name="parameters"></a><span data-ttu-id="cbd42-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cbd42-112">Parameters</span></span>

<span data-ttu-id="cbd42-113">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="cbd42-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cbd42-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cbd42-114">Return value</span></span>

<span data-ttu-id="cbd42-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="cbd42-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbd42-116">Notes</span><span class="sxs-lookup"><span data-stu-id="cbd42-116">Remarks</span></span>

<span data-ttu-id="cbd42-117">Lorsque la vue change dans le lecteur Windows Media, le lecteur appelle le plug-in de la boutique en ligne pour déterminer quelle page de découverte afficher ensuite.</span><span class="sxs-lookup"><span data-stu-id="cbd42-117">When the view changes in Windows Media Player, the Player calls the online store's plug-in to determine which discovery page to display next.</span></span> <span data-ttu-id="cbd42-118">Dans certains cas, toutefois, le magasin en ligne peut souhaiter que le lecteur continue à afficher la page de découverte existante.</span><span class="sxs-lookup"><span data-stu-id="cbd42-118">In some cases, however, the online store might want the Player to continue displaying the existing discovery page.</span></span> <span data-ttu-id="cbd42-119">Le processus suivant détermine si le lecteur affiche une nouvelle page de découverte :</span><span class="sxs-lookup"><span data-stu-id="cbd42-119">The following process determines whether the Player displays a new discovery page:</span></span>

1.  <span data-ttu-id="cbd42-120">Une action de l’utilisateur, que ce soit dans l’interface utilisateur du joueur ou sur la page de découverte, demande que le joueur modifie son affichage.</span><span class="sxs-lookup"><span data-stu-id="cbd42-120">An action by the user, either in the Player's user interface or on the discovery page, requests that the Player change its view.</span></span>
2.  <span data-ttu-id="cbd42-121">Le lecteur appelle la méthode [GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) du plug-in pour déterminer quelle page de découverte afficher ensuite.</span><span class="sxs-lookup"><span data-stu-id="cbd42-121">The Player calls the plug-in's [GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) method to determine which discovery page to display next.</span></span> <span data-ttu-id="cbd42-122">Le lecteur stocke l’URL de la nouvelle page de découverte, mais n’affiche pas la nouvelle page de découverte pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="cbd42-122">The Player stores the URL of the new discovery page but does not display the new discovery page at this time.</span></span>
3.  <span data-ttu-id="cbd42-123">Le lecteur déclenche l’événement [OnViewChange](external-onviewchange-event.md) .</span><span class="sxs-lookup"><span data-stu-id="cbd42-123">The Player raises the [OnViewChange](external-onviewchange-event.md) event.</span></span>
4.  <span data-ttu-id="cbd42-124">Si le gestionnaire d’événements **OnViewChange** sur la page de découverte appelle **CancelNavigate**, le lecteur n’affiche pas la page nouvelle détection (déterminée à l’étape 2).</span><span class="sxs-lookup"><span data-stu-id="cbd42-124">If the **OnViewChange** event handler on the discovery page calls **cancelNavigate**, the Player does not display the new discovery page (determined in step 2).</span></span> <span data-ttu-id="cbd42-125">Au lieu de cela, il continue d’afficher la page découverte existante.</span><span class="sxs-lookup"><span data-stu-id="cbd42-125">Instead, it continues to display the existing discovery page.</span></span> <span data-ttu-id="cbd42-126">Si le gestionnaire d’événements **OnViewChange** n’appelle pas **CancelNavigate**, le lecteur affiche la page nouvelle détection.</span><span class="sxs-lookup"><span data-stu-id="cbd42-126">If the **OnViewChange** event handler does not call **cancelNavigate**, the Player does display the new discovery page.</span></span>

<span data-ttu-id="cbd42-127">Supposons, par exemple, que le joueur affiche actuellement la vue d’un album avec une certaine piste sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="cbd42-127">For example, suppose the Player is currently displaying the view of an album with a certain track selected.</span></span> <span data-ttu-id="cbd42-128">Supposons également que la page détection en cours est la page qui représente l’intégralité de l’album.</span><span class="sxs-lookup"><span data-stu-id="cbd42-128">Also assume that the current discovery page is the page that represents the entire album.</span></span> <span data-ttu-id="cbd42-129">Si l’utilisateur clique sur une autre piste du même album, la vue du joueur change légèrement pour montrer que la nouvelle piste est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="cbd42-129">If the user clicks a different track from the same album, the Player's view changes slightly to show that the new track is selected.</span></span> <span data-ttu-id="cbd42-130">Mais il n’est pas nécessaire d’afficher une nouvelle page de découverte.</span><span class="sxs-lookup"><span data-stu-id="cbd42-130">But there is no need to display a new discovery page.</span></span> <span data-ttu-id="cbd42-131">La page de découverte qui représente l’intégralité de l’album est toujours la page appropriée à afficher par le lecteur.</span><span class="sxs-lookup"><span data-stu-id="cbd42-131">The discovery page that represents the entire album is still the appropriate page for the Player to display.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbd42-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cbd42-132">Requirements</span></span>



| <span data-ttu-id="cbd42-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cbd42-133">Requirement</span></span> | <span data-ttu-id="cbd42-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="cbd42-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cbd42-135">Version</span><span class="sxs-lookup"><span data-stu-id="cbd42-135">Version</span></span><br/> | <span data-ttu-id="cbd42-136">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="cbd42-136">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="cbd42-137">DLL</span><span class="sxs-lookup"><span data-stu-id="cbd42-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="cbd42-138"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbd42-138"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbd42-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cbd42-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbd42-140">**Objet externe pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="cbd42-140">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="cbd42-141">**External. changeViewOnlineList**</span><span class="sxs-lookup"><span data-stu-id="cbd42-141">**External.changeViewOnlineList**</span></span>](external-changeviewonlinelist.md)
</dt> <dt>

[<span data-ttu-id="cbd42-142">**External. OnViewChange**</span><span class="sxs-lookup"><span data-stu-id="cbd42-142">**External.OnViewChange**</span></span>](external-onviewchange-event.md)
</dt> </dl>

 

 





