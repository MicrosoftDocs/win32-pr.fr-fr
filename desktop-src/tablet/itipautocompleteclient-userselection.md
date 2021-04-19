---
description: Notifie le panneau de saisie que l’utilisateur a sélectionné un nom dans la liste de saisie semi-automatique et qu’il ignore tout le texte restant qui n’a pas encore été inséré.
ms.assetid: 2e6fabe1-7984-4908-bf90-0603d0dad268
title: 'ITipAutocompleteClient :: UserSelection, méthode (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.UserSelection
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 1894db9da3b8e3a36e59eb45150b27facfe0291f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521002"
---
# <a name="itipautocompleteclientuserselection-method"></a><span data-ttu-id="18d8d-103">ITipAutocompleteClient :: UserSelection, méthode</span><span class="sxs-lookup"><span data-stu-id="18d8d-103">ITipAutocompleteClient::UserSelection method</span></span>

<span data-ttu-id="18d8d-104">Notifie le panneau de saisie que l’utilisateur a sélectionné un nom dans la liste de saisie semi-automatique et qu’il ignore tout le texte restant qui n’a pas encore été inséré.</span><span class="sxs-lookup"><span data-stu-id="18d8d-104">Notifies the Input Panel that the user has selected something in the auto complete list and to discard all remaining text that has not yet been inserted.</span></span>

## <a name="syntax"></a><span data-ttu-id="18d8d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18d8d-105">Syntax</span></span>


```C++
HRESULT UserSelection();
```



## <a name="parameters"></a><span data-ttu-id="18d8d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="18d8d-106">Parameters</span></span>

<span data-ttu-id="18d8d-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="18d8d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="18d8d-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="18d8d-108">Return value</span></span>

<span data-ttu-id="18d8d-109">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="18d8d-109">This method can return one of these values.</span></span>



| <span data-ttu-id="18d8d-110">Code de retour</span><span class="sxs-lookup"><span data-stu-id="18d8d-110">Return code</span></span>                                                                            | <span data-ttu-id="18d8d-111">Description</span><span class="sxs-lookup"><span data-stu-id="18d8d-111">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="18d8d-112"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="18d8d-112"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="18d8d-113">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="18d8d-113">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="18d8d-114"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="18d8d-114"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="18d8d-115">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="18d8d-115">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="18d8d-116">Notes</span><span class="sxs-lookup"><span data-stu-id="18d8d-116">Remarks</span></span>

<span data-ttu-id="18d8d-117">Cette méthode est appelée à partir du fournisseur pour notifier au client qu’une sélection a été effectuée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="18d8d-117">This method is called from the provider to notify the client that a selection has been made by the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="18d8d-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18d8d-118">Requirements</span></span>



| <span data-ttu-id="18d8d-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18d8d-119">Requirement</span></span> | <span data-ttu-id="18d8d-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="18d8d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18d8d-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18d8d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="18d8d-122">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18d8d-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="18d8d-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18d8d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="18d8d-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="18d8d-124">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="18d8d-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="18d8d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="18d8d-126"><dt>TipAutoComplete. h (nécessite également PenInputPanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="18d8d-126"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="18d8d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="18d8d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18d8d-128"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18d8d-128"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="18d8d-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18d8d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18d8d-130">**Interface ITipAutocompleteClient**</span><span class="sxs-lookup"><span data-stu-id="18d8d-130">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="18d8d-131">Référence du panneau de saisie de texte</span><span class="sxs-lookup"><span data-stu-id="18d8d-131">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




