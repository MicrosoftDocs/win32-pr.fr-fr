---
title: BN_PAINT le code de notification (winuser. h)
description: Envoyé lorsqu’un bouton doit être peint.
ms.assetid: 1c742272-60bb-42f1-a9b3-974e9a8540cd
keywords:
- Contrôles Windows de code de notification BN_PAINT
topic_type:
- apiref
api_name:
- BN_PAINT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f142c0c502d92933bf7bbc9cb01e3062c8bba96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032366"
---
# <a name="bn_paint-notification-code"></a><span data-ttu-id="ecdf2-104">Code de notification de peinture de l’un \_</span><span class="sxs-lookup"><span data-stu-id="ecdf2-104">BN\_PAINT notification code</span></span>

<span data-ttu-id="ecdf2-105">Envoyé lorsqu’un bouton doit être peint.</span><span class="sxs-lookup"><span data-stu-id="ecdf2-105">Sent when a button should be painted.</span></span>

> [!Note]  
> <span data-ttu-id="ecdf2-106">Ce code de notification est fourni uniquement pour la compatibilité avec les versions 16 bits de Windows antérieures à la version 3,0.</span><span class="sxs-lookup"><span data-stu-id="ecdf2-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="ecdf2-107">Les applications doivent utiliser le style de bouton [**BS \_ OwnerDraw**](button-styles.md) et la structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) pour cette tâche.</span><span class="sxs-lookup"><span data-stu-id="ecdf2-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="ecdf2-108">La fenêtre parente du bouton reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="ecdf2-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_PAINT

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ecdf2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ecdf2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecdf2-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ecdf2-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ecdf2-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de contrôle du bouton.</span><span class="sxs-lookup"><span data-stu-id="ecdf2-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="ecdf2-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="ecdf2-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="ecdf2-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ecdf2-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ecdf2-114">Handle du bouton.</span><span class="sxs-lookup"><span data-stu-id="ecdf2-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ecdf2-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ecdf2-115">Requirements</span></span>



| <span data-ttu-id="ecdf2-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ecdf2-116">Requirement</span></span> | <span data-ttu-id="ecdf2-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ecdf2-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecdf2-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecdf2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ecdf2-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ecdf2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ecdf2-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecdf2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ecdf2-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ecdf2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ecdf2-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="ecdf2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecdf2-123"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ecdf2-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

