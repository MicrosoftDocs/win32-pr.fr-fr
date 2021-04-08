---
title: BN_DISABLE le code de notification (winuser. h)
description: Envoyé lorsqu’un bouton est désactivé.
ms.assetid: 5e2bb434-f20d-42f1-a9e9-46c4d10b8c7e
keywords:
- Contrôles Windows de code de notification BN_DISABLE
topic_type:
- apiref
api_name:
- BN_DISABLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faaba622c056366fe0c49683adc2c020a6302929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941850"
---
# <a name="bn_disable-notification-code"></a><span data-ttu-id="7766a-104">Désactivation du \_ Code de notification</span><span class="sxs-lookup"><span data-stu-id="7766a-104">BN\_DISABLE notification code</span></span>

<span data-ttu-id="7766a-105">Envoyé lorsqu’un bouton est désactivé.</span><span class="sxs-lookup"><span data-stu-id="7766a-105">Sent when a button is disabled.</span></span>

> [!Note]  
> <span data-ttu-id="7766a-106">Ce code de notification est fourni uniquement pour la compatibilité avec les versions 16 bits de Windows antérieures à la version 3,0.</span><span class="sxs-lookup"><span data-stu-id="7766a-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="7766a-107">Les applications doivent utiliser le style de bouton [**BS \_ OwnerDraw**](button-styles.md) et la structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) pour cette tâche.</span><span class="sxs-lookup"><span data-stu-id="7766a-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="7766a-108">La fenêtre parente du bouton reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="7766a-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_DISABLE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="7766a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7766a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7766a-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7766a-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7766a-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de contrôle du bouton.</span><span class="sxs-lookup"><span data-stu-id="7766a-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="7766a-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="7766a-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="7766a-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7766a-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7766a-114">Handle du bouton.</span><span class="sxs-lookup"><span data-stu-id="7766a-114">Handle to the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7766a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7766a-115">Requirements</span></span>



| <span data-ttu-id="7766a-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7766a-116">Requirement</span></span> | <span data-ttu-id="7766a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="7766a-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7766a-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7766a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7766a-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7766a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7766a-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7766a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7766a-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7766a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7766a-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="7766a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7766a-123"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7766a-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

