---
title: Message TCM_GETITEM (commctrl. h)
description: Récupère des informations sur un onglet dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl GetItem.
ms.assetid: 41774f14-c4e9-4c98-bc25-3522b2125ed5
keywords:
- TCM_GETITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_GETITEM
- TCM_GETITEMA
- TCM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f94f26a0893416847df052ff47731391a86f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509353"
---
# <a name="tcm_getitem-message"></a><span data-ttu-id="91a13-105">\_Message TCM GETITEM</span><span class="sxs-lookup"><span data-stu-id="91a13-105">TCM\_GETITEM message</span></span>

<span data-ttu-id="91a13-106">Récupère des informations sur un onglet dans un contrôle onglet.</span><span class="sxs-lookup"><span data-stu-id="91a13-106">Retrieves information about a tab in a tab control.</span></span> <span data-ttu-id="91a13-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitem) .</span><span class="sxs-lookup"><span data-stu-id="91a13-107">You can send this message explicitly or by using the [**TabCtrl\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="91a13-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91a13-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91a13-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="91a13-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91a13-110">Index de l’onglet.</span><span class="sxs-lookup"><span data-stu-id="91a13-110">Index of the tab.</span></span>

</dd> <dt>

<span data-ttu-id="91a13-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="91a13-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91a13-112">Pointeur vers une structure [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) qui spécifie les informations à récupérer et à recevoir des informations à propos de l’onglet. Lorsque le message est envoyé, le membre **Mask** spécifie les attributs à retourner.</span><span class="sxs-lookup"><span data-stu-id="91a13-112">Pointer to a [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure that specifies the information to retrieve and receives information about the tab. When the message is sent, the **mask** member specifies which attributes to return.</span></span> <span data-ttu-id="91a13-113">Si le membre de **masque** spécifie la \_ valeur de texte TCIF, le membre **pszText** doit contenir l’adresse de la mémoire tampon qui reçoit le texte de l’élément, et le membre **cchTextMax** doit spécifier la taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="91a13-113">If the **mask** member specifies the TCIF\_TEXT value, the **pszText** member must contain the address of the buffer that receives the item text, and the **cchTextMax** member must specify the size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91a13-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="91a13-114">Return value</span></span>

<span data-ttu-id="91a13-115">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="91a13-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="91a13-116">Notes</span><span class="sxs-lookup"><span data-stu-id="91a13-116">Remarks</span></span>

<span data-ttu-id="91a13-117">Si l' \_ indicateur de texte TCIF est défini dans le membre **Mask** de la structure [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) , le contrôle peut modifier le membre **pszText** de la structure afin qu’il pointe vers le nouveau texte au lieu de remplir la mémoire tampon avec le texte demandé.</span><span class="sxs-lookup"><span data-stu-id="91a13-117">If the TCIF\_TEXT flag is set in the **mask** member of the [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure, the control may change the **pszText** member of the structure to point to the new text instead of filling the buffer with the requested text.</span></span> <span data-ttu-id="91a13-118">Le contrôle peut affecter la **valeur null** au membre **pszText** pour indiquer qu’aucun texte n’est associé à l’élément.</span><span class="sxs-lookup"><span data-stu-id="91a13-118">The control may set the **pszText** member to **NULL** to indicate that no text is associated with the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="91a13-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91a13-119">Requirements</span></span>



| <span data-ttu-id="91a13-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91a13-120">Requirement</span></span> | <span data-ttu-id="91a13-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="91a13-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91a13-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91a13-122">Minimum supported client</span></span><br/> | <span data-ttu-id="91a13-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91a13-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="91a13-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91a13-124">Minimum supported server</span></span><br/> | <span data-ttu-id="91a13-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91a13-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="91a13-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="91a13-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="91a13-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="91a13-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="91a13-128">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="91a13-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="91a13-129">**TCM \_ GETITEMW** (Unicode) et **TCM \_ GETITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="91a13-129">**TCM\_GETITEMW** (Unicode) and **TCM\_GETITEMA** (ANSI)</span></span><br/>                   |



 

 





