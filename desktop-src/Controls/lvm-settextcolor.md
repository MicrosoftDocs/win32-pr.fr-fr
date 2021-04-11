---
title: Message LVM_SETTEXTCOLOR (commctrl. h)
description: Définit la couleur du texte d’un contrôle d’affichage de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SetTextColor.
ms.assetid: ff90c18b-0cd7-4331-bcd8-61044e891d1f
keywords:
- LVM_SETTEXTCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b30c965bd523cd5638c894b47fc4785ffbdd09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103356"
---
# <a name="lvm_settextcolor-message"></a><span data-ttu-id="9e142-105">\_Message SETTEXTCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="9e142-105">LVM\_SETTEXTCOLOR message</span></span>

<span data-ttu-id="9e142-106">Définit la couleur du texte d’un contrôle d’affichage de liste.</span><span class="sxs-lookup"><span data-stu-id="9e142-106">Sets the text color of a list-view control.</span></span> <span data-ttu-id="9e142-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ SetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextcolor) .</span><span class="sxs-lookup"><span data-stu-id="9e142-107">You can send this message explicitly or by using the [**ListView\_SetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9e142-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e142-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e142-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9e142-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9e142-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="9e142-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9e142-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9e142-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e142-112">[**COLORREF**](/windows/desktop/gdi/colorref) qui spécifie la nouvelle couleur de texte.</span><span class="sxs-lookup"><span data-stu-id="9e142-112">A [**COLORREF**](/windows/desktop/gdi/colorref) that specifies the new text color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e142-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9e142-113">Return value</span></span>

<span data-ttu-id="9e142-114">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="9e142-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e142-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e142-115">Requirements</span></span>



| <span data-ttu-id="9e142-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e142-116">Requirement</span></span> | <span data-ttu-id="9e142-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e142-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e142-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e142-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9e142-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9e142-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9e142-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e142-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9e142-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9e142-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9e142-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="9e142-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e142-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e142-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

