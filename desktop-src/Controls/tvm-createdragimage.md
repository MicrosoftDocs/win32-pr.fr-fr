---
title: Message TVM_CREATEDRAGIMAGE (commctrl. h)
description: Crée une image bitmap de glissement pour l’élément spécifié dans un contrôle Tree-View.
ms.assetid: fbe97921-c9d3-473c-933c-d6bc0599e24d
keywords:
- TVM_CREATEDRAGIMAGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 189b37affc6a4382541faea13199cacfcb9b7df5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103903"
---
# <a name="tvm_createdragimage-message"></a><span data-ttu-id="24ce7-104">TVM \_ CREATEDRAGIMAGE message</span><span class="sxs-lookup"><span data-stu-id="24ce7-104">TVM\_CREATEDRAGIMAGE message</span></span>

<span data-ttu-id="24ce7-105">Crée une image bitmap de glissement pour l’élément spécifié dans un contrôle Tree-View.</span><span class="sxs-lookup"><span data-stu-id="24ce7-105">Creates a dragging bitmap for the specified item in a tree-view control.</span></span> <span data-ttu-id="24ce7-106">Le message crée également une liste d’images pour l’image bitmap et ajoute l’image bitmap à la liste d’images.</span><span class="sxs-lookup"><span data-stu-id="24ce7-106">The message also creates an image list for the bitmap and adds the bitmap to the image list.</span></span> <span data-ttu-id="24ce7-107">Une application peut afficher l’image lors du déplacement de l’élément à l’aide des fonctions de la liste d’images.</span><span class="sxs-lookup"><span data-stu-id="24ce7-107">An application can display the image when dragging the item by using the image list functions.</span></span> <span data-ttu-id="24ce7-108">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ CreateDragImage TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_createdragimage) .</span><span class="sxs-lookup"><span data-stu-id="24ce7-108">You can send this message explicitly or by using the [**TreeView\_CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_createdragimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="24ce7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="24ce7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24ce7-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="24ce7-110">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="24ce7-111">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="24ce7-111">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="24ce7-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="24ce7-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24ce7-113">Handle de l’élément qui reçoit la nouvelle bitmap de glissement.</span><span class="sxs-lookup"><span data-stu-id="24ce7-113">Handle to the item that receives the new dragging bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24ce7-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="24ce7-114">Return value</span></span>

<span data-ttu-id="24ce7-115">Retourne le handle de la liste d’images à laquelle la bitmap glissante a été ajoutée en cas de réussite, ou **null** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="24ce7-115">Returns the handle to the image list to which the dragging bitmap was added if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="24ce7-116">Notes</span><span class="sxs-lookup"><span data-stu-id="24ce7-116">Remarks</span></span>

<span data-ttu-id="24ce7-117">Si vous créez un contrôle Tree-View sans liste d’images associée, vous ne pouvez pas utiliser le message **TVM \_ CREATEDRAGIMAGE** pour créer l’image à afficher pendant une opération glisser.</span><span class="sxs-lookup"><span data-stu-id="24ce7-117">If you create a tree-view control without an associated image list, you cannot use the **TVM\_CREATEDRAGIMAGE** message to create the image to display during a drag operation.</span></span> <span data-ttu-id="24ce7-118">Vous devez implémenter votre propre méthode de création d’un curseur de glissement.</span><span class="sxs-lookup"><span data-stu-id="24ce7-118">You must implement your own method of creating a drag cursor.</span></span>

<span data-ttu-id="24ce7-119">Votre application est responsable de la destruction de la liste d’images lorsqu’elle n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="24ce7-119">Your application is responsible for destroying the image list when it is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="24ce7-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24ce7-120">Requirements</span></span>



| <span data-ttu-id="24ce7-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24ce7-121">Requirement</span></span> | <span data-ttu-id="24ce7-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="24ce7-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="24ce7-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24ce7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="24ce7-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24ce7-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="24ce7-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24ce7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="24ce7-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24ce7-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="24ce7-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="24ce7-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="24ce7-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="24ce7-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





