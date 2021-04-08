---
title: Message LVM_GETBKIMAGE (commctrl. h)
description: Obtient l’image d’arrière-plan dans un contrôle d’affichage de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetBkImage.
ms.assetid: db0e8f31-746a-4a16-b689-68da696e3657
keywords:
- LVM_GETBKIMAGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETBKIMAGE
- LVM_GETBKIMAGEA
- LVM_GETBKIMAGEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29e178bae10b9bed880213ca4a4ab2a1b4e07239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739957"
---
# <a name="lvm_getbkimage-message"></a><span data-ttu-id="389d5-105">\_Message GETBKIMAGE LVM</span><span class="sxs-lookup"><span data-stu-id="389d5-105">LVM\_GETBKIMAGE message</span></span>

<span data-ttu-id="389d5-106">Obtient l’image d’arrière-plan dans un contrôle d’affichage de liste.</span><span class="sxs-lookup"><span data-stu-id="389d5-106">Gets the background image in a list-view control.</span></span> <span data-ttu-id="389d5-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetBkImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkimage) .</span><span class="sxs-lookup"><span data-stu-id="389d5-107">You can send this message explicitly or by using the [**ListView\_GetBkImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="389d5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="389d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="389d5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="389d5-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="389d5-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="389d5-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="389d5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="389d5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="389d5-112">Pointeur vers une structure [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) qui recevra les informations sur l’image d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="389d5-112">A pointer to an [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) structure that will receive the background image information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="389d5-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="389d5-113">Return value</span></span>

<span data-ttu-id="389d5-114">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="389d5-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="389d5-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="389d5-115">Requirements</span></span>



| <span data-ttu-id="389d5-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="389d5-116">Requirement</span></span> | <span data-ttu-id="389d5-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="389d5-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="389d5-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="389d5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="389d5-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="389d5-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="389d5-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="389d5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="389d5-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="389d5-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="389d5-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="389d5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="389d5-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="389d5-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="389d5-124">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="389d5-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="389d5-125">**LVM \_ GETBKIMAGEW** (Unicode) et **LVM \_ GETBKIMAGEA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="389d5-125">**LVM\_GETBKIMAGEW** (Unicode) and **LVM\_GETBKIMAGEA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="389d5-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="389d5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="389d5-127">**\_SETBKIMAGE LVM**</span><span class="sxs-lookup"><span data-stu-id="389d5-127">**LVM\_SETBKIMAGE**</span></span>](lvm-setbkimage.md)
</dt> </dl>

 

 





