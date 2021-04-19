---
description: Déplace un contexte de tablette vers l’avant ou l’arrière de la file d’attente d’entrée.
ms.assetid: ef4521b5-776b-46dc-864a-625bc221054a
title: 'ITabletContextP :: superposition, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.Overlap
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: b009bc08dddb15bc7aa5b12c8846ea66c4a52e56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534707"
---
# <a name="itabletcontextpoverlap-method"></a><span data-ttu-id="5c943-103">ITabletContextP :: superposition, méthode</span><span class="sxs-lookup"><span data-stu-id="5c943-103">ITabletContextP::Overlap method</span></span>

<span data-ttu-id="5c943-104">Déplace un contexte de tablette vers l’avant ou l’arrière de la file d’attente d’entrée.</span><span class="sxs-lookup"><span data-stu-id="5c943-104">Moves a tablet context to the front or back of the input queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c943-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5c943-105">Syntax</span></span>


```C++
HRESULT Overlap(
  [in]  BOOL  bTop,
  [out] DWORD *pdwtcid
);
```



## <a name="parameters"></a><span data-ttu-id="5c943-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5c943-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c943-107">*bTop* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5c943-107">*bTop* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c943-108">Indique si le contexte de tablette doit être déplacé vers le haut ou le bas de la file d’attente d’entrée.</span><span class="sxs-lookup"><span data-stu-id="5c943-108">Indicates if the tablet context should be moved to the top or bottom of the input queue.</span></span>

</dd> <dt>

<span data-ttu-id="5c943-109">*pdwtcid* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5c943-109">*pdwtcid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c943-110">Identificateur du contexte de tablette.</span><span class="sxs-lookup"><span data-stu-id="5c943-110">The tablet context identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c943-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5c943-111">Return value</span></span>

<span data-ttu-id="5c943-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="5c943-112">This method can return one of these values.</span></span>



| <span data-ttu-id="5c943-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5c943-113">Return code</span></span>                                                                            | <span data-ttu-id="5c943-114">Description</span><span class="sxs-lookup"><span data-stu-id="5c943-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="5c943-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5c943-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="5c943-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="5c943-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="5c943-117"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="5c943-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="5c943-118">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="5c943-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5c943-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5c943-119">Requirements</span></span>



| <span data-ttu-id="5c943-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5c943-120">Requirement</span></span> | <span data-ttu-id="5c943-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c943-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c943-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c943-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5c943-123">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c943-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5c943-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c943-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5c943-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c943-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5c943-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5c943-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="5c943-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5c943-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c943-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c943-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c943-129">**Interface ITabletContextP**</span><span class="sxs-lookup"><span data-stu-id="5c943-129">**ITabletContextP Interface**</span></span>](itabletcontextp.md)
</dt> </dl>

 

 




