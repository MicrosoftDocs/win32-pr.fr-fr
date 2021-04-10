---
title: BN_UNHILITE le code de notification (winuser. h)
description: Envoyé lorsque la sélection doit être supprimée d’un bouton.
ms.assetid: 9839a55b-9e9c-4c9c-8e92-347007ea27be
keywords:
- Contrôles Windows de code de notification BN_UNHILITE
topic_type:
- apiref
api_name:
- BN_UNHILITE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 395901548103a7a678b4873e1fde52e259297ebb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941799"
---
# <a name="bn_unhilite-notification-code"></a><span data-ttu-id="8722f-104">\_Code de notification UNHILITEy</span><span class="sxs-lookup"><span data-stu-id="8722f-104">BN\_UNHILITE notification code</span></span>

<span data-ttu-id="8722f-105">Envoyé lorsque la sélection doit être supprimée d’un bouton.</span><span class="sxs-lookup"><span data-stu-id="8722f-105">Sent when the highlight should be removed from a button.</span></span>

> [!Note]  
> <span data-ttu-id="8722f-106">Ce code de notification est fourni uniquement pour la compatibilité avec les versions 16 bits de Windows antérieures à la version 3,0.</span><span class="sxs-lookup"><span data-stu-id="8722f-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="8722f-107">Les applications doivent utiliser le style de bouton [**BS \_ OwnerDraw**](button-styles.md) et la structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) pour cette tâche.</span><span class="sxs-lookup"><span data-stu-id="8722f-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="8722f-108">La fenêtre parente du bouton reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="8722f-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_UNHILITE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="8722f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8722f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8722f-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8722f-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8722f-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de contrôle du bouton.</span><span class="sxs-lookup"><span data-stu-id="8722f-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="8722f-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="8722f-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="8722f-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8722f-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8722f-114">Handle du bouton.</span><span class="sxs-lookup"><span data-stu-id="8722f-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8722f-115">Notes</span><span class="sxs-lookup"><span data-stu-id="8722f-115">Remarks</span></span>

<span data-ttu-id="8722f-116">L' \_ UNHILITE de la cale est le même que le code de notification de la fonction de [ \_ Push](bn-unpushed.md) .</span><span class="sxs-lookup"><span data-stu-id="8722f-116">BN\_UNHILITE is the same as the [BN\_UNPUSHED](bn-unpushed.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8722f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8722f-117">Requirements</span></span>



| <span data-ttu-id="8722f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8722f-118">Requirement</span></span> | <span data-ttu-id="8722f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="8722f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8722f-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8722f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8722f-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8722f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8722f-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8722f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8722f-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8722f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8722f-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="8722f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8722f-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8722f-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

