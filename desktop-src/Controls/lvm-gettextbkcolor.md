---
title: Message LVM_GETTEXTBKCOLOR (commctrl. h)
description: Récupère la couleur d’arrière-plan du texte d’un contrôle d’affichage de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetTextBkColor.
ms.assetid: 3d2c8be8-d7f9-4aa7-b358-f7effc6dbb25
keywords:
- LVM_GETTEXTBKCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETTEXTBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36bf5b6700904c5af47ef47e749dfa753c5ff8cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942645"
---
# <a name="lvm_gettextbkcolor-message"></a><span data-ttu-id="07162-105">\_Message GETTEXTBKCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="07162-105">LVM\_GETTEXTBKCOLOR message</span></span>

<span data-ttu-id="07162-106">Récupère la couleur d’arrière-plan du texte d’un contrôle d’affichage de liste.</span><span class="sxs-lookup"><span data-stu-id="07162-106">Retrieves the text background color of a list-view control.</span></span> <span data-ttu-id="07162-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetTextBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettextbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="07162-107">You can send this message explicitly or by using the [**ListView\_GetTextBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettextbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="07162-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="07162-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07162-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="07162-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="07162-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="07162-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="07162-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="07162-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="07162-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="07162-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07162-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="07162-113">Return value</span></span>

<span data-ttu-id="07162-114">Retourne la couleur d’arrière-plan du texte.</span><span class="sxs-lookup"><span data-stu-id="07162-114">Returns the background color of the text.</span></span>

## <a name="requirements"></a><span data-ttu-id="07162-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07162-115">Requirements</span></span>



| <span data-ttu-id="07162-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07162-116">Requirement</span></span> | <span data-ttu-id="07162-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="07162-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="07162-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07162-118">Minimum supported client</span></span><br/> | <span data-ttu-id="07162-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07162-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="07162-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07162-120">Minimum supported server</span></span><br/> | <span data-ttu-id="07162-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07162-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="07162-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="07162-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="07162-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="07162-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





