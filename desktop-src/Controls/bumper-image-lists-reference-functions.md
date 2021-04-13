---
title: Fonctions de liste d’images
description: Fonctions de liste d’images
ms.assetid: b5754633-f673-414e-9e0b-3f6f211ecd2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb3e877e4f264aa9c0440b183a2c528592b6ccee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104321926"
---
# <a name="image-list-functions"></a><span data-ttu-id="7908e-103">Fonctions de liste d’images</span><span class="sxs-lookup"><span data-stu-id="7908e-103">Image List Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7908e-104">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="7908e-104">In This Section</span></span>

-   [<span data-ttu-id="7908e-105">**HIMAGELIST \_ QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="7908e-105">**HIMAGELIST\_QueryInterface**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-himagelist_queryinterface)
-   [<span data-ttu-id="7908e-106">**\_Ajouter ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-106">**ImageList\_Add**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add)
-   [<span data-ttu-id="7908e-107">**\_AddMasked ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-107">**ImageList\_AddMasked**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addmasked)
-   [<span data-ttu-id="7908e-108">**\_BeginDrag ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-108">**ImageList\_BeginDrag**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag)
-   [<span data-ttu-id="7908e-109">**ImageList \_ CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="7908e-109">**ImageList\_CoCreateInstance**</span></span>](/windows/desktop/api/CommonControls/nf-commoncontrols-imagelist_cocreateinstance)
-   [<span data-ttu-id="7908e-110">**\_Copie ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-110">**ImageList\_Copy**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_copy)
-   [<span data-ttu-id="7908e-111">**\_Créer ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-111">**ImageList\_Create**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create)
-   [<span data-ttu-id="7908e-112">**\_Supprimer ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-112">**ImageList\_Destroy**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_destroy)
-   [<span data-ttu-id="7908e-113">**ImageList \_ DragEnter**</span><span class="sxs-lookup"><span data-stu-id="7908e-113">**ImageList\_DragEnter**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragenter)
-   [<span data-ttu-id="7908e-114">**\_DragLeave ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-114">**ImageList\_DragLeave**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragleave)
-   [<span data-ttu-id="7908e-115">**\_DragMove ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-115">**ImageList\_DragMove**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove)
-   [<span data-ttu-id="7908e-116">**\_DragShowNolock ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-116">**ImageList\_DragShowNolock**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragshownolock)
-   [<span data-ttu-id="7908e-117">**\_Dessin ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-117">**ImageList\_Draw**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw)
-   [<span data-ttu-id="7908e-118">**\_DrawEx ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-118">**ImageList\_DrawEx**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex)
-   [<span data-ttu-id="7908e-119">**\_DrawIndirect ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-119">**ImageList\_DrawIndirect**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawindirect)
-   [<span data-ttu-id="7908e-120">**\_Doublon ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-120">**ImageList\_Duplicate**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_duplicate)
-   [<span data-ttu-id="7908e-121">**\_EndDrag ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-121">**ImageList\_EndDrag**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag)
-   [<span data-ttu-id="7908e-122">**\_GetBkColor ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-122">**ImageList\_GetBkColor**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getbkcolor)
-   [<span data-ttu-id="7908e-123">**\_GetDragImage ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-123">**ImageList\_GetDragImage**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getdragimage)
-   [<span data-ttu-id="7908e-124">**\_GetIcon ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-124">**ImageList\_GetIcon**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_geticon)
-   [<span data-ttu-id="7908e-125">**\_GetIconSize ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-125">**ImageList\_GetIconSize**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_geticonsize)
-   [<span data-ttu-id="7908e-126">**\_GetImageCount ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-126">**ImageList\_GetImageCount**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getimagecount)
-   [<span data-ttu-id="7908e-127">**\_GetImageInfo ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-127">**ImageList\_GetImageInfo**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getimageinfo)
-   [<span data-ttu-id="7908e-128">**\_LoadImage ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-128">**ImageList\_LoadImage**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_loadimagea)
-   [<span data-ttu-id="7908e-129">**\_Fusion ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-129">**ImageList\_Merge**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_merge)
-   [<span data-ttu-id="7908e-130">**\_Lecture ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-130">**ImageList\_Read**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_read)
-   [<span data-ttu-id="7908e-131">**\_ReadEx ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-131">**ImageList\_ReadEx**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_readex)
-   [<span data-ttu-id="7908e-132">**ImageList \_ Supprimer**</span><span class="sxs-lookup"><span data-stu-id="7908e-132">**ImageList\_Remove**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_remove)
-   [<span data-ttu-id="7908e-133">**ImageList- \_ remplacer**</span><span class="sxs-lookup"><span data-stu-id="7908e-133">**ImageList\_Replace**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_replace)
-   [<span data-ttu-id="7908e-134">**\_ReplaceIcon ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-134">**ImageList\_ReplaceIcon**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_replaceicon)
-   [<span data-ttu-id="7908e-135">**\_SetBkColor ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-135">**ImageList\_SetBkColor**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setbkcolor)
-   [<span data-ttu-id="7908e-136">**\_SetColorTable ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-136">**ImageList\_SetColorTable**</span></span>](imagelist-setcolortable.md)
-   [<span data-ttu-id="7908e-137">**\_SetDragCursorImage ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-137">**ImageList\_SetDragCursorImage**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setdragcursorimage)
-   [<span data-ttu-id="7908e-138">**\_SetIconSize ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-138">**ImageList\_SetIconSize**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_seticonsize)
-   [<span data-ttu-id="7908e-139">**\_SetImageCount ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-139">**ImageList\_SetImageCount**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setimagecount)
-   [<span data-ttu-id="7908e-140">**\_SetOverlayImage ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-140">**ImageList\_SetOverlayImage**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage)
-   [<span data-ttu-id="7908e-141">**\_Écriture ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-141">**ImageList\_Write**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_write)
-   [<span data-ttu-id="7908e-142">**\_WriteEx ImageList**</span><span class="sxs-lookup"><span data-stu-id="7908e-142">**ImageList\_WriteEx**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_writeex)

 

 




