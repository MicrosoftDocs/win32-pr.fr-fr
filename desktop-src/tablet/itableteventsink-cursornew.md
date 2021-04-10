---
description: Se produit lorsqu’un nouveau stylet est ajouté au système.
ms.assetid: bd0f0d2a-c0d9-48fc-bc90-f63f038639f3
title: 'ITabletEventSink :: CursorNew, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorNew
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 31db152eb15d6f980234dc556e277691d3f14959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210617"
---
# <a name="itableteventsinkcursornew-method"></a><span data-ttu-id="d2d17-103">ITabletEventSink :: CursorNew, méthode</span><span class="sxs-lookup"><span data-stu-id="d2d17-103">ITabletEventSink::CursorNew method</span></span>

<span data-ttu-id="d2d17-104">Se produit lorsqu’un nouveau stylet est ajouté au système.</span><span class="sxs-lookup"><span data-stu-id="d2d17-104">Occurs when a new stylus is added to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2d17-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2d17-105">Syntax</span></span>


```C++
HRESULT CursorNew(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a><span data-ttu-id="d2d17-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2d17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2d17-107">*TCID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2d17-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2d17-108">Identificateur du contexte de tablette dans lequel le nouveau stylet a été ajouté.</span><span class="sxs-lookup"><span data-stu-id="d2d17-108">The identifier of the tablet context where the new stylus was added.</span></span>

</dd> <dt>

<span data-ttu-id="d2d17-109">*confirmation*</span><span class="sxs-lookup"><span data-stu-id="d2d17-109">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="d2d17-110">Identificateur du nouvel objet stylet.</span><span class="sxs-lookup"><span data-stu-id="d2d17-110">The identifier of the new stylus object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2d17-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d2d17-111">Return value</span></span>

<span data-ttu-id="d2d17-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="d2d17-112">This method can return one of these values.</span></span>



| <span data-ttu-id="d2d17-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d2d17-113">Return code</span></span>                                                                            | <span data-ttu-id="d2d17-114">Description</span><span class="sxs-lookup"><span data-stu-id="d2d17-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="d2d17-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d2d17-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="d2d17-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="d2d17-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="d2d17-117"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="d2d17-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="d2d17-118">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="d2d17-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d2d17-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2d17-119">Requirements</span></span>



| <span data-ttu-id="d2d17-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2d17-120">Requirement</span></span> | <span data-ttu-id="d2d17-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2d17-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2d17-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2d17-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d2d17-123">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2d17-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d2d17-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2d17-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d2d17-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2d17-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d2d17-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d2d17-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="d2d17-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d2d17-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2d17-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2d17-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2d17-129">**Interface ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="d2d17-129">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




