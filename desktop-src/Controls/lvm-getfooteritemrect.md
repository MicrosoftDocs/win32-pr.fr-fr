---
title: Message LVM_GETFOOTERITEMRECT (commctrl. h)
description: Obtient les coordonnées d’un pied de page pour un élément spécifié dans un contrôle de vue liste. Envoyez ce message explicitement ou à l’aide de la \_ macro ListView GetFooterItemRect.
ms.assetid: 4a6055d3-1cc1-4c3d-a5f6-006617ff3bce
keywords:
- LVM_GETFOOTERITEMRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142cb92806fa1d58faa0414c10c41bd2815d5b6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200540"
---
# <a name="lvm_getfooteritemrect-message"></a><span data-ttu-id="19ac5-105">\_Message GETFOOTERITEMRECT LVM</span><span class="sxs-lookup"><span data-stu-id="19ac5-105">LVM\_GETFOOTERITEMRECT message</span></span>

<span data-ttu-id="19ac5-106">Obtient les coordonnées d’un pied de page pour un élément spécifié dans un contrôle de vue liste.</span><span class="sxs-lookup"><span data-stu-id="19ac5-106">Gets the coordinates of a footer for a specified item in a list-view control.</span></span> <span data-ttu-id="19ac5-107">Envoyez ce message explicitement ou à l’aide de la macro [**ListView \_ GetFooterItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritemrect) .</span><span class="sxs-lookup"><span data-stu-id="19ac5-107">Send this message explicitly or by using the [**ListView\_GetFooterItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="19ac5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19ac5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19ac5-109">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="19ac5-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19ac5-110">Index de l’élément dans le contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="19ac5-110">The index of the item in the list-view control.</span></span>

</dd> <dt>

<span data-ttu-id="19ac5-111">*lParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="19ac5-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="19ac5-112">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) pour recevoir les coordonnées.</span><span class="sxs-lookup"><span data-stu-id="19ac5-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive the coordinates.</span></span> <span data-ttu-id="19ac5-113">L’application appelante est chargée d’allouer cette structure.</span><span class="sxs-lookup"><span data-stu-id="19ac5-113">The calling application is responsible for allocating this structure.</span></span> <span data-ttu-id="19ac5-114">Les coordonnées reçues sont exprimées en tant que coordonnées clientes.</span><span class="sxs-lookup"><span data-stu-id="19ac5-114">The coordinates received are expressed as client coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19ac5-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="19ac5-115">Return value</span></span>

<span data-ttu-id="19ac5-116">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="19ac5-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="19ac5-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19ac5-117">Requirements</span></span>



| <span data-ttu-id="19ac5-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19ac5-118">Requirement</span></span> | <span data-ttu-id="19ac5-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="19ac5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19ac5-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19ac5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="19ac5-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19ac5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="19ac5-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19ac5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="19ac5-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19ac5-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="19ac5-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="19ac5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="19ac5-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="19ac5-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

