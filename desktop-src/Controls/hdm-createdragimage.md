---
title: Message HDM_CREATEDRAGIMAGE (commctrl. h)
description: Crée une version semi-transparente de l’image d’un élément à utiliser comme image de glissement. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ CreateDragImage.
ms.assetid: 1b9dc515-d327-4634-a424-cc15a32f0f7c
keywords:
- HDM_CREATEDRAGIMAGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9e801ad9771205b5f2e6df8e37bb0a0ad7f0bc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033018"
---
# <a name="hdm_createdragimage-message"></a><span data-ttu-id="b1f09-105">\_Message HDM CREATEDRAGIMAGE</span><span class="sxs-lookup"><span data-stu-id="b1f09-105">HDM\_CREATEDRAGIMAGE message</span></span>

<span data-ttu-id="b1f09-106">Crée une version semi-transparente de l’image d’un élément à utiliser comme image de glissement.</span><span class="sxs-lookup"><span data-stu-id="b1f09-106">Creates a semi-transparent version of an item's image for use as a dragging image.</span></span> <span data-ttu-id="b1f09-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro d' [**en-tête \_ CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-header_createdragimage) .</span><span class="sxs-lookup"><span data-stu-id="b1f09-107">You can send this message explicitly or use the [**Header\_CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-header_createdragimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b1f09-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1f09-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1f09-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b1f09-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1f09-110">Index de base zéro de l’élément dans le contrôle header.</span><span class="sxs-lookup"><span data-stu-id="b1f09-110">The zero-based index of the item within the header control.</span></span> <span data-ttu-id="b1f09-111">L’image assignée à cet élément est la base de l’image transparente.</span><span class="sxs-lookup"><span data-stu-id="b1f09-111">The image assigned to this item is the basis for the transparent image.</span></span>

</dd> <dt>

<span data-ttu-id="b1f09-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b1f09-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b1f09-113">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="b1f09-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1f09-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b1f09-114">Return value</span></span>

<span data-ttu-id="b1f09-115">Retourne un handle vers une liste d’images qui contient la nouvelle image comme son seul élément.</span><span class="sxs-lookup"><span data-stu-id="b1f09-115">Returns a handle to an image list that contains the new image as its only element.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1f09-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1f09-116">Requirements</span></span>



| <span data-ttu-id="b1f09-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1f09-117">Requirement</span></span> | <span data-ttu-id="b1f09-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1f09-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1f09-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1f09-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b1f09-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1f09-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b1f09-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1f09-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b1f09-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1f09-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b1f09-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b1f09-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1f09-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1f09-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





