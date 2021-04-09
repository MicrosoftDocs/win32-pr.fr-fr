---
title: Message LVM_SETITEMPOSITION32 (commctrl. h)
description: Déplace un élément à une position spécifiée dans un contrôle List View (doit être en mode icône ou petite icône).
ms.assetid: 77db5fd0-bbc3-47ad-95ef-61ef4ac022bc
keywords:
- LVM_SETITEMPOSITION32 les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETITEMPOSITION32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 450963e4adf5ea2b0644f8d155145ba577efab83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032918"
---
# <a name="lvm_setitemposition32-message"></a><span data-ttu-id="f6f21-104">\_Message SETITEMPOSITION32 LVM</span><span class="sxs-lookup"><span data-stu-id="f6f21-104">LVM\_SETITEMPOSITION32 message</span></span>

<span data-ttu-id="f6f21-105">Déplace un élément à une position spécifiée dans un contrôle List View (doit être en mode icône ou petite icône).</span><span class="sxs-lookup"><span data-stu-id="f6f21-105">Moves an item to a specified position in a list-view control (must be in icon or small icon view).</span></span> <span data-ttu-id="f6f21-106">Ce message diffère du message [**\_ SETITEMPOSITION LVM**](lvm-setitemposition.md) en ce qu’il utilise des coordonnées 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f6f21-106">This message differs from the [**LVM\_SETITEMPOSITION**](lvm-setitemposition.md) message in that it uses 32-bit coordinates.</span></span> <span data-ttu-id="f6f21-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ SetItemPosition32**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition32) .</span><span class="sxs-lookup"><span data-stu-id="f6f21-107">You can send this message explicitly or by using the [**ListView\_SetItemPosition32**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition32) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f6f21-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f6f21-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6f21-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f6f21-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6f21-110">Index de l’élément de vue de liste pour lequel définir la position.</span><span class="sxs-lookup"><span data-stu-id="f6f21-110">Index of the list-view item for which to set the position.</span></span>

</dd> <dt>

<span data-ttu-id="f6f21-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f6f21-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6f21-112">Pointeur vers une structure de [**points**](/previous-versions//dd162805(v=vs.85)) qui contient la nouvelle position de l’élément, en coordonnées de vue de liste.</span><span class="sxs-lookup"><span data-stu-id="f6f21-112">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that contains the new position of the item, in list-view coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6f21-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f6f21-113">Return value</span></span>

<span data-ttu-id="f6f21-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="f6f21-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6f21-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f6f21-115">Requirements</span></span>



| <span data-ttu-id="f6f21-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f6f21-116">Requirement</span></span> | <span data-ttu-id="f6f21-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6f21-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f6f21-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6f21-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f6f21-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f6f21-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f6f21-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6f21-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f6f21-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f6f21-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f6f21-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="f6f21-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6f21-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6f21-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

