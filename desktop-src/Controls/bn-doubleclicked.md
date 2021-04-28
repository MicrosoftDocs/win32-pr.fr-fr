---
title: BN_DOUBLECLICKED le code de notification (winuser. h)
description: Code de notification BN_DOUBLECLICKED-envoyé lorsque l’utilisateur double-clique sur un bouton.
ms.assetid: 2fd7363a-5a02-453c-bfab-df5cbf8e42a5
keywords:
- Contrôles Windows de code de notification BN_DOUBLECLICKED
topic_type:
- apiref
api_name:
- BN_DOUBLECLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64a11a4dec91a7a2f1d200c4c86c6989d846604a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104187"
---
# <a name="bn_doubleclicked-notification-code"></a><span data-ttu-id="4e835-104">Code de notification de la \_</span><span class="sxs-lookup"><span data-stu-id="4e835-104">BN\_DOUBLECLICKED notification code</span></span>

<span data-ttu-id="4e835-105">Envoyé lorsque l’utilisateur double-clique sur un bouton.</span><span class="sxs-lookup"><span data-stu-id="4e835-105">Sent when the user double-clicks a button.</span></span> <span data-ttu-id="4e835-106">Ce code de notification est envoyé automatiquement pour les boutons [**BS \_ UserButton**](button-styles.md), [**BS \_ RadioButton**](button-styles.md)et [**BS \_ OwnerDraw**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="4e835-106">This notification code is sent automatically for [**BS\_USERBUTTON**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), and [**BS\_OWNERDRAW**](button-styles.md) buttons.</span></span> <span data-ttu-id="4e835-107">Les autres types de boutons envoient un type d' \_ utilisateur avec le style de [**\_ notification BS**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="4e835-107">Other button types send BN\_DOUBLECLICKED only if they have the [**BS\_NOTIFY**](button-styles.md) style.</span></span>

<span data-ttu-id="4e835-108">La fenêtre parente du bouton reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="4e835-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_DOUBLECLICKED

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="4e835-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e835-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e835-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4e835-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4e835-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de contrôle du bouton.</span><span class="sxs-lookup"><span data-stu-id="4e835-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="4e835-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="4e835-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="4e835-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4e835-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4e835-114">Handle du bouton.</span><span class="sxs-lookup"><span data-stu-id="4e835-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e835-115">Notes </span><span class="sxs-lookup"><span data-stu-id="4e835-115">Remarks</span></span>

<span data-ttu-id="4e835-116">L’erreur de l’un des fautes \_ est le même que le code de notification [ \_ DBLCLK](bn-dblclk.md) .</span><span class="sxs-lookup"><span data-stu-id="4e835-116">BN\_DOUBLECLICKED is the same as the [BN\_DBLCLK](bn-dblclk.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e835-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e835-117">Requirements</span></span>



| <span data-ttu-id="4e835-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e835-118">Requirement</span></span> | <span data-ttu-id="4e835-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e835-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e835-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e835-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4e835-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e835-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4e835-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e835-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4e835-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e835-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4e835-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="4e835-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e835-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e835-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

