---
description: Affiche ou masque la liste de saisie semi-automatique.
ms.assetid: 756ffa3d-03ee-4753-a826-3bc22ab16f5f
title: 'ITipAutocompleteProvider :: Show, méthode (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider.Show
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 950358ae28d1cb68af803ed6b7f520f1bbad8c03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759814"
---
# <a name="itipautocompleteprovidershow-method"></a><span data-ttu-id="ec9bf-103">ITipAutocompleteProvider :: Show, méthode</span><span class="sxs-lookup"><span data-stu-id="ec9bf-103">ITipAutocompleteProvider::Show method</span></span>

<span data-ttu-id="ec9bf-104">Affiche ou masque la liste de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="ec9bf-104">Displays or hides the auto complete list.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec9bf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec9bf-105">Syntax</span></span>


```C++
HRESULT Show(
  [in] BOOL fShow
);
```



## <a name="parameters"></a><span data-ttu-id="ec9bf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec9bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec9bf-107">*fShow* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ec9bf-107">*fShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec9bf-108">**True** pour afficher l’interface utilisateur de saisie semi-automatique, **false** pour masquer l’interface utilisateur de la liste de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="ec9bf-108">**TRUE** to show the auto complete user interface, **FALSE** to hide the auto complete list user interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec9bf-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ec9bf-109">Return value</span></span>

<span data-ttu-id="ec9bf-110">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="ec9bf-110">This method can return one of these values.</span></span>



| <span data-ttu-id="ec9bf-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ec9bf-111">Return code</span></span>                                                                            | <span data-ttu-id="ec9bf-112">Description</span><span class="sxs-lookup"><span data-stu-id="ec9bf-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="ec9bf-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ec9bf-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="ec9bf-114">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="ec9bf-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="ec9bf-115"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="ec9bf-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="ec9bf-116">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="ec9bf-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ec9bf-117">Notes</span><span class="sxs-lookup"><span data-stu-id="ec9bf-117">Remarks</span></span>

<span data-ttu-id="ec9bf-118">Cette méthode est appelée par le client pour afficher ou masquer la liste de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="ec9bf-118">This method is called by the client to show or hide the auto complete list.</span></span> <span data-ttu-id="ec9bf-119">Si la liste de saisie semi-automatique n’est pas affichée et que *fShow* a la **valeur false**, cette méthode n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="ec9bf-119">If the auto complete list is not displayed and *fShow* is **FALSE**, this method does nothing.</span></span> <span data-ttu-id="ec9bf-120">Si la liste de saisie semi-automatique est affichée et que *fShow* a la **valeur true**, cette méthode n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="ec9bf-120">If the auto complete list is displayed and *fShow* is **TRUE**, this method does nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec9bf-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec9bf-121">Requirements</span></span>



| <span data-ttu-id="ec9bf-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec9bf-122">Requirement</span></span> | <span data-ttu-id="ec9bf-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec9bf-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec9bf-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec9bf-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ec9bf-125">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ec9bf-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="ec9bf-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec9bf-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ec9bf-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec9bf-127">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="ec9bf-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="ec9bf-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec9bf-129"><dt>TipAutoComplete. h (nécessite également PenInputPanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ec9bf-129"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ec9bf-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ec9bf-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec9bf-131"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec9bf-131"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="ec9bf-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec9bf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec9bf-133">**Interface ITipAutocompleteProvider**</span><span class="sxs-lookup"><span data-stu-id="ec9bf-133">**ITipAutocompleteProvider Interface**</span></span>](itipautocompleteprovider.md)
</dt> <dt>

[<span data-ttu-id="ec9bf-134">Référence du panneau de saisie de texte</span><span class="sxs-lookup"><span data-stu-id="ec9bf-134">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




