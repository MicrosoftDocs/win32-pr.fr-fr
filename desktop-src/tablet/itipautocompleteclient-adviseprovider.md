---
description: Inscrit le fournisseur auprès du client pour permettre au client d’appeler l’objet fournisseur de saisie semi-automatique de l’application.
ms.assetid: 7b761b30-66f7-454a-9e0d-f45c8099f19f
title: 'ITipAutocompleteClient :: AdviseProvider, méthode (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.AdviseProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 9ef35ac730089403ac47c14421de96e75a022192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526114"
---
# <a name="itipautocompleteclientadviseprovider-method"></a><span data-ttu-id="053ad-103">ITipAutocompleteClient :: AdviseProvider, méthode</span><span class="sxs-lookup"><span data-stu-id="053ad-103">ITipAutocompleteClient::AdviseProvider method</span></span>

<span data-ttu-id="053ad-104">Inscrit le fournisseur auprès du client pour permettre au client d’appeler l’objet fournisseur de saisie semi-automatique de l’application.</span><span class="sxs-lookup"><span data-stu-id="053ad-104">Registers the provider with the client to enable the client to call the application's auto complete provider object.</span></span>

## <a name="syntax"></a><span data-ttu-id="053ad-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="053ad-105">Syntax</span></span>


```C++
HRESULT AdviseProvider(
  [in] HWND                     hWndField,
  [in] ITipAutocompleteProvider *pIACProvider
);
```



## <a name="parameters"></a><span data-ttu-id="053ad-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="053ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="053ad-107">*hWndField* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="053ad-107">*hWndField* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="053ad-108">Handle de fenêtre du champ qui fournit la fonctionnalité de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="053ad-108">The window handle of the field which provide the auto complete feature.</span></span>

</dd> <dt>

<span data-ttu-id="053ad-109">*pIACProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="053ad-109">*pIACProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="053ad-110">Pointeur d’interface vers l’interface du fournisseur de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="053ad-110">The interface pointer to the auto complete provider interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="053ad-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="053ad-111">Return value</span></span>

<span data-ttu-id="053ad-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="053ad-112">This method can return one of these values.</span></span>



| <span data-ttu-id="053ad-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="053ad-113">Return code</span></span>                                                                            | <span data-ttu-id="053ad-114">Description</span><span class="sxs-lookup"><span data-stu-id="053ad-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="053ad-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="053ad-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="053ad-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="053ad-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="053ad-117"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="053ad-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="053ad-118">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="053ad-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="053ad-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="053ad-119">Requirements</span></span>



| <span data-ttu-id="053ad-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="053ad-120">Requirement</span></span> | <span data-ttu-id="053ad-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="053ad-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="053ad-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="053ad-122">Minimum supported client</span></span><br/> | <span data-ttu-id="053ad-123">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="053ad-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="053ad-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="053ad-124">Minimum supported server</span></span><br/> | <span data-ttu-id="053ad-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="053ad-125">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="053ad-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="053ad-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="053ad-127"><dt>TipAutoComplete. h (nécessite également PenInputPanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="053ad-127"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="053ad-128">DLL</span><span class="sxs-lookup"><span data-stu-id="053ad-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="053ad-129"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="053ad-129"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="053ad-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="053ad-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="053ad-131">**Interface ITipAutocompleteClient**</span><span class="sxs-lookup"><span data-stu-id="053ad-131">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="053ad-132">**ITipAutocompleteClient :: UnadviseProvider, méthode**</span><span class="sxs-lookup"><span data-stu-id="053ad-132">**ITipAutocompleteClient::UnadviseProvider Method**</span></span>](itipautocompleteclient-unadviseprovider.md)
</dt> <dt>

[<span data-ttu-id="053ad-133">Référence du panneau de saisie de texte</span><span class="sxs-lookup"><span data-stu-id="053ad-133">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




