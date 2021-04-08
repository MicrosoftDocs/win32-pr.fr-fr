---
description: Demande à une fenêtre IME d’afficher la position de la fenêtre de composition. Pour envoyer cette commande, l’application utilise le \_ message de \_ contrôle de l’IME WM avec les paramètres indiqués ci-dessous.
ms.assetid: d2c60974-a602-4a42-8a45-870ee39df001
title: Commande IMC_GETCOMPOSITIONWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b32b8f4414311d0727f622a1b552428cd31b0716
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752341"
---
# <a name="imc_getcompositionwindow-command"></a><span data-ttu-id="b0069-104">\_Commande IMC GETCOMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="b0069-104">IMC\_GETCOMPOSITIONWINDOW command</span></span>

<span data-ttu-id="b0069-105">Demande à une fenêtre IME d’afficher la position de la fenêtre de composition.</span><span class="sxs-lookup"><span data-stu-id="b0069-105">Instructs an IME window to get the position of the composition window.</span></span> <span data-ttu-id="b0069-106">Pour envoyer cette commande, l’application utilise le message de [**\_ \_ contrôle de l’IME WM**](wm-ime-control.md) avec les paramètres indiqués ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b0069-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_GETCOMPOSITIONWINDOW
```



## <a name="parameters"></a><span data-ttu-id="b0069-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0069-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0069-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="b0069-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="b0069-109">Défini sur IMC \_ GETCOMPOSITIONWINDOW.</span><span class="sxs-lookup"><span data-stu-id="b0069-109">Set to IMC\_GETCOMPOSITIONWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="b0069-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="b0069-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="b0069-111">Pointeur vers une structure [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) qui contient la position de la fenêtre de composition.</span><span class="sxs-lookup"><span data-stu-id="b0069-111">Pointer to a [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) structure that contains the position of the composition window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0069-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b0069-112">Return Value</span></span>

<span data-ttu-id="b0069-113">Retourne 0 en cas de réussite, ou une valeur différente de zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b0069-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0069-114">Notes</span><span class="sxs-lookup"><span data-stu-id="b0069-114">Remarks</span></span>

<span data-ttu-id="b0069-115">Étant donné que l’IME peut ajuster la position d’une fenêtre de composition, une application utilise cette commande pour obtenir la position réelle pour décider s’il faut repositionner la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b0069-115">Because the IME might adjust the position of a composition window, an application uses this command to get the actual position to decide whether to reposition the window.</span></span> <span data-ttu-id="b0069-116">La position Récupérée est dans les coordonnées de la fenêtre par rapport à la fenêtre qui a le focus d’entrée actuel.</span><span class="sxs-lookup"><span data-stu-id="b0069-116">The retrieved position is in window coordinates relative to the window having the current input focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0069-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0069-117">Requirements</span></span>



| <span data-ttu-id="b0069-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0069-118">Requirement</span></span> | <span data-ttu-id="b0069-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0069-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0069-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0069-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b0069-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b0069-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b0069-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0069-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b0069-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b0069-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b0069-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="b0069-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0069-125"><dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b0069-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0069-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0069-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0069-127">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="b0069-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="b0069-128">Commandes du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="b0069-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="b0069-129">**COMPOSITIONFORM**</span><span class="sxs-lookup"><span data-stu-id="b0069-129">**COMPOSITIONFORM**</span></span>](/windows/win32/api/imm/ns-imm-compositionform)
</dt> </dl>

 

 




