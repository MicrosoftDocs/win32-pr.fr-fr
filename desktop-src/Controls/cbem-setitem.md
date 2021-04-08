---
title: Message CBEM_SETITEM (commctrl. h)
description: Définit les attributs d’un élément dans un contrôle ComboBoxEx.
ms.assetid: 752df8ea-fd5e-47fa-b729-d019bdde0904
keywords:
- CBEM_SETITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- CBEM_SETITEM
- CBEM_SETITEMA
- CBEM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50ae19287e3e30810b1d8c558be9b6153a86ab6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743397"
---
# <a name="cbem_setitem-message"></a><span data-ttu-id="25b1a-104">\_Message CBEM SETITEM</span><span class="sxs-lookup"><span data-stu-id="25b1a-104">CBEM\_SETITEM message</span></span>

<span data-ttu-id="25b1a-105">Définit les attributs d’un élément dans un contrôle ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="25b1a-105">Sets the attributes for an item in a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="25b1a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25b1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25b1a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="25b1a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="25b1a-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="25b1a-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="25b1a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="25b1a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25b1a-110">Pointeur vers une structure [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) qui contient les informations d’élément à définir.</span><span class="sxs-lookup"><span data-stu-id="25b1a-110">A pointer to a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure that contains the item information to be set.</span></span> <span data-ttu-id="25b1a-111">Lorsque le message est envoyé, le membre de **masque** de la structure doit être défini pour indiquer les attributs qui sont valides et le membre **iItem** doit spécifier l’index de base zéro de l’élément à modifier.</span><span class="sxs-lookup"><span data-stu-id="25b1a-111">When the message is sent, the **mask** member of the structure must be set to indicate which attributes are valid and the **iItem** member must specify the zero-based index of the item to be modified.</span></span> <span data-ttu-id="25b1a-112">L’affectation de la valeur-1 au membre **iItem** modifie l’élément affiché dans le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="25b1a-112">Setting the **iItem** member to -1 will modify the item displayed in the edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25b1a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="25b1a-113">Return value</span></span>

<span data-ttu-id="25b1a-114">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="25b1a-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="25b1a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25b1a-115">Requirements</span></span>



| <span data-ttu-id="25b1a-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25b1a-116">Requirement</span></span> | <span data-ttu-id="25b1a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="25b1a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25b1a-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25b1a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="25b1a-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25b1a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="25b1a-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25b1a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="25b1a-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25b1a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="25b1a-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="25b1a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="25b1a-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="25b1a-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="25b1a-124">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="25b1a-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="25b1a-125">**CBEM \_ SETITEMW** (Unicode) et **CBEM \_ SETITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="25b1a-125">**CBEM\_SETITEMW** (Unicode) and **CBEM\_SETITEMA** (ANSI)</span></span><br/>                 |



 

 





