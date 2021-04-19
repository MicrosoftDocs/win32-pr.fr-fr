---
title: Message CBEM_GETITEM (commctrl. h)
description: Obtient des informations sur les éléments d’un élément ComboBoxEx donné.
ms.assetid: 2df07ae8-fa84-487c-a4a7-90244dfdb40e
keywords:
- CBEM_GETITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- CBEM_GETITEM
- CBEM_GETITEMA
- CBEM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 940bbf7aea8ec93dd0f808937d959477c964df96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509551"
---
# <a name="cbem_getitem-message"></a><span data-ttu-id="e9636-104">\_Message CBEM GETITEM</span><span class="sxs-lookup"><span data-stu-id="e9636-104">CBEM\_GETITEM message</span></span>

<span data-ttu-id="e9636-105">Obtient des informations sur les éléments d’un élément ComboBoxEx donné.</span><span class="sxs-lookup"><span data-stu-id="e9636-105">Gets item information for a given ComboBoxEx item.</span></span>

## <a name="parameters"></a><span data-ttu-id="e9636-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9636-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9636-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e9636-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e9636-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="e9636-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e9636-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e9636-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9636-110">Pointeur vers une structure [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) qui reçoit les informations de l’élément.</span><span class="sxs-lookup"><span data-stu-id="e9636-110">A pointer to a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure that receives the item information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9636-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e9636-111">Return value</span></span>

<span data-ttu-id="e9636-112">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e9636-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9636-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e9636-113">Remarks</span></span>

<span data-ttu-id="e9636-114">Lorsque le message est envoyé, les membres **iItem** et **Mask** de la structure doivent être définis pour indiquer l’index de l’élément cible et le type d’informations à récupérer.</span><span class="sxs-lookup"><span data-stu-id="e9636-114">When the message is sent, the **iItem** and **mask** members of the structure must be set to indicate the index of the target item and the type of information to be retrieved.</span></span> <span data-ttu-id="e9636-115">D’autres membres sont définis en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="e9636-115">Other members are set as needed.</span></span> <span data-ttu-id="e9636-116">Par exemple, pour récupérer du texte, vous devez définir l' \_ indicateur de texte CBEIF dans le **masque** et assigner une valeur à **cchTextMax**.</span><span class="sxs-lookup"><span data-stu-id="e9636-116">For example, to retrieve text, you must set the CBEIF\_TEXT flag in **mask**, and assign a value to **cchTextMax**.</span></span> <span data-ttu-id="e9636-117">La définition du membre **iItem** sur-1 permet de récupérer l’élément affiché dans le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="e9636-117">Setting the **iItem** member to -1 will retrieve the item displayed in the edit control.</span></span>

<span data-ttu-id="e9636-118">Si l' \_ indicateur de texte CBEIF est défini dans le membre **Mask** de la structure [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) , le contrôle peut modifier le membre **pszText** de la structure afin qu’il pointe vers le nouveau texte au lieu de remplir la mémoire tampon avec le texte demandé.</span><span class="sxs-lookup"><span data-stu-id="e9636-118">If the CBEIF\_TEXT flag is set in the **mask** member of the [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure, the control may change the **pszText** member of the structure to point to the new text instead of filling the buffer with the requested text.</span></span> <span data-ttu-id="e9636-119">Les applications ne doivent pas supposer que le texte sera toujours placé dans la mémoire tampon demandée.</span><span class="sxs-lookup"><span data-stu-id="e9636-119">Applications should not assume that the text will always be placed in the requested buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9636-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9636-120">Requirements</span></span>



| <span data-ttu-id="e9636-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9636-121">Requirement</span></span> | <span data-ttu-id="e9636-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9636-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e9636-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9636-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e9636-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9636-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e9636-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9636-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e9636-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9636-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e9636-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9636-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9636-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9636-128"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="e9636-129">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="e9636-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e9636-130">**CBEM \_ GETITEMW** (Unicode) et **CBEM \_ GETITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e9636-130">**CBEM\_GETITEMW** (Unicode) and **CBEM\_GETITEMA** (ANSI)</span></span><br/>                 |



 

 





