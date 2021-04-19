---
description: Avertit une application lorsque l’IME sélectionné a besoin d’informations sur les coordonnées d’un caractère dans la chaîne de composition. L’application reçoit cette commande via le \_ \_ message de demande de l’IME WM avec les paramètres de paramètre, comme indiqué ci-dessous.
ms.assetid: cae7e5b3-8aaf-452d-80df-fb0ae04a342c
title: IMR_QUERYCHARPOSITION le code de notification (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 947eec9b3dd1f678d9266bb795214cf392629193
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106525048"
---
# <a name="imr_querycharposition-notification-code"></a><span data-ttu-id="3489d-104">\_Code de notification IMR QUERYCHARPOSITION</span><span class="sxs-lookup"><span data-stu-id="3489d-104">IMR\_QUERYCHARPOSITION notification code</span></span>

<span data-ttu-id="3489d-105">Avertit une application lorsque l’IME sélectionné a besoin d’informations sur les coordonnées d’un caractère dans la chaîne de composition.</span><span class="sxs-lookup"><span data-stu-id="3489d-105">Notifies an application when the selected IME needs information about the coordinates of a character in the composition string.</span></span> <span data-ttu-id="3489d-106">L’application reçoit cette commande via le message de [**\_ \_ demande de l’IME WM**](wm-ime-request.md) avec les paramètres de paramètre, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="3489d-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMR_QUERYCHARPOSITION
```



## <a name="parameters"></a><span data-ttu-id="3489d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3489d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3489d-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="3489d-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="3489d-109">Définissez sur IMR \_ QUERYCHARPOSITION.</span><span class="sxs-lookup"><span data-stu-id="3489d-109">Set to IMR\_QUERYCHARPOSITION.</span></span>

</dd> <dt>

<span data-ttu-id="3489d-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="3489d-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="3489d-111">Pointeur vers une structure [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) qui contient la position du caractère dans la fenêtre de composition.</span><span class="sxs-lookup"><span data-stu-id="3489d-111">Pointer to an [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) structure that contains the position of the character in the composition window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3489d-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3489d-112">Return Value</span></span>

<span data-ttu-id="3489d-113">Retourne une valeur différente de zéro si l’application remplit la structure [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) .</span><span class="sxs-lookup"><span data-stu-id="3489d-113">Returns a nonzero value if the application fills the [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) structure.</span></span> <span data-ttu-id="3489d-114">Dans le cas contraire, la commande retourne 0.</span><span class="sxs-lookup"><span data-stu-id="3489d-114">Otherwise, the command returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="3489d-115">Notes</span><span class="sxs-lookup"><span data-stu-id="3489d-115">Remarks</span></span>

<span data-ttu-id="3489d-116">Une application qui dessine la chaîne de composition elle-même, au lieu de s’appuyer sur l’IME, est responsable du remplissage de tous les membres de la structure [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) .</span><span class="sxs-lookup"><span data-stu-id="3489d-116">An application that draws the composition string itself, instead of relying on the IME, is responsible for filling in all the members of the [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) structure.</span></span> <span data-ttu-id="3489d-117">Dans le cas contraire, l’application doit passer la commande à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ou [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea) si elle possède sa propre fenêtre d’interface utilisateur IME.</span><span class="sxs-lookup"><span data-stu-id="3489d-117">Otherwise, the application should pass the command to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) or [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea) if it has its own IME user interface window.</span></span>

## <a name="requirements"></a><span data-ttu-id="3489d-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3489d-118">Requirements</span></span>



| <span data-ttu-id="3489d-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3489d-119">Requirement</span></span> | <span data-ttu-id="3489d-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="3489d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3489d-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3489d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3489d-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3489d-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3489d-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3489d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3489d-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3489d-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3489d-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="3489d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3489d-126"><dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3489d-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3489d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3489d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3489d-128">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="3489d-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="3489d-129">Commandes du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="3489d-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="3489d-130">**IMECHARPOSITION**</span><span class="sxs-lookup"><span data-stu-id="3489d-130">**IMECHARPOSITION**</span></span>](/windows/win32/api/imm/ns-imm-imecharposition)
</dt> <dt>

[<span data-ttu-id="3489d-131">**ImmIsUIMessage**</span><span class="sxs-lookup"><span data-stu-id="3489d-131">**ImmIsUIMessage**</span></span>](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> <dt>

[<span data-ttu-id="3489d-132">**demande de l' \_ IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="3489d-132">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> </dl>

 

 
