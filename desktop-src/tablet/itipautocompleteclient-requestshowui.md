---
description: Détermine si le panneau de saisie est prêt à afficher la liste de saisie semi-automatique.
ms.assetid: 1e0d4bc6-e6a3-4123-a381-00a41ed9c848
title: 'ITipAutocompleteClient :: RequestShowUI, méthode (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.RequestShowUI
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: e547376bf2e9c50c224d1917e00329e8d9555e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203245"
---
# <a name="itipautocompleteclientrequestshowui-method"></a><span data-ttu-id="8d35d-103">ITipAutocompleteClient :: RequestShowUI, méthode</span><span class="sxs-lookup"><span data-stu-id="8d35d-103">ITipAutocompleteClient::RequestShowUI method</span></span>

<span data-ttu-id="8d35d-104">Détermine si le panneau de saisie est prêt à afficher la liste de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="8d35d-104">Determines whether Input Panel is ready to have the auto complete list shown.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d35d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d35d-105">Syntax</span></span>


```C++
HRESULT RequestShowUI(
  [in]  HWND hWndACList,
  [out] BOOL *pfAllowShowing
);
```



## <a name="parameters"></a><span data-ttu-id="8d35d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d35d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d35d-107">*hWndACList* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d35d-107">*hWndACList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d35d-108">Handle de fenêtre de l’interface utilisateur de la liste de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="8d35d-108">Window handle of the auto complete list user interface.</span></span>

</dd> <dt>

<span data-ttu-id="8d35d-109">*pfAllowShowing* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8d35d-109">*pfAllowShowing* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d35d-110">**False** si le client recommande de ne pas afficher l’interface utilisateur de la liste de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="8d35d-110">**FALSE** if client recommends to not show the auto complete list user interface.</span></span> <span data-ttu-id="8d35d-111">**True** si le fournisseur de saisie semi-automatique peut afficher l’interface utilisateur de la liste.</span><span class="sxs-lookup"><span data-stu-id="8d35d-111">**TRUE** if the auto complete provider can show the list user interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d35d-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8d35d-112">Return value</span></span>

<span data-ttu-id="8d35d-113">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="8d35d-113">This method can return one of these values.</span></span>



| <span data-ttu-id="8d35d-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8d35d-114">Return code</span></span>                                                                            | <span data-ttu-id="8d35d-115">Description</span><span class="sxs-lookup"><span data-stu-id="8d35d-115">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="8d35d-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8d35d-116"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="8d35d-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="8d35d-117">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="8d35d-118"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="8d35d-118"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="8d35d-119">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="8d35d-119">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8d35d-120">Notes</span><span class="sxs-lookup"><span data-stu-id="8d35d-120">Remarks</span></span>

<span data-ttu-id="8d35d-121">Cette méthode est appelée par le fournisseur de saisie semi-automatique lorsqu’il est sur le présent d’afficher l’interface utilisateur de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="8d35d-121">This method is called by the auto complete provider when it is about to show the auto complete user interface.</span></span> <span data-ttu-id="8d35d-122">Si l’état interne du client n’autorise pas le fournisseur à afficher l’interface utilisateur, *pfAllowShowing* est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="8d35d-122">If the client's internal state doesn't allow the provider to show the user interface, *pfAllowShowing* will be set to **FALSE**.</span></span> <span data-ttu-id="8d35d-123">Par exemple, lorsque le texte est envoyé au champ à partir de l’apparence de l’écriture manuscrite dans le panneau de saisie Tablet PC et que l’utilisateur commence immédiatement l’entrée manuscrite, le client recommande de ne pas afficher l’interface utilisateur de saisie semi-automatique, afin d’éviter la destruction de l’entrée de l’utilisateur, en affectant à *pfAllowShowing* la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="8d35d-123">For example, when the text gets sent to the field from the handwriting skin on the Tablet PC Input Panel and the user immediately starts inking, the client will recommend to not show the auto complete user interface, in order to avoid destructing the user's inking, by setting *pfAllowShowing* to **FALSE**.</span></span>

<span data-ttu-id="8d35d-124">Appelez **RequestShowUI** pour définir le handle de fenêtre de la liste de saisie semi-automatique contextuelle avant d’appeler la [**méthode ITipAutocompleteClient ::P referredrects**](itipautocompleteclient-preferredrects.md).</span><span class="sxs-lookup"><span data-stu-id="8d35d-124">Call **RequestShowUI** to set the popup auto complete list window handle before you call the [**ITipAutocompleteClient::PreferredRects Method**](itipautocompleteclient-preferredrects.md).</span></span> <span data-ttu-id="8d35d-125">Dans le cas contraire, une erreur d' **E \_ INVALIDARG** se produira lors de l’appel de **PreferredRects**.</span><span class="sxs-lookup"><span data-stu-id="8d35d-125">Failure to do so will cause an **E\_INVALIDARG** error when calling **PreferredRects**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d35d-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d35d-126">Requirements</span></span>



| <span data-ttu-id="8d35d-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d35d-127">Requirement</span></span> | <span data-ttu-id="8d35d-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d35d-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d35d-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d35d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8d35d-130">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8d35d-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="8d35d-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d35d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8d35d-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d35d-132">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="8d35d-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="8d35d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d35d-134"><dt>TipAutoComplete. h (nécessite également PenInputPanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8d35d-134"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8d35d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8d35d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d35d-136"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d35d-136"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="8d35d-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d35d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d35d-138">**Interface ITipAutocompleteClient**</span><span class="sxs-lookup"><span data-stu-id="8d35d-138">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="8d35d-139">**ITipAutocompleteClient ::P méthode referredRects**</span><span class="sxs-lookup"><span data-stu-id="8d35d-139">**ITipAutocompleteClient::PreferredRects Method**</span></span>](itipautocompleteclient-preferredrects.md)
</dt> <dt>

[<span data-ttu-id="8d35d-140">Référence du panneau de saisie de texte</span><span class="sxs-lookup"><span data-stu-id="8d35d-140">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




