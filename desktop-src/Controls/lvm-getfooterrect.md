---
title: Message LVM_GETFOOTERRECT (commctrl. h)
description: Récupère les coordonnées du pied de page pour un contrôle d’affichage de liste. Envoyez ce message explicitement ou à l’aide de la \_ macro ListView GetFooterRect.
ms.assetid: f8816f35-c1d2-4072-81d3-0a9a3df53d64
keywords:
- LVM_GETFOOTERRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETFOOTERRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31df3a1b7b29e5ad9191da9e990e04daec99e948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102893"
---
# <a name="lvm_getfooterrect-message"></a><span data-ttu-id="2f6eb-105">\_Message GETFOOTERRECT LVM</span><span class="sxs-lookup"><span data-stu-id="2f6eb-105">LVM\_GETFOOTERRECT message</span></span>

<span data-ttu-id="2f6eb-106">Récupère les coordonnées du pied de page pour un contrôle d’affichage de liste.</span><span class="sxs-lookup"><span data-stu-id="2f6eb-106">Retrieves the coordinates of the footer for a list-view control.</span></span> <span data-ttu-id="2f6eb-107">Envoyez ce message explicitement ou à l’aide de la macro [**ListView \_ GetFooterRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterrect) .</span><span class="sxs-lookup"><span data-stu-id="2f6eb-107">Send this message explicitly or by using the [**ListView\_GetFooterRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2f6eb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f6eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f6eb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2f6eb-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2f6eb-110">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="2f6eb-110">Not used.</span></span> <span data-ttu-id="2f6eb-111">Doit être égal à 0.</span><span class="sxs-lookup"><span data-stu-id="2f6eb-111">Must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="2f6eb-112">*lParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2f6eb-112">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f6eb-113">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) pour recevoir les coordonnées.</span><span class="sxs-lookup"><span data-stu-id="2f6eb-113">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive the coordinates.</span></span> <span data-ttu-id="2f6eb-114">Le processus appelant est chargé d’allouer cette structure.</span><span class="sxs-lookup"><span data-stu-id="2f6eb-114">The calling process is responsible for allocating this structure.</span></span> <span data-ttu-id="2f6eb-115">Les coordonnées reçues sont exprimées en tant que coordonnées clientes.</span><span class="sxs-lookup"><span data-stu-id="2f6eb-115">The coordinates received are expressed as client coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f6eb-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2f6eb-116">Return value</span></span>

<span data-ttu-id="2f6eb-117">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="2f6eb-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f6eb-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f6eb-118">Requirements</span></span>



| <span data-ttu-id="2f6eb-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f6eb-119">Requirement</span></span> | <span data-ttu-id="2f6eb-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f6eb-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f6eb-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f6eb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2f6eb-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f6eb-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2f6eb-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f6eb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2f6eb-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f6eb-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2f6eb-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f6eb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f6eb-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f6eb-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

