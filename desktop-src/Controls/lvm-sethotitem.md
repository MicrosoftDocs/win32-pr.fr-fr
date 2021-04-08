---
title: Message LVM_SETHOTITEM (commctrl. h)
description: Définit l’élément réactif pour un contrôle d’affichage de liste. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView SetHotItem.
ms.assetid: 0aa2b15d-4983-4234-9863-f1fdee09f913
keywords:
- LVM_SETHOTITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82c17bc67c530581b79a87030b31b655f856dd0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739941"
---
# <a name="lvm_sethotitem-message"></a><span data-ttu-id="2aa74-105">\_Message SETHOTITEM LVM</span><span class="sxs-lookup"><span data-stu-id="2aa74-105">LVM\_SETHOTITEM message</span></span>

<span data-ttu-id="2aa74-106">Définit l’élément réactif pour un contrôle d’affichage de liste.</span><span class="sxs-lookup"><span data-stu-id="2aa74-106">Sets the hot item for a list-view control.</span></span> <span data-ttu-id="2aa74-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ SetHotItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotitem) .</span><span class="sxs-lookup"><span data-stu-id="2aa74-107">You can send this message explicitly or use the [**ListView\_SetHotItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2aa74-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2aa74-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2aa74-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2aa74-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2aa74-110">Index de base zéro de l’élément à définir comme élément réactif.</span><span class="sxs-lookup"><span data-stu-id="2aa74-110">Zero-based index of the item to be set as the hot item.</span></span>

</dd> <dt>

<span data-ttu-id="2aa74-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2aa74-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2aa74-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="2aa74-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2aa74-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2aa74-113">Return value</span></span>

<span data-ttu-id="2aa74-114">Retourne l’index de l’élément qui était précédemment chaud.</span><span class="sxs-lookup"><span data-stu-id="2aa74-114">Returns the index of the item that was previously hot.</span></span>

## <a name="requirements"></a><span data-ttu-id="2aa74-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2aa74-115">Requirements</span></span>



| <span data-ttu-id="2aa74-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2aa74-116">Requirement</span></span> | <span data-ttu-id="2aa74-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="2aa74-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2aa74-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2aa74-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2aa74-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2aa74-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2aa74-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2aa74-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2aa74-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2aa74-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2aa74-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="2aa74-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2aa74-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2aa74-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





