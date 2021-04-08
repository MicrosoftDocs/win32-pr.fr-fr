---
description: Annule l’inscription du fournisseur associé.
ms.assetid: b5edc33d-dfd0-4350-b8cd-eaa30b726771
title: 'ITipAutocompleteClient :: UnadviseProvider, méthode (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.UnadviseProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 1100ebb700ef2fb769a13f9b62aacf5c1d007e0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865821"
---
# <a name="itipautocompleteclientunadviseprovider-method"></a><span data-ttu-id="0aaab-103">ITipAutocompleteClient :: UnadviseProvider, méthode</span><span class="sxs-lookup"><span data-stu-id="0aaab-103">ITipAutocompleteClient::UnadviseProvider method</span></span>

<span data-ttu-id="0aaab-104">Annule l’inscription du fournisseur associé.</span><span class="sxs-lookup"><span data-stu-id="0aaab-104">Unregisters the associated provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="0aaab-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0aaab-105">Syntax</span></span>


```C++
HRESULT UnadviseProvider(
  [in] HWND                   hWndField,
  [in] ITipAutocompleProvider *pIACProvider
);
```



## <a name="parameters"></a><span data-ttu-id="0aaab-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0aaab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0aaab-107">*hWndField* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0aaab-107">*hWndField* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0aaab-108">Handle de fenêtre du champ qui fournit la fonctionnalité de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="0aaab-108">Window handle of the field which provide the auto complete feature.</span></span>

</dd> <dt>

<span data-ttu-id="0aaab-109">*pIACProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0aaab-109">*pIACProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0aaab-110">Pointeur d’interface vers l’interface du fournisseur de saisie semi-automatique dont l’inscription doit être annulée.</span><span class="sxs-lookup"><span data-stu-id="0aaab-110">Interface pointer to the auto complete provider interface to be unregistered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0aaab-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0aaab-111">Return value</span></span>

<span data-ttu-id="0aaab-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="0aaab-112">This method can return one of these values.</span></span>



| <span data-ttu-id="0aaab-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0aaab-113">Return code</span></span>                                                                            | <span data-ttu-id="0aaab-114">Description</span><span class="sxs-lookup"><span data-stu-id="0aaab-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="0aaab-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0aaab-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="0aaab-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="0aaab-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="0aaab-117"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="0aaab-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="0aaab-118">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="0aaab-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0aaab-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0aaab-119">Requirements</span></span>



| <span data-ttu-id="0aaab-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0aaab-120">Requirement</span></span> | <span data-ttu-id="0aaab-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="0aaab-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aaab-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0aaab-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0aaab-123">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0aaab-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="0aaab-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0aaab-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0aaab-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0aaab-125">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="0aaab-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="0aaab-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0aaab-127"><dt>TipAutoComplete. h (nécessite également PenInputPanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0aaab-127"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0aaab-128">DLL</span><span class="sxs-lookup"><span data-stu-id="0aaab-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0aaab-129"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0aaab-129"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="0aaab-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0aaab-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aaab-131">**Interface ITipAutocompleteClient**</span><span class="sxs-lookup"><span data-stu-id="0aaab-131">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="0aaab-132">Référence du panneau de saisie de texte</span><span class="sxs-lookup"><span data-stu-id="0aaab-132">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




