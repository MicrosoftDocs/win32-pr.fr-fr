---
title: Message HDM_GETITEM (commctrl. h)
description: Obtient des informations sur un élément dans un contrôle header. Vous pouvez envoyer ce message explicitement ou utiliser la macro Header \_ GetItem.
ms.assetid: fb1330d3-fd28-490c-9caa-4b2b5ff86ba0
keywords:
- HDM_GETITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_GETITEM
- HDM_GETITEMA
- HDM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2073602121480930e0f7d9d2e5a904c0dea77ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103777"
---
# <a name="hdm_getitem-message"></a><span data-ttu-id="ce71d-105">\_Message HDM GETITEM</span><span class="sxs-lookup"><span data-stu-id="ce71d-105">HDM\_GETITEM message</span></span>

<span data-ttu-id="ce71d-106">Obtient des informations sur un élément dans un contrôle header.</span><span class="sxs-lookup"><span data-stu-id="ce71d-106">Gets information about an item in a header control.</span></span> <span data-ttu-id="ce71d-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro [**header \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitem) .</span><span class="sxs-lookup"><span data-stu-id="ce71d-107">You can send this message explicitly or use the [**Header\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ce71d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce71d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce71d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ce71d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce71d-110">Index de l’élément pour lequel les informations doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="ce71d-110">The index of the item for which information is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="ce71d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce71d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce71d-112">Pointeur vers une structure [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) .</span><span class="sxs-lookup"><span data-stu-id="ce71d-112">A pointer to an [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure.</span></span> <span data-ttu-id="ce71d-113">Lorsque le message est envoyé, le membre **Mask** indique le type d’informations demandées.</span><span class="sxs-lookup"><span data-stu-id="ce71d-113">When the message is sent, the **mask** member indicates the type of information being requested.</span></span> <span data-ttu-id="ce71d-114">Lorsque le message est renvoyé, les autres membres reçoivent les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="ce71d-114">When the message returns, the other members receive the requested information.</span></span> <span data-ttu-id="ce71d-115">Si le membre de **masque** spécifie zéro, le message retourne la **valeur true** , mais aucune information n’est copiée dans la structure.</span><span class="sxs-lookup"><span data-stu-id="ce71d-115">If the **mask** member specifies zero, the message returns **TRUE** but copies no information to the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce71d-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ce71d-116">Return value</span></span>

<span data-ttu-id="ce71d-117">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ce71d-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce71d-118">Notes</span><span class="sxs-lookup"><span data-stu-id="ce71d-118">Remarks</span></span>

<span data-ttu-id="ce71d-119">Si l' \_ indicateur de texte hdi est défini dans le membre **Mask** de la structure [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) , le contrôle peut modifier le membre **pszText** de la structure afin qu’il pointe vers le nouveau texte au lieu de remplir la mémoire tampon avec le texte demandé.</span><span class="sxs-lookup"><span data-stu-id="ce71d-119">If the HDI\_TEXT flag is set in the **mask** member of the [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure, the control may change the **pszText** member of the structure to point to the new text instead of filling the buffer with the requested text.</span></span> <span data-ttu-id="ce71d-120">Les applications ne doivent pas supposer que le texte sera toujours placé dans la mémoire tampon demandée.</span><span class="sxs-lookup"><span data-stu-id="ce71d-120">Applications should not assume that the text will always be placed in the requested buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce71d-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce71d-121">Requirements</span></span>



| <span data-ttu-id="ce71d-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce71d-122">Requirement</span></span> | <span data-ttu-id="ce71d-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce71d-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce71d-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce71d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ce71d-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce71d-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ce71d-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce71d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ce71d-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce71d-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ce71d-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce71d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce71d-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce71d-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ce71d-130">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="ce71d-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ce71d-131">**HDM \_ GETITEMW** (Unicode) et **HDM \_ GETITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ce71d-131">**HDM\_GETITEMW** (Unicode) and **HDM\_GETITEMA** (ANSI)</span></span><br/>                   |



 

 





