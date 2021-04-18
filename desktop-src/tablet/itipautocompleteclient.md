---
description: Permet au client d’appeler l’objet fournisseur de saisie semi-automatique du panneau de saisie du texte de l’application.
ms.assetid: 448b8136-ebcb-4116-9a81-a77a37d69e24
title: Interface ITipAutocompleteClient (TipAutoComplete. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 7b9dad38d0e3f169019934b7e60a09096aced1b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522738"
---
# <a name="itipautocompleteclient-interface"></a><span data-ttu-id="99a5c-103">Interface ITipAutocompleteClient</span><span class="sxs-lookup"><span data-stu-id="99a5c-103">ITipAutocompleteClient interface</span></span>

<span data-ttu-id="99a5c-104">Permet au client d’appeler l’objet fournisseur de saisie semi-automatique du panneau de saisie du texte de l’application.</span><span class="sxs-lookup"><span data-stu-id="99a5c-104">Enables the client to call the application's Text Input Panel auto complete provider object.</span></span>

## <a name="members"></a><span data-ttu-id="99a5c-105">Membres</span><span class="sxs-lookup"><span data-stu-id="99a5c-105">Members</span></span>

<span data-ttu-id="99a5c-106">L’interface **ITipAutocompleteClient** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="99a5c-106">The **ITipAutocompleteClient** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="99a5c-107">**ITipAutocompleteClient** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="99a5c-107">**ITipAutocompleteClient** also has these types of members:</span></span>

-   [<span data-ttu-id="99a5c-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="99a5c-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="99a5c-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="99a5c-109">Methods</span></span>

<span data-ttu-id="99a5c-110">L’interface **ITipAutocompleteClient** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="99a5c-110">The **ITipAutocompleteClient** interface has these methods.</span></span>



| <span data-ttu-id="99a5c-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="99a5c-111">Method</span></span>                                                              | <span data-ttu-id="99a5c-112">Description</span><span class="sxs-lookup"><span data-stu-id="99a5c-112">Description</span></span>                                                                                                                                                          |
|:--------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="99a5c-113">**AdviseProvider**</span><span class="sxs-lookup"><span data-stu-id="99a5c-113">**AdviseProvider**</span></span>](itipautocompleteclient-adviseprovider.md)     | <span data-ttu-id="99a5c-114">Inscrit le fournisseur auprès du client pour permettre au client d’appeler l’objet fournisseur de saisie semi-automatique de l’application.</span><span class="sxs-lookup"><span data-stu-id="99a5c-114">Registers the provider with the client to enable the client to call the application's auto complete provider object.</span></span><br/>                                      |
| [<span data-ttu-id="99a5c-115">**PreferredRects**</span><span class="sxs-lookup"><span data-stu-id="99a5c-115">**PreferredRects**</span></span>](itipautocompleteclient-preferredrects.md)     | <span data-ttu-id="99a5c-116">Permet au client de suggérer où placer la liste de saisie semi-automatique pour éviter le chevauchement du panneau de saisie.</span><span class="sxs-lookup"><span data-stu-id="99a5c-116">Allows the client to suggest where to position the auto complete list to avoid overlapping the Input Panel.</span></span><br/>                                               |
| [<span data-ttu-id="99a5c-117">**RequestShowUI**</span><span class="sxs-lookup"><span data-stu-id="99a5c-117">**RequestShowUI**</span></span>](itipautocompleteclient-requestshowui.md)       | <span data-ttu-id="99a5c-118">Détermine si le panneau de saisie est prêt à afficher la liste de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="99a5c-118">Determines whether Input Panel is ready to have the auto complete list shown.</span></span><br/>                                                                             |
| [<span data-ttu-id="99a5c-119">**UnadviseProvider**</span><span class="sxs-lookup"><span data-stu-id="99a5c-119">**UnadviseProvider**</span></span>](itipautocompleteclient-unadviseprovider.md) | <span data-ttu-id="99a5c-120">Annule l’inscription du fournisseur associé.</span><span class="sxs-lookup"><span data-stu-id="99a5c-120">Unregisters the associated provider.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="99a5c-121">**UserSelection**</span><span class="sxs-lookup"><span data-stu-id="99a5c-121">**UserSelection**</span></span>](itipautocompleteclient-userselection.md)       | <span data-ttu-id="99a5c-122">Notifie le panneau de saisie que l’utilisateur a sélectionné un nom dans la liste de saisie semi-automatique et qu’il ignore tout le texte restant qui n’a pas encore été inséré.</span><span class="sxs-lookup"><span data-stu-id="99a5c-122">Notifies the Input Panel that the user has selected something in the auto complete list and to discard all remaining text that has not yet been inserted.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="99a5c-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99a5c-123">Requirements</span></span>



| <span data-ttu-id="99a5c-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99a5c-124">Requirement</span></span> | <span data-ttu-id="99a5c-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="99a5c-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99a5c-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99a5c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="99a5c-127">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="99a5c-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="99a5c-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99a5c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="99a5c-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="99a5c-129">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="99a5c-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="99a5c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="99a5c-131"><dt>TipAutoComplete. h (nécessite également PenInputPanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="99a5c-131"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="99a5c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="99a5c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99a5c-133"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99a5c-133"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



 

