---
description: Permet au client de suggérer où placer la liste de saisie semi-automatique pour éviter le chevauchement du panneau de saisie.
ms.assetid: c82ffecb-f3e6-4c50-80bb-8393b39d3b2a
title: ITipAutocompleteClient ::P méthode referredRects (TipAutoComplete. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.PreferredRects
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 04e935c668e858ae3d22936e8a63f9116ebd6ab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534015"
---
# <a name="itipautocompleteclientpreferredrects-method"></a><span data-ttu-id="dcc0d-103">ITipAutocompleteClient ::P méthode referredRects</span><span class="sxs-lookup"><span data-stu-id="dcc0d-103">ITipAutocompleteClient::PreferredRects method</span></span>

<span data-ttu-id="dcc0d-104">Permet au client de suggérer où placer la liste de saisie semi-automatique pour éviter le chevauchement du panneau de saisie.</span><span class="sxs-lookup"><span data-stu-id="dcc0d-104">Allows the client to suggest where to position the auto complete list to avoid overlapping the Input Panel.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcc0d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dcc0d-105">Syntax</span></span>


```C++
HRESULT PreferredRects(
  [in]      RECT *prcACList,
  [in]      RECT *prcField,
  [out]     RECT *prcModified,
  [in, out] BOOL *pfShownAboveTip
);
```



## <a name="parameters"></a><span data-ttu-id="dcc0d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dcc0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcc0d-107">*prcACList* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dcc0d-107">*prcACList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcc0d-108">Rectangle, en coordonnées d’écran, indiquant l’emplacement préféré du fournisseur et la taille de l’interface utilisateur de la liste de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="dcc0d-108">A rectangle, in screen coordinates, indicating the provider's preferred location and the size of the auto complete list user interface.</span></span>

</dd> <dt>

<span data-ttu-id="dcc0d-109">*prcField* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dcc0d-109">*prcField* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcc0d-110">Rectangle, en coordonnées d’écran, indiquant l’emplacement et la taille du champ ayant le focus.</span><span class="sxs-lookup"><span data-stu-id="dcc0d-110">A rectangle, in screen coordinates, indicating the location and the size of the focused field.</span></span>

</dd> <dt>

<span data-ttu-id="dcc0d-111">*prcModified* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dcc0d-111">*prcModified* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcc0d-112">Un rectangle basé sur l’état actuel de l’info-bulle et l’emplacement et la taille de la liste de saisie semi-automatique par défaut spécifiés par *prcACList*.</span><span class="sxs-lookup"><span data-stu-id="dcc0d-112">A rectangle based on the current state of the TIP and the preferred auto complete list location and size specified by *prcACList*.</span></span>

</dd> <dt>

<span data-ttu-id="dcc0d-113">*pfShownAboveTip* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="dcc0d-113">*pfShownAboveTip* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcc0d-114">**True** si le rectangle modifié doit être affiché au-dessus de la zone cible du panneau de saisie du texte ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="dcc0d-114">**TRUE** if the modified rectangle is to be shown above the Text Input Panel's target area; otherwise, **FALSE**.</span></span> <span data-ttu-id="dcc0d-115">Cette valeur doit être initialisée à l’orientation par défaut du fournisseur avant que la méthode ne soit appelée.</span><span class="sxs-lookup"><span data-stu-id="dcc0d-115">This value must be initialized to the provider's preferred orientation before the method is called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcc0d-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dcc0d-116">Return value</span></span>

<span data-ttu-id="dcc0d-117">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="dcc0d-117">This method can return one of these values.</span></span>



| <span data-ttu-id="dcc0d-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="dcc0d-118">Return code</span></span>                                                                                  | <span data-ttu-id="dcc0d-119">Description</span><span class="sxs-lookup"><span data-stu-id="dcc0d-119">Description</span></span>                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dcc0d-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dcc0d-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="dcc0d-121">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="dcc0d-121">Success.</span></span><br/>                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="dcc0d-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="dcc0d-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="dcc0d-123">Appelez la [**méthode ITipAutocompleteClient :: RequestShowUI**](itipautocompleteclient-requestshowui.md) pour définir la fenêtre Liste de saisie semi-automatique des fenêtres contextuelles avant d’appeler la [**méthode ITipAutocompleteClient ::P referredrects**](itipautocompleteclient-preferredrects.md).</span><span class="sxs-lookup"><span data-stu-id="dcc0d-123">Call the [**ITipAutocompleteClient::RequestShowUI Method**](itipautocompleteclient-requestshowui.md) to set the popup auto complete list window before calling the [**ITipAutocompleteClient::PreferredRects Method**](itipautocompleteclient-preferredrects.md).</span></span><br/> |
| <dl> <span data-ttu-id="dcc0d-124"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="dcc0d-124"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="dcc0d-125">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="dcc0d-125">An unspecified error occurred.</span></span><br/>                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="dcc0d-126">Notes</span><span class="sxs-lookup"><span data-stu-id="dcc0d-126">Remarks</span></span>

<span data-ttu-id="dcc0d-127">Il s’agit de la méthode appelée par le fournisseur de saisie semi-automatique lorsqu’il est sur le présent d’afficher l’interface utilisateur de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="dcc0d-127">This is the method that the auto complete provider calls when it is about to show the auto complete user interface.</span></span> <span data-ttu-id="dcc0d-128">Le client modifie le rectangle préféré du fournisseur spécifié par *prcACList* à l’aide de l’argument *prcModified* .</span><span class="sxs-lookup"><span data-stu-id="dcc0d-128">The client modifies the provider's preferred rectangle specified by *prcACList* through *prcModified* argument.</span></span>

<span data-ttu-id="dcc0d-129">Appelez la [**méthode ITipAutocompleteClient :: RequestShowUI**](itipautocompleteclient-requestshowui.md) pour définir le handle de fenêtre de la liste de saisie semi-automatique contextuelle avant d’appeler **PreferredRects**.</span><span class="sxs-lookup"><span data-stu-id="dcc0d-129">Call the [**ITipAutocompleteClient::RequestShowUI Method**](itipautocompleteclient-requestshowui.md) to set the popup auto complete list window handle before you call **PreferredRects**.</span></span> <span data-ttu-id="dcc0d-130">Dans le cas contraire, une erreur d' **E \_ INVALIDARG** se produira lors de l’appel de **PreferredRects**.</span><span class="sxs-lookup"><span data-stu-id="dcc0d-130">Failure to do so will cause an **E\_INVALIDARG** error when calling **PreferredRects**.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcc0d-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dcc0d-131">Requirements</span></span>



| <span data-ttu-id="dcc0d-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dcc0d-132">Requirement</span></span> | <span data-ttu-id="dcc0d-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="dcc0d-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcc0d-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dcc0d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="dcc0d-135">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dcc0d-135">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="dcc0d-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dcc0d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="dcc0d-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="dcc0d-137">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="dcc0d-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="dcc0d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcc0d-139"><dt>TipAutoComplete. h (nécessite également PenInputPanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="dcc0d-139"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="dcc0d-140">DLL</span><span class="sxs-lookup"><span data-stu-id="dcc0d-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcc0d-141"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dcc0d-141"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="dcc0d-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dcc0d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcc0d-143">**Interface ITipAutocompleteClient**</span><span class="sxs-lookup"><span data-stu-id="dcc0d-143">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="dcc0d-144">**ITipAutocompleteClient :: RequestShowUI, méthode**</span><span class="sxs-lookup"><span data-stu-id="dcc0d-144">**ITipAutocompleteClient::RequestShowUI Method**</span></span>](itipautocompleteclient-requestshowui.md)
</dt> <dt>

[<span data-ttu-id="dcc0d-145">Référence du panneau de saisie de texte</span><span class="sxs-lookup"><span data-stu-id="dcc0d-145">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




