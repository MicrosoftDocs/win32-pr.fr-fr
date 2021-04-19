---
description: Demande à une fenêtre IME de définir le style de la fenêtre de composition. Pour envoyer cette commande, l’application utilise le \_ message de \_ contrôle de l’IME WM avec les paramètres indiqués ci-dessous.
ms.assetid: 19b99228-a1fc-4cd5-8f37-5462bf767f85
title: Commande IMC_SETCOMPOSITIONWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b06c53b1ff2ec343d6382dd48d0d4108cf403c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531670"
---
# <a name="imc_setcompositionwindow-command"></a><span data-ttu-id="c9408-104">\_Commande IMC SETCOMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="c9408-104">IMC\_SETCOMPOSITIONWINDOW command</span></span>

<span data-ttu-id="c9408-105">Demande à une fenêtre IME de définir le style de la fenêtre de composition.</span><span class="sxs-lookup"><span data-stu-id="c9408-105">Instructs an IME window to set the style of the composition window.</span></span> <span data-ttu-id="c9408-106">Pour envoyer cette commande, l’application utilise le message de [**\_ \_ contrôle de l’IME WM**](wm-ime-control.md) avec les paramètres indiqués ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="c9408-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_SETCOMPOSITIONWINDOW
```



## <a name="parameters"></a><span data-ttu-id="c9408-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9408-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9408-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="c9408-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="c9408-109">Défini sur IMC \_ SETCOMPOSITIONWINDOW.</span><span class="sxs-lookup"><span data-stu-id="c9408-109">Set to IMC\_SETCOMPOSITIONWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="c9408-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="c9408-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="c9408-111">Pointeur vers une structure [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) qui contient les informations de style.</span><span class="sxs-lookup"><span data-stu-id="c9408-111">Pointer to a [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) structure that contains the style information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9408-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c9408-112">Return Value</span></span>

<span data-ttu-id="c9408-113">Retourne 0 en cas de réussite, ou une valeur différente de zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c9408-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9408-114">Notes</span><span class="sxs-lookup"><span data-stu-id="c9408-114">Remarks</span></span>

<span data-ttu-id="c9408-115">Cette commande définit le style dans le contexte d’entrée actuel, et le style est ensuite appliqué à chaque fenêtre IME qui reçoit ce contexte d’entrée.</span><span class="sxs-lookup"><span data-stu-id="c9408-115">This command sets the style in the current input context, and the style is subsequently applied to each IME window that receives that input context.</span></span>

<span data-ttu-id="c9408-116">Par défaut, la fenêtre IME a le \_ style point cfs.</span><span class="sxs-lookup"><span data-stu-id="c9408-116">By default, the IME window has the CFS\_POINT style.</span></span> <span data-ttu-id="c9408-117">Avec ce style, la fenêtre IME utilise l’emplacement actuel du signe insertion et la zone cliente de la fenêtre quand elle ouvre une fenêtre de composition.</span><span class="sxs-lookup"><span data-stu-id="c9408-117">With this style, the IME window uses the current caret position and window client area when it opens any composition window.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9408-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9408-118">Requirements</span></span>



| <span data-ttu-id="c9408-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9408-119">Requirement</span></span> | <span data-ttu-id="c9408-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9408-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9408-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9408-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c9408-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9408-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c9408-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9408-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c9408-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9408-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c9408-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9408-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9408-126"><dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9408-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9408-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9408-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9408-128">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="c9408-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="c9408-129">Commandes du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="c9408-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="c9408-130">**COMPOSITIONFORM**</span><span class="sxs-lookup"><span data-stu-id="c9408-130">**COMPOSITIONFORM**</span></span>](/windows/win32/api/imm/ns-imm-compositionform)
</dt> <dt>

[<span data-ttu-id="c9408-131">**contrôle de l' \_ IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="c9408-131">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 




