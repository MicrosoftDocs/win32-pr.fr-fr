---
description: Récupère l’objet bouton spécifié à partir d’un stylet de tablette.
ms.assetid: 83a26703-4501-4f43-9e86-c5c753347012
title: 'ITabletCursor :: GetButton, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetButton
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 0b9e8e1337cacdb26d8c124d10e0a886748e70fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541869"
---
# <a name="itabletcursorgetbutton-method"></a><span data-ttu-id="e78e4-103">ITabletCursor :: GetButton, méthode</span><span class="sxs-lookup"><span data-stu-id="e78e4-103">ITabletCursor::GetButton method</span></span>

<span data-ttu-id="e78e4-104">Récupère l’objet bouton spécifié à partir d’un stylet de tablette.</span><span class="sxs-lookup"><span data-stu-id="e78e4-104">Retrieves the specified button object from a tablet stylus.</span></span>

## <a name="syntax"></a><span data-ttu-id="e78e4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e78e4-105">Syntax</span></span>


```C++
HRESULT GetButton(
  [in]  ULONG               iButton,
  [out] ITabletCursorButton **ppButton
);
```



## <a name="parameters"></a><span data-ttu-id="e78e4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e78e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e78e4-107">*iButton* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e78e4-107">*iButton* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e78e4-108">Identificateur du bouton à récupérer.</span><span class="sxs-lookup"><span data-stu-id="e78e4-108">Identifier of the button to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="e78e4-109">*ppButton* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e78e4-109">*ppButton* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e78e4-110">Objet bouton spécifié par le paramètre *iButton* .</span><span class="sxs-lookup"><span data-stu-id="e78e4-110">The button object specified by the *iButton* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e78e4-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e78e4-111">Return value</span></span>

<span data-ttu-id="e78e4-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="e78e4-112">This method can return one of these values.</span></span>



| <span data-ttu-id="e78e4-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e78e4-113">Return code</span></span>                                                                            | <span data-ttu-id="e78e4-114">Description</span><span class="sxs-lookup"><span data-stu-id="e78e4-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="e78e4-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e78e4-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="e78e4-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="e78e4-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="e78e4-117"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="e78e4-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="e78e4-118">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="e78e4-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e78e4-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e78e4-119">Requirements</span></span>



| <span data-ttu-id="e78e4-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e78e4-120">Requirement</span></span> | <span data-ttu-id="e78e4-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="e78e4-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e78e4-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e78e4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e78e4-123">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e78e4-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e78e4-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e78e4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e78e4-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e78e4-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e78e4-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e78e4-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="e78e4-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e78e4-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e78e4-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e78e4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e78e4-129">**Interface ITabletCursor**</span><span class="sxs-lookup"><span data-stu-id="e78e4-129">**ITabletCursor Interface**</span></span>](itabletcursor.md)
</dt> </dl>

 

 




