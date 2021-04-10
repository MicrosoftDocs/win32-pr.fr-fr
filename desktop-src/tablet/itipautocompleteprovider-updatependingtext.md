---
description: Utilisé par le client de saisie semi-automatique pour notifier l’application du texte qu’un utilisateur a inséré dans le panneau de saisie.
ms.assetid: 68413836-321a-4e75-8538-c5a8fc577c0f
title: 'ITipAutocompleteProvider :: UpdatePendingText, méthode (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider.UpdatePendingText
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 5c66e625639aa7088b1b3934a2f984d0f4097536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042828"
---
# <a name="itipautocompleteproviderupdatependingtext-method"></a><span data-ttu-id="283b5-103">ITipAutocompleteProvider :: UpdatePendingText, méthode</span><span class="sxs-lookup"><span data-stu-id="283b5-103">ITipAutocompleteProvider::UpdatePendingText method</span></span>

<span data-ttu-id="283b5-104">Utilisé par le client de saisie semi-automatique pour notifier l’application du texte qu’un utilisateur a inséré dans le panneau de saisie.</span><span class="sxs-lookup"><span data-stu-id="283b5-104">Used by the auto complete client to notify the application of the text a user has inked into Input Panel.</span></span>

## <a name="syntax"></a><span data-ttu-id="283b5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="283b5-105">Syntax</span></span>


```C++
HRESULT UpdatePendingText(
  [in] BSTR bstrPendingText
);
```



## <a name="parameters"></a><span data-ttu-id="283b5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="283b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="283b5-107">*bstrPendingText* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="283b5-107">*bstrPendingText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="283b5-108">Texte source à utiliser pour générer la liste de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="283b5-108">Source text to be used to generate the auto complete list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="283b5-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="283b5-109">Return value</span></span>

<span data-ttu-id="283b5-110">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="283b5-110">This method can return one of these values.</span></span>



| <span data-ttu-id="283b5-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="283b5-111">Return code</span></span>                                                                            | <span data-ttu-id="283b5-112">Description</span><span class="sxs-lookup"><span data-stu-id="283b5-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="283b5-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="283b5-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="283b5-114">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="283b5-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="283b5-115"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="283b5-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="283b5-116">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="283b5-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="283b5-117">Notes</span><span class="sxs-lookup"><span data-stu-id="283b5-117">Remarks</span></span>

<span data-ttu-id="283b5-118">Ce texte ne contient pas le texte déjà inséré dans le champ ayant le focus.</span><span class="sxs-lookup"><span data-stu-id="283b5-118">This text will not contain the text already inserted in the focused field.</span></span> <span data-ttu-id="283b5-119">Le fournisseur de saisie semi-automatique est chargé de tenir compte du texte du champ actuel et de la sélection pour générer la liste de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="283b5-119">The auto complete provider is responsible for taking into account the current field text and the selection to generate the auto complete list.</span></span> <span data-ttu-id="283b5-120">Quand *bstrPendingText* a la **valeur null**, la liste de saisie semi-automatique est générée avec le texte actuel à gauche de la sélection dans le champ.</span><span class="sxs-lookup"><span data-stu-id="283b5-120">When *bstrPendingText* is **NULL**, the auto complete list is generated with the current text to the left of the selection in the field.</span></span>

## <a name="requirements"></a><span data-ttu-id="283b5-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="283b5-121">Requirements</span></span>



| <span data-ttu-id="283b5-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="283b5-122">Requirement</span></span> | <span data-ttu-id="283b5-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="283b5-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="283b5-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="283b5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="283b5-125">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="283b5-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="283b5-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="283b5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="283b5-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="283b5-127">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="283b5-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="283b5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="283b5-129"><dt>TipAutoComplete. h (nécessite également PenInputPanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="283b5-129"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="283b5-130">DLL</span><span class="sxs-lookup"><span data-stu-id="283b5-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="283b5-131"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="283b5-131"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="283b5-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="283b5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="283b5-133">**Interface ITipAutocompleteProvider**</span><span class="sxs-lookup"><span data-stu-id="283b5-133">**ITipAutocompleteProvider Interface**</span></span>](itipautocompleteprovider.md)
</dt> <dt>

[<span data-ttu-id="283b5-134">Référence du panneau de saisie de texte</span><span class="sxs-lookup"><span data-stu-id="283b5-134">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




