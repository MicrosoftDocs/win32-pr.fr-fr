---
title: Message LVM_CREATEDRAGIMAGE (commctrl. h)
description: Crée une liste d’images de glissement pour l’élément spécifié. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView CreateDragImage.
ms.assetid: face4c8f-01ff-4f5a-a468-e306a50dae35
keywords:
- LVM_CREATEDRAGIMAGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace975b178fee85e2794b518a78b40b375c65ae7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102905"
---
# <a name="lvm_createdragimage-message"></a><span data-ttu-id="bbf7a-105">\_Message CREATEDRAGIMAGE LVM</span><span class="sxs-lookup"><span data-stu-id="bbf7a-105">LVM\_CREATEDRAGIMAGE message</span></span>

<span data-ttu-id="bbf7a-106">Crée une liste d’images de glissement pour l’élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="bbf7a-106">Creates a drag image list for the specified item.</span></span> <span data-ttu-id="bbf7a-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_createdragimage) .</span><span class="sxs-lookup"><span data-stu-id="bbf7a-107">You can send this message explicitly or by using the [**ListView\_CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_createdragimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bbf7a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bbf7a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbf7a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bbf7a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bbf7a-110">Index de l'élément.</span><span class="sxs-lookup"><span data-stu-id="bbf7a-110">The index of the item.</span></span>

</dd> <dt>

<span data-ttu-id="bbf7a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bbf7a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bbf7a-112">Pointeur vers une structure de [**points**](/previous-versions//dd162805(v=vs.85)) qui reçoit l’emplacement initial de l’angle supérieur gauche de l’image, en coordonnées de vue.</span><span class="sxs-lookup"><span data-stu-id="bbf7a-112">A pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that receives the initial location of the upper-left corner of the image, in view coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbf7a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bbf7a-113">Return value</span></span>

<span data-ttu-id="bbf7a-114">Retourne le handle de la liste d’images de glissement en cas de réussite, ou **null** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="bbf7a-114">Returns the handle to the drag image list if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbf7a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="bbf7a-115">Remarks</span></span>

<span data-ttu-id="bbf7a-116">Votre application est responsable de la destruction de la liste d’images lorsqu’elle n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="bbf7a-116">Your application is responsible for destroying the image list when it is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbf7a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bbf7a-117">Requirements</span></span>



| <span data-ttu-id="bbf7a-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bbf7a-118">Requirement</span></span> | <span data-ttu-id="bbf7a-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbf7a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bbf7a-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbf7a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bbf7a-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bbf7a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bbf7a-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbf7a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bbf7a-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bbf7a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bbf7a-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="bbf7a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbf7a-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbf7a-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

