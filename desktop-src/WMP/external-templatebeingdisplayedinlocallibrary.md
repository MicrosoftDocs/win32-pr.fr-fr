---
title: External. templateBeingDisplayedInLocalLibrary
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. templateBeingDisplayedInLocalLibrary
ms.assetid: a1399c20-804b-4413-be9d-bcf160d75d29
keywords:
- External. templateBeingDisplayedInLocalLibrary Windows Media Player
topic_type:
- apiref
api_name:
- External.templateBeingDisplayedInLocalLibrary
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f1d9a93d870882a34014ea2d0d35f29b91f54d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539679"
---
# <a name="externaltemplatebeingdisplayedinlocallibrary"></a><span data-ttu-id="7f138-105">External. templateBeingDisplayedInLocalLibrary</span><span class="sxs-lookup"><span data-stu-id="7f138-105">External.templateBeingDisplayedInLocalLibrary</span></span>

> [!Note]  
> <span data-ttu-id="7f138-106">Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="7f138-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="7f138-107">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="7f138-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="7f138-108">La propriété **templateBeingDisplayedInLocalLibrary** indique si le flux représenté par la page de découverte active s’affiche dans le contrôle d’arborescence de la bibliothèque locale.</span><span class="sxs-lookup"><span data-stu-id="7f138-108">The **templateBeingDisplayedInLocalLibrary** property indicates whether the feed represented by the current discovery page is being displayed in the local library tree-view control.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f138-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f138-109">Syntax</span></span>

``` syntax
window.external.templateBeingDisplayedInLocalLibrary
```

## <a name="possible-values"></a><span data-ttu-id="7f138-110">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="7f138-110">Possible Values</span></span>

<span data-ttu-id="7f138-111">Cette propriété est une **valeur booléenne** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7f138-111">This property is a read-only **Boolean**.</span></span> <span data-ttu-id="7f138-112">**True** indique que le flux est affiché dans le contrôle Tree-View de la bibliothèque locale.</span><span class="sxs-lookup"><span data-stu-id="7f138-112">**TRUE** indicates that the feed is being displayed in the local library tree-view control.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f138-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7f138-113">Remarks</span></span>

<span data-ttu-id="7f138-114">Une page de découverte qui représente un flux pour une sélection dynamique peut afficher un bouton qui permet à l’utilisateur d’enregistrer le flux dans sa bibliothèque locale.</span><span class="sxs-lookup"><span data-stu-id="7f138-114">A discovery page that represents a feed for a dynamic playlist can display a button that allows the user to "save" the feed in his or her local library.</span></span> <span data-ttu-id="7f138-115">L’enregistrement du flux, dans ce contexte, signifie que certaines métadonnées sont enregistrées sur l’ordinateur de l’utilisateur et que le flux est listé sous le nœud **sélections** dans le contrôle arborescence de la bibliothèque locale.</span><span class="sxs-lookup"><span data-stu-id="7f138-115">Saving the feed, in this context, means that some metadata is saved on the user's computer, and the feed is listed under the **Playlists** node in the local library tree-view control.</span></span> <span data-ttu-id="7f138-116">Script sur la page détection peut inspecter la propriété **templateBeingDisplayedInLocalLibrary** pour déterminer si l’utilisateur a déjà enregistré le flux dans la bibliothèque locale.</span><span class="sxs-lookup"><span data-stu-id="7f138-116">Script on the discovery page can inspect the **templateBeingDisplayedInLocalLibrary** property to determine whether the user has already saved the feed in the local library.</span></span> <span data-ttu-id="7f138-117">Si l’utilisateur a déjà enregistré le flux, la page détection ne doit pas afficher le bouton enregistrer.</span><span class="sxs-lookup"><span data-stu-id="7f138-117">If the user has already saved the feed, the discovery page should not display the save button.</span></span>

<span data-ttu-id="7f138-118">Une page de découverte qui représente un flux radio doit inspecter la propriété **templateBeingDisplayedInLocalLibrary** pour la même raison.</span><span class="sxs-lookup"><span data-stu-id="7f138-118">A discovery page that represents a radio feed should inspect the **templateBeingDisplayedInLocalLibrary** property for the same reason.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f138-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f138-119">Requirements</span></span>



| <span data-ttu-id="7f138-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f138-120">Requirement</span></span> | <span data-ttu-id="7f138-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f138-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7f138-122">Version</span><span class="sxs-lookup"><span data-stu-id="7f138-122">Version</span></span><br/> | <span data-ttu-id="7f138-123">Lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="7f138-123">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="7f138-124">DLL</span><span class="sxs-lookup"><span data-stu-id="7f138-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="7f138-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f138-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f138-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f138-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f138-127">**Objet externe pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="7f138-127">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





