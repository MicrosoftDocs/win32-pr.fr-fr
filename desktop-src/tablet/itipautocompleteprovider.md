---
description: Gère le côté de l’application de l’intégration de la saisie semi-automatique du panneau de saisie de texte.
ms.assetid: 02601258-d867-4c01-b094-bf9ff96d2f6e
title: Interface ITipAutocompleteProvider (TipAutoComplete. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 3c300e2724ccabbc8388ef647f8f0145531cfc8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538194"
---
# <a name="itipautocompleteprovider-interface"></a><span data-ttu-id="7f81d-103">Interface ITipAutocompleteProvider</span><span class="sxs-lookup"><span data-stu-id="7f81d-103">ITipAutocompleteProvider interface</span></span>

<span data-ttu-id="7f81d-104">Gère le côté de l’application de l’intégration de la saisie semi-automatique du panneau de saisie de texte.</span><span class="sxs-lookup"><span data-stu-id="7f81d-104">Manages the application's side of the Text Input Panel auto complete integration.</span></span>

## <a name="members"></a><span data-ttu-id="7f81d-105">Membres</span><span class="sxs-lookup"><span data-stu-id="7f81d-105">Members</span></span>

<span data-ttu-id="7f81d-106">L’interface **ITipAutocompleteProvider** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7f81d-106">The **ITipAutocompleteProvider** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7f81d-107">**ITipAutocompleteProvider** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7f81d-107">**ITipAutocompleteProvider** also has these types of members:</span></span>

-   [<span data-ttu-id="7f81d-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7f81d-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7f81d-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7f81d-109">Methods</span></span>

<span data-ttu-id="7f81d-110">L’interface **ITipAutocompleteProvider** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="7f81d-110">The **ITipAutocompleteProvider** interface has these methods.</span></span>



| <span data-ttu-id="7f81d-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="7f81d-111">Method</span></span>                                                                  | <span data-ttu-id="7f81d-112">Description</span><span class="sxs-lookup"><span data-stu-id="7f81d-112">Description</span></span>                                                                                                          |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f81d-113">**Afficher**</span><span class="sxs-lookup"><span data-stu-id="7f81d-113">**Show**</span></span>](itipautocompleteprovider-show.md)                           | <span data-ttu-id="7f81d-114">Affiche ou masque la liste de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="7f81d-114">Displays or hides the auto complete list.</span></span><br/>                                                                 |
| [<span data-ttu-id="7f81d-115">**UpdatePendingText**</span><span class="sxs-lookup"><span data-stu-id="7f81d-115">**UpdatePendingText**</span></span>](itipautocompleteprovider-updatependingtext.md) | <span data-ttu-id="7f81d-116">Utilisé par le client de saisie semi-automatique pour notifier l’application du texte qu’un utilisateur a inséré dans le panneau de saisie.</span><span class="sxs-lookup"><span data-stu-id="7f81d-116">Used by the auto complete client to notify the application of the text a user has inked into Input Panel.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7f81d-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f81d-117">Requirements</span></span>



| <span data-ttu-id="7f81d-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f81d-118">Requirement</span></span> | <span data-ttu-id="7f81d-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f81d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f81d-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f81d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7f81d-121">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7f81d-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="7f81d-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f81d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7f81d-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f81d-123">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="7f81d-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="7f81d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f81d-125"><dt>TipAutoComplete. h (nécessite également PenInputPanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7f81d-125"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7f81d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7f81d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f81d-127"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f81d-127"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="7f81d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f81d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f81d-129">Référence du panneau de saisie de texte</span><span class="sxs-lookup"><span data-stu-id="7f81d-129">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> <dt>

[<span data-ttu-id="7f81d-130">**Interface ITipAutocompleteClient**</span><span class="sxs-lookup"><span data-stu-id="7f81d-130">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> </dl>

 

