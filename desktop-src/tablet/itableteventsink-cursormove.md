---
description: Se produit lorsque le curseur se déplace sur le digitaliseur de tablette.
ms.assetid: cd2863af-59a9-4dd0-a679-84861a70ef53
title: 'ITabletEventSink :: CursorMove, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorMove
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f6950e0b30c1b8fc8ccf3e60a8aaa05b9eeb3215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541984"
---
# <a name="itableteventsinkcursormove-method"></a><span data-ttu-id="081e2-103">ITabletEventSink :: CursorMove, méthode</span><span class="sxs-lookup"><span data-stu-id="081e2-103">ITabletEventSink::CursorMove method</span></span>

<span data-ttu-id="081e2-104">Se produit lorsque le curseur se déplace sur le digitaliseur de tablette.</span><span class="sxs-lookup"><span data-stu-id="081e2-104">Occurs when the cursor moves over the tablet digitizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="081e2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="081e2-105">Syntax</span></span>


```C++
HRESULT CursorMove(
   TABLET_CONTEXT_ID tcid,
   CURSOR_ID         cid,
   HWND              hWnd,
   LONG              xPos,
   LONG              yPos
);
```



## <a name="parameters"></a><span data-ttu-id="081e2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="081e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="081e2-107">*tcid*</span><span class="sxs-lookup"><span data-stu-id="081e2-107">*tcid*</span></span> 
</dt> <dd>

<span data-ttu-id="081e2-108">Dentifier unique du digitaliseur de tablette.</span><span class="sxs-lookup"><span data-stu-id="081e2-108">Unique dentifier of the tablet digitizer.</span></span>

</dd> <dt>

<span data-ttu-id="081e2-109">*confirmation*</span><span class="sxs-lookup"><span data-stu-id="081e2-109">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="081e2-110">Identificateur unique du stylet de tablette.</span><span class="sxs-lookup"><span data-stu-id="081e2-110">Unique identifier of the tablet stylus.</span></span>

</dd> <dt>

<span data-ttu-id="081e2-111">*hWnd*</span><span class="sxs-lookup"><span data-stu-id="081e2-111">*hWnd*</span></span> 
</dt> <dd>

<span data-ttu-id="081e2-112">Fenêtre sur laquelle le curseur a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="081e2-112">The window over which the cursor moved.</span></span>

</dd> <dt>

<span data-ttu-id="081e2-113">*xPos*</span><span class="sxs-lookup"><span data-stu-id="081e2-113">*xPos*</span></span> 
</dt> <dd>

<span data-ttu-id="081e2-114">Position X du stylet.</span><span class="sxs-lookup"><span data-stu-id="081e2-114">The X position of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="081e2-115">*PosY*</span><span class="sxs-lookup"><span data-stu-id="081e2-115">*yPos*</span></span> 
</dt> <dd>

<span data-ttu-id="081e2-116">Position Y du stylet.</span><span class="sxs-lookup"><span data-stu-id="081e2-116">The Y position of the stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="081e2-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="081e2-117">Return value</span></span>

<span data-ttu-id="081e2-118">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="081e2-118">This method can return one of these values.</span></span>



| <span data-ttu-id="081e2-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="081e2-119">Return code</span></span>                                                                            | <span data-ttu-id="081e2-120">Description</span><span class="sxs-lookup"><span data-stu-id="081e2-120">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="081e2-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="081e2-121"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="081e2-122">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="081e2-122">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="081e2-123"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="081e2-123"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="081e2-124">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="081e2-124">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="081e2-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="081e2-125">Requirements</span></span>



| <span data-ttu-id="081e2-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="081e2-126">Requirement</span></span> | <span data-ttu-id="081e2-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="081e2-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="081e2-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="081e2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="081e2-129">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="081e2-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="081e2-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="081e2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="081e2-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="081e2-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="081e2-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="081e2-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="081e2-133"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="081e2-133"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="081e2-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="081e2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="081e2-135">**Interface ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="081e2-135">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




