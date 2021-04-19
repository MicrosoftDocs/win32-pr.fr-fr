---
title: Message CBEM_INSERTITEM (commctrl. h)
description: Insère un nouvel élément dans un contrôle ComboBoxEx.
ms.assetid: c99db676-204d-44c9-aaa3-81b70fe2cf44
keywords:
- CBEM_INSERTITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- CBEM_INSERTITEM
- CBEM_INSERTITEMA
- CBEM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23e6cb26a575472e53703d65e407a94a024dcfac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106516297"
---
# <a name="cbem_insertitem-message"></a><span data-ttu-id="39a66-104">\_Message CBEM INSERTITEM</span><span class="sxs-lookup"><span data-stu-id="39a66-104">CBEM\_INSERTITEM message</span></span>

<span data-ttu-id="39a66-105">Insère un nouvel élément dans un contrôle ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="39a66-105">Inserts a new item in a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="39a66-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39a66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39a66-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="39a66-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="39a66-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="39a66-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="39a66-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39a66-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39a66-110">Pointeur vers une structure [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) qui contient des informations sur l’élément à insérer.</span><span class="sxs-lookup"><span data-stu-id="39a66-110">A pointer to a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure that contains information about the item to be inserted.</span></span> <span data-ttu-id="39a66-111">Lorsque le message est envoyé, le membre **iItem** doit être défini pour indiquer l’index de base zéro au niveau duquel insérer l’élément.</span><span class="sxs-lookup"><span data-stu-id="39a66-111">When the message is sent, the **iItem** member must be set to indicate the zero-based index at which to insert the item.</span></span> <span data-ttu-id="39a66-112">Pour insérer un élément à la fin de la liste, affectez la valeur-1 au membre **iItem** .</span><span class="sxs-lookup"><span data-stu-id="39a66-112">To insert an item at the end of the list, set the **iItem** member to -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39a66-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="39a66-113">Return value</span></span>

<span data-ttu-id="39a66-114">Retourne l’index auquel le nouvel élément a été inséré en cas de réussite, ou-1 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="39a66-114">Returns the index at which the new item was inserted if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="39a66-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39a66-115">Requirements</span></span>



| <span data-ttu-id="39a66-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39a66-116">Requirement</span></span> | <span data-ttu-id="39a66-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="39a66-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39a66-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39a66-118">Minimum supported client</span></span><br/> | <span data-ttu-id="39a66-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39a66-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="39a66-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39a66-120">Minimum supported server</span></span><br/> | <span data-ttu-id="39a66-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39a66-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="39a66-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="39a66-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="39a66-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="39a66-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="39a66-124">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="39a66-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="39a66-125">**CBEM \_ INSERTITEMW** (Unicode) et **CBEM \_ INSERTITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="39a66-125">**CBEM\_INSERTITEMW** (Unicode) and **CBEM\_INSERTITEMA** (ANSI)</span></span><br/>           |



 

 





