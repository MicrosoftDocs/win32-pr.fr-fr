---
title: BN_HILITE le code de notification (winuser. h)
description: Envoyé lorsque l’utilisateur sélectionne un bouton.
ms.assetid: f20ba77e-257c-44ec-a2dd-dbf23cd78d07
keywords:
- Contrôles Windows de code de notification BN_HILITE
topic_type:
- apiref
api_name:
- BN_HILITE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5567837c9883c52d99f0ca68d450f7b3538f233b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941849"
---
# <a name="bn_hilite-notification-code"></a><span data-ttu-id="27383-104">\_Code de notification HILITEy</span><span class="sxs-lookup"><span data-stu-id="27383-104">BN\_HILITE notification code</span></span>

<span data-ttu-id="27383-105">Envoyé lorsque l’utilisateur sélectionne un bouton.</span><span class="sxs-lookup"><span data-stu-id="27383-105">Sent when the user selects a button.</span></span>

> [!Note]  
> <span data-ttu-id="27383-106">Ce code de notification est fourni uniquement pour la compatibilité avec les versions 16 bits de Windows antérieures à la version 3,0.</span><span class="sxs-lookup"><span data-stu-id="27383-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="27383-107">Les applications doivent utiliser le style de bouton [**BS \_ OwnerDraw**](button-styles.md) et la structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) pour cette tâche.</span><span class="sxs-lookup"><span data-stu-id="27383-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="27383-108">La fenêtre parente du bouton reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="27383-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_HILITE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="27383-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="27383-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27383-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="27383-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27383-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de contrôle du bouton.</span><span class="sxs-lookup"><span data-stu-id="27383-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="27383-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="27383-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="27383-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="27383-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27383-114">Handle du bouton.</span><span class="sxs-lookup"><span data-stu-id="27383-114">Handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="27383-115">Notes</span><span class="sxs-lookup"><span data-stu-id="27383-115">Remarks</span></span>

<span data-ttu-id="27383-116">L' \_ HiLite de l’erreur est le même que le code de notification [ \_ Push](bn-pushed.md) de la fonction.</span><span class="sxs-lookup"><span data-stu-id="27383-116">BN\_HILITE is the same as the [BN\_PUSHED](bn-pushed.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="27383-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="27383-117">Requirements</span></span>



| <span data-ttu-id="27383-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="27383-118">Requirement</span></span> | <span data-ttu-id="27383-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="27383-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27383-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27383-120">Minimum supported client</span></span><br/> | <span data-ttu-id="27383-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="27383-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="27383-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27383-122">Minimum supported server</span></span><br/> | <span data-ttu-id="27383-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="27383-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="27383-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="27383-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="27383-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="27383-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

