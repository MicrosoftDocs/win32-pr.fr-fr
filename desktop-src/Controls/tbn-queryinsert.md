---
title: TBN_QUERYINSERT le code de notification (commctrl. h)
description: Avertit la fenêtre parente de la barre d’outils qu’un bouton peut être inséré à gauche du bouton spécifié pendant que l’utilisateur personnalise une barre d’outils. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: d389fabb-16f6-43aa-a4b6-abb80723345b
keywords:
- Contrôles Windows de code de notification TBN_QUERYINSERT
topic_type:
- apiref
api_name:
- TBN_QUERYINSERT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1a21e9ade8f54ffe27ebffdfc2a8b535b4b3630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942761"
---
# <a name="tbn_queryinsert-notification-code"></a><span data-ttu-id="03ac0-105">\_Code de notification TBN QUERYINSERT</span><span class="sxs-lookup"><span data-stu-id="03ac0-105">TBN\_QUERYINSERT notification code</span></span>

<span data-ttu-id="03ac0-106">Avertit la fenêtre parente de la barre d’outils qu’un bouton peut être inséré à gauche du bouton spécifié pendant que l’utilisateur personnalise une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="03ac0-106">Notifies the toolbar's parent window whether a button may be inserted to the left of the specified button while the user is customizing a toolbar.</span></span> <span data-ttu-id="03ac0-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="03ac0-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_QUERYINSERT 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="03ac0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03ac0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03ac0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="03ac0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03ac0-110">Pointeur vers une structure [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) .</span><span class="sxs-lookup"><span data-stu-id="03ac0-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="03ac0-111">Le membre **iItem** contient l’index de base zéro du bouton à insérer.</span><span class="sxs-lookup"><span data-stu-id="03ac0-111">The **iItem** member contains the zero-based index of the button to be inserted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03ac0-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="03ac0-112">Return value</span></span>

<span data-ttu-id="03ac0-113">Retourne **true** pour autoriser l’insertion d’un bouton devant le bouton donné, ou **false** pour empêcher l’insertion du bouton.</span><span class="sxs-lookup"><span data-stu-id="03ac0-113">Return **TRUE** to allow a button to be inserted in front of the given button, or **FALSE** to prevent the button from being inserted.</span></span>

## <a name="requirements"></a><span data-ttu-id="03ac0-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03ac0-114">Requirements</span></span>



| <span data-ttu-id="03ac0-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03ac0-115">Requirement</span></span> | <span data-ttu-id="03ac0-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="03ac0-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="03ac0-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03ac0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="03ac0-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="03ac0-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="03ac0-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03ac0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="03ac0-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="03ac0-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="03ac0-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="03ac0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="03ac0-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="03ac0-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





