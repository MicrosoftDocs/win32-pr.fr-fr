---
title: Message TB_GETIMAGELIST (commctrl. h)
description: Récupère la liste d’images utilisée par un contrôle de barre d’outils pour afficher les boutons dans leur état par défaut. Un contrôle ToolBar utilise cette liste d’images pour afficher les boutons lorsqu’ils ne sont pas à chaud ou désactivés.
ms.assetid: 21edde99-019b-495c-a38b-4d686e124f8e
keywords:
- TB_GETIMAGELIST les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07a56b8b847bd212e703d3b512b255cf1693abf7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740276"
---
# <a name="tb_getimagelist-message"></a><span data-ttu-id="ae387-105">TO \_ GETIMAGELIST message</span><span class="sxs-lookup"><span data-stu-id="ae387-105">TB\_GETIMAGELIST message</span></span>

<span data-ttu-id="ae387-106">Récupère la liste d’images utilisée par un contrôle de barre d’outils pour afficher les boutons dans leur état par défaut.</span><span class="sxs-lookup"><span data-stu-id="ae387-106">Retrieves the image list that a toolbar control uses to display buttons in their default state.</span></span> <span data-ttu-id="ae387-107">Un contrôle ToolBar utilise cette liste d’images pour afficher les boutons lorsqu’ils ne sont pas à chaud ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="ae387-107">A toolbar control uses this image list to display buttons when they are not hot or disabled.</span></span>

## <a name="parameters"></a><span data-ttu-id="ae387-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae387-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae387-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ae387-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ae387-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="ae387-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ae387-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ae387-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ae387-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="ae387-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae387-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ae387-113">Return value</span></span>

<span data-ttu-id="ae387-114">Retourne le handle de la liste d’images, ou **null** si aucune liste d’images n’est définie.</span><span class="sxs-lookup"><span data-stu-id="ae387-114">Returns the handle to the image list, or **NULL** if no image list is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae387-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae387-115">Requirements</span></span>



| <span data-ttu-id="ae387-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae387-116">Requirement</span></span> | <span data-ttu-id="ae387-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae387-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae387-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae387-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ae387-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae387-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ae387-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae387-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ae387-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae387-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ae387-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="ae387-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae387-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae387-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





