---
title: External. OnViewChange, événement
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. L’événement OnViewChange se produit lorsque la vue change dans le lecteur Windows Media.
ms.assetid: aa1378ad-8b84-4592-85c5-5e284be05ea6
keywords:
- Événement External. OnViewChange lecteur Windows Media
topic_type:
- apiref
api_name:
- External.OnViewChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c7144e03955fb67ed90cad4a4336bf782ca1566
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536455"
---
# <a name="externalonviewchange-event"></a><span data-ttu-id="bba8c-106">External. OnViewChange, événement</span><span class="sxs-lookup"><span data-stu-id="bba8c-106">External.OnViewChange Event</span></span>

> [!Note]  
> <span data-ttu-id="bba8c-107">Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="bba8c-107">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="bba8c-108">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="bba8c-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="bba8c-109">L’événement **OnViewChange** se produit lorsque la vue change dans le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="bba8c-109">The **OnViewChange** event occurs when the view changes in Windows Media Player.</span></span>

``` syntax
window.external.OnViewChange = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="bba8c-110">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="bba8c-110">Possible Values</span></span>

<span data-ttu-id="bba8c-111">Il s’agit d’une propriété en écriture seule qui spécifie le nom de la fonction dans le script que le lecteur Windows Media appelle lorsque l’événement se produit.</span><span class="sxs-lookup"><span data-stu-id="bba8c-111">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="bba8c-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bba8c-112">Parameters</span></span>

<span data-ttu-id="bba8c-113">La fonction qui gère cet événement n’accepte aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="bba8c-113">The function that handles this event takes no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="bba8c-114">Notes</span><span class="sxs-lookup"><span data-stu-id="bba8c-114">Remarks</span></span>

<span data-ttu-id="bba8c-115">La vue dans le lecteur Windows Media peut changer pour l’une des raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="bba8c-115">The view in Windows Media Player can change for any of the following reasons:</span></span>

-   <span data-ttu-id="bba8c-116">L’utilisateur interagit avec l’interface utilisateur du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="bba8c-116">The user interacts with the Windows Media Player user interface.</span></span>
-   <span data-ttu-id="bba8c-117">L’utilisateur interagit avec une page de découverte et le script sur la page de découverte appelle [External. changeView](external-changeview.md).</span><span class="sxs-lookup"><span data-stu-id="bba8c-117">The user interacts with a discovery page, and script on the discovery page calls [External.changeView](external-changeview.md).</span></span>
-   <span data-ttu-id="bba8c-118">L’utilisateur interagit avec une page de découverte et le script sur la page de découverte appelle [External. changeViewOnlineList](external-changeviewonlinelist.md).</span><span class="sxs-lookup"><span data-stu-id="bba8c-118">The user interacts with a discovery page, and script on the discovery page calls [External.changeViewOnlineList](external-changeviewonlinelist.md).</span></span>

<span data-ttu-id="bba8c-119">Lorsque la vue change dans le lecteur Windows Media, le lecteur appelle [IWMPContentPartner :: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) pour obtenir l’URL de la page de découverte suivante à afficher.</span><span class="sxs-lookup"><span data-stu-id="bba8c-119">When the view changes in Windows Media Player, the Player calls [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) to get the URL of the next discovery page to display.</span></span> <span data-ttu-id="bba8c-120">Toutefois, avant que le lecteur n’affiche la page nouvelle détection, il déclenche l’événement **OnViewChange** .</span><span class="sxs-lookup"><span data-stu-id="bba8c-120">However, before the Player displays the new discovery page, it raises the **OnViewChange** event.</span></span> <span data-ttu-id="bba8c-121">Si le gestionnaire d’événements **OnViewChange** appelle [External. CancelNavigate](external-cancelnavigate.md), le lecteur Windows Media n’affiche pas la page nouvelle détection.</span><span class="sxs-lookup"><span data-stu-id="bba8c-121">If the **OnViewChange** event handler calls [External.cancelNavigate](external-cancelnavigate.md), Windows Media Player does not display the new discovery page.</span></span> <span data-ttu-id="bba8c-122">Au lieu de cela, il continue d’afficher la page de découverte actuelle.</span><span class="sxs-lookup"><span data-stu-id="bba8c-122">Instead, it continues to display the current discovery page.</span></span>

## <a name="requirements"></a><span data-ttu-id="bba8c-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bba8c-123">Requirements</span></span>



| <span data-ttu-id="bba8c-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bba8c-124">Requirement</span></span> | <span data-ttu-id="bba8c-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="bba8c-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bba8c-126">Version</span><span class="sxs-lookup"><span data-stu-id="bba8c-126">Version</span></span><br/> | <span data-ttu-id="bba8c-127">Lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="bba8c-127">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="bba8c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="bba8c-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="bba8c-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bba8c-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bba8c-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bba8c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bba8c-131">**Objet externe pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="bba8c-131">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="bba8c-132">**External. changeView**</span><span class="sxs-lookup"><span data-stu-id="bba8c-132">**External.changeView**</span></span>](external-changeview.md)
</dt> <dt>

[<span data-ttu-id="bba8c-133">**External. changeViewOnlineList**</span><span class="sxs-lookup"><span data-stu-id="bba8c-133">**External.changeViewOnlineList**</span></span>](external-changeviewonlinelist.md)
</dt> </dl>

 

 





