---
title: Message RB_INSERTBAND (commctrl. h)
description: Insère une nouvelle bande dans un contrôle rebar.
ms.assetid: ac621f65-b8ab-41d6-928d-a48fbea572e7
keywords:
- RB_INSERTBAND les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_INSERTBAND
- RB_INSERTBANDA
- RB_INSERTBANDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39b45eb662fb4c2058b87837352339c84762188
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844457"
---
# <a name="rb_insertband-message"></a><span data-ttu-id="49a96-104">\_Message INSERTBAND RB</span><span class="sxs-lookup"><span data-stu-id="49a96-104">RB\_INSERTBAND message</span></span>

<span data-ttu-id="49a96-105">Insère une nouvelle bande dans un contrôle rebar.</span><span class="sxs-lookup"><span data-stu-id="49a96-105">Inserts a new band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="49a96-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49a96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49a96-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="49a96-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49a96-108">Index de base zéro de l’emplacement où la bande sera insérée.</span><span class="sxs-lookup"><span data-stu-id="49a96-108">Zero-based index of the location where the band will be inserted.</span></span> <span data-ttu-id="49a96-109">Si vous affectez la valeur-1 à ce paramètre, le contrôle ajoutera la nouvelle bande au dernier emplacement.</span><span class="sxs-lookup"><span data-stu-id="49a96-109">If you set this parameter to -1, the control will add the new band at the last location.</span></span>

</dd> <dt>

<span data-ttu-id="49a96-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49a96-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49a96-111">Pointeur vers une structure [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) qui définit la bande à insérer.</span><span class="sxs-lookup"><span data-stu-id="49a96-111">Pointer to a [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure that defines the band to be inserted.</span></span> <span data-ttu-id="49a96-112">Vous devez définir le membre **cbSize** de cette structure sur **sizeof**(REBARBANDINFO) avant d’envoyer ce message.</span><span class="sxs-lookup"><span data-stu-id="49a96-112">You must set the **cbSize** member of this structure to **sizeof**(REBARBANDINFO) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49a96-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="49a96-113">Return value</span></span>

<span data-ttu-id="49a96-114">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="49a96-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="49a96-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49a96-115">Requirements</span></span>



| <span data-ttu-id="49a96-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49a96-116">Requirement</span></span> | <span data-ttu-id="49a96-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="49a96-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49a96-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49a96-118">Minimum supported client</span></span><br/> | <span data-ttu-id="49a96-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49a96-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="49a96-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49a96-120">Minimum supported server</span></span><br/> | <span data-ttu-id="49a96-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49a96-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="49a96-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="49a96-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="49a96-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="49a96-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="49a96-124">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="49a96-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="49a96-125">**RB \_ INSERTBANDW** (Unicode) et **RB \_ INSERTBANDA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="49a96-125">**RB\_INSERTBANDW** (Unicode) and **RB\_INSERTBANDA** (ANSI)</span></span><br/>               |



 

 





