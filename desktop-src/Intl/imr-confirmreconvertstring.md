---
description: Avertit une application lorsque l’IME doit modifier la structure RECONVERTSTRING. L’application reçoit cette commande via le \_ \_ message de demande de l’IME WM avec les paramètres de paramètre, comme indiqué ci-dessous.
ms.assetid: 035a7072-d292-4883-bc3e-d1e9ed64d9ec
title: IMR_CONFIRMRECONVERTSTRING le code de notification (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c500a155be14f447bb07ad506e12d5bece66e225
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756495"
---
# <a name="imr_confirmreconvertstring-notification-code"></a><span data-ttu-id="b7c80-104">\_Code de notification IMR CONFIRMRECONVERTSTRING</span><span class="sxs-lookup"><span data-stu-id="b7c80-104">IMR\_CONFIRMRECONVERTSTRING notification code</span></span>

<span data-ttu-id="b7c80-105">Avertit une application lorsque l’IME doit modifier la structure [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) .</span><span class="sxs-lookup"><span data-stu-id="b7c80-105">Notifies an application when the IME needs to change the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure.</span></span> <span data-ttu-id="b7c80-106">L’application reçoit cette commande via le message de [**\_ \_ demande de l’IME WM**](wm-ime-request.md) avec les paramètres de paramètre, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b7c80-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMR_CONFIRMRECONVERTSTRING
```



## <a name="parameters"></a><span data-ttu-id="b7c80-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7c80-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7c80-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="b7c80-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="b7c80-109">Définissez sur IMR \_ CONFIRMRECONVERTSTRING.</span><span class="sxs-lookup"><span data-stu-id="b7c80-109">Set to IMR\_CONFIRMRECONVERTSTRING.</span></span>

</dd> <dt>

<span data-ttu-id="b7c80-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="b7c80-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="b7c80-111">Pointeur vers une structure [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) à partir de l’IME.</span><span class="sxs-lookup"><span data-stu-id="b7c80-111">Pointer to a [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure from the IME.</span></span> <span data-ttu-id="b7c80-112">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="b7c80-112">For more information, see the Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7c80-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b7c80-113">Return Value</span></span>

<span data-ttu-id="b7c80-114">Retourne une valeur différente de zéro si l’application accepte la structure [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) modifiée.</span><span class="sxs-lookup"><span data-stu-id="b7c80-114">Returns a nonzero value if the application accepts the changed [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure.</span></span> <span data-ttu-id="b7c80-115">Dans le cas contraire, la commande retourne 0 et l’IME utilise la structure **RECONVERTSTRING** d’origine.</span><span class="sxs-lookup"><span data-stu-id="b7c80-115">Otherwise, the command returns 0 and the IME uses the original **RECONVERTSTRING** structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7c80-116">Notes</span><span class="sxs-lookup"><span data-stu-id="b7c80-116">Remarks</span></span>

<span data-ttu-id="b7c80-117">L’application remplit la structure [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) lors de la réception de la commande [IMR \_ RECONVERTSTRING](imr-reconvertstring.md) .</span><span class="sxs-lookup"><span data-stu-id="b7c80-117">The application fills in the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure upon receiving the [IMR\_RECONVERTSTRING](imr-reconvertstring.md) command.</span></span>

<span data-ttu-id="b7c80-118">Une fois que l’application a géré [IMR \_ RECONVERTSTRING](imr-reconvertstring.md), l’IME peut ou non ajuster la structure [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) .</span><span class="sxs-lookup"><span data-stu-id="b7c80-118">After the application has handled [IMR\_RECONVERTSTRING](imr-reconvertstring.md), the IME might or might not adjust the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure.</span></span> <span data-ttu-id="b7c80-119">L’IME envoie une \_ demande de l’IME WM \_ avec **IMR \_ CONFIRMRECONVERTSTRING** pour confirmer les modifications apportées à la structure **RECONVERTSTRING** .</span><span class="sxs-lookup"><span data-stu-id="b7c80-119">The IME sends WM\_IME\_REQUEST with **IMR\_CONFIRMRECONVERTSTRING** to confirm the changes to the **RECONVERTSTRING** structure.</span></span> <span data-ttu-id="b7c80-120">Si l’application retourne la **valeur true** pour **IMR \_ CONFIRMRECONVERTSTRING**, l’IME génère une nouvelle chaîne de composition basée sur la structure **RECONVERTSTRING** pour la commande **IMR \_ CONFIRMRECONVERTSTRING** .</span><span class="sxs-lookup"><span data-stu-id="b7c80-120">If the application returns **TRUE** for **IMR\_CONFIRMRECONVERTSTRING**, the IME generates a new composition string based on the **RECONVERTSTRING** structure for the **IMR\_CONFIRMRECONVERTSTRING** command.</span></span> <span data-ttu-id="b7c80-121">Si l’application retourne **false** pour **IMR \_ CONFIRMRECONVERTSTRING**, l’IME génère une nouvelle chaîne de composition basée sur la structure **RECONVERTSTRING** d’origine spécifiée par l’application dans la \_ commande IMR RECONVERTSTRING.</span><span class="sxs-lookup"><span data-stu-id="b7c80-121">If the application returns **FALSE** for **IMR\_CONFIRMRECONVERTSTRING**, the IME generates a new composition string based on the original **RECONVERTSTRING** structure specified by the application in the IMR\_RECONVERTSTRING command.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7c80-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7c80-122">Requirements</span></span>



| <span data-ttu-id="b7c80-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7c80-123">Requirement</span></span> | <span data-ttu-id="b7c80-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7c80-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7c80-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7c80-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b7c80-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7c80-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b7c80-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7c80-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b7c80-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7c80-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b7c80-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="b7c80-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7c80-130"><dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b7c80-130"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7c80-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7c80-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7c80-132">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="b7c80-132">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="b7c80-133">Commandes du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="b7c80-133">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="b7c80-134">IMR \_ RECONVERTSTRING</span><span class="sxs-lookup"><span data-stu-id="b7c80-134">IMR\_RECONVERTSTRING</span></span>](imr-reconvertstring.md)
</dt> <dt>

[<span data-ttu-id="b7c80-135">**RECONVERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="b7c80-135">**RECONVERTSTRING**</span></span>](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[<span data-ttu-id="b7c80-136">**demande de l' \_ IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="b7c80-136">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> </dl>

 

 




