---
title: Message TCM_INSERTITEM (commctrl. h)
description: Insère un nouvel onglet dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl InsertItem.
ms.assetid: e547c49a-699c-4137-8680-20391d138d54
keywords:
- TCM_INSERTITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_INSERTITEM
- TCM_INSERTITEMA
- TCM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58002006944a221571e37c37d25259d0aaa74fc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106517321"
---
# <a name="tcm_insertitem-message"></a><span data-ttu-id="c2e3e-105">\_Message INSERTITEM de TCM</span><span class="sxs-lookup"><span data-stu-id="c2e3e-105">TCM\_INSERTITEM message</span></span>

<span data-ttu-id="c2e3e-106">Insère un nouvel onglet dans un contrôle onglet.</span><span class="sxs-lookup"><span data-stu-id="c2e3e-106">Inserts a new tab in a tab control.</span></span> <span data-ttu-id="c2e3e-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_insertitem) .</span><span class="sxs-lookup"><span data-stu-id="c2e3e-107">You can send this message explicitly or by using the [**TabCtrl\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_insertitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c2e3e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c2e3e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2e3e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c2e3e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2e3e-110">Index du nouvel onglet.</span><span class="sxs-lookup"><span data-stu-id="c2e3e-110">Index of the new tab.</span></span>

</dd> <dt>

<span data-ttu-id="c2e3e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c2e3e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2e3e-112">Pointeur vers une structure [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) qui spécifie les attributs de l’onglet. Les membres **dwState** et **dwStateMask** de cette structure sont ignorés par ce message.</span><span class="sxs-lookup"><span data-stu-id="c2e3e-112">Pointer to a [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure that specifies the attributes of the tab. The **dwState** and **dwStateMask** members of this structure are ignored by this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2e3e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c2e3e-113">Return value</span></span>

<span data-ttu-id="c2e3e-114">Retourne l’index du nouvel onglet en cas de réussite, ou-1 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c2e3e-114">Returns the index of the new tab if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2e3e-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2e3e-115">Requirements</span></span>



| <span data-ttu-id="c2e3e-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2e3e-116">Requirement</span></span> | <span data-ttu-id="c2e3e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2e3e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2e3e-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2e3e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c2e3e-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2e3e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c2e3e-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2e3e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c2e3e-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2e3e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c2e3e-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="c2e3e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2e3e-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2e3e-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="c2e3e-124">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="c2e3e-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c2e3e-125">**TCM \_ INSERTITEMW** (Unicode) et **TCM \_ INSERTITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c2e3e-125">**TCM\_INSERTITEMW** (Unicode) and **TCM\_INSERTITEMA** (ANSI)</span></span><br/>             |



 

 





