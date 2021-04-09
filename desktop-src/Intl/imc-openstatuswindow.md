---
description: Indique à la fenêtre IME d’afficher la fenêtre d’État. Pour envoyer cette commande, l’application utilise le \_ message de \_ contrôle de l’IME WM avec les paramètres indiqués ci-dessous.
ms.assetid: 8c422592-ef59-4030-b684-81e4e552c6b0
title: Commande IMC_OPENSTATUSWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd0b5e19ef6a026459eedb050e9ac9587b5ea24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862925"
---
# <a name="imc_openstatuswindow-command"></a><span data-ttu-id="4de54-104">\_Commande IMC OPENSTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="4de54-104">IMC\_OPENSTATUSWINDOW command</span></span>

<span data-ttu-id="4de54-105">Indique à la fenêtre IME d’afficher la fenêtre d’État.</span><span class="sxs-lookup"><span data-stu-id="4de54-105">Instructs the IME window to show the status window.</span></span> <span data-ttu-id="4de54-106">Pour envoyer cette commande, l’application utilise le message de [**\_ \_ contrôle de l’IME WM**](wm-ime-control.md) avec les paramètres indiqués ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="4de54-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_OPENSTATUSWINDOW
```



## <a name="parameters"></a><span data-ttu-id="4de54-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4de54-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4de54-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="4de54-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="4de54-109">Défini sur IMC \_ OPENSTATUSWINDOW.</span><span class="sxs-lookup"><span data-stu-id="4de54-109">Set to IMC\_OPENSTATUSWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="4de54-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="4de54-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="4de54-111">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="4de54-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4de54-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4de54-112">Return Value</span></span>

<span data-ttu-id="4de54-113">Retourne 0 en cas de réussite, ou une valeur différente de zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4de54-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4de54-114">Notes</span><span class="sxs-lookup"><span data-stu-id="4de54-114">Remarks</span></span>

<span data-ttu-id="4de54-115">Cette commande est ignorée si le système d’exploitation n’est pas dans le mode afficher l’État IME.</span><span class="sxs-lookup"><span data-stu-id="4de54-115">This command is ignored if the operating system is not in the show IME status mode.</span></span> <span data-ttu-id="4de54-116">L’utilisateur peut définir ou désactiver le mode afficher l’État IME à partir de la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="4de54-116">The user can set or clear the show IME status mode from the task bar.</span></span>

<span data-ttu-id="4de54-117">Si la fenêtre d’État est déjà affichée, cette commande ne fait rien.</span><span class="sxs-lookup"><span data-stu-id="4de54-117">If the status window is already shown, this command does nothing.</span></span> <span data-ttu-id="4de54-118">Bien que l’application puisse envoyer cette commande à la fenêtre IME, l’application ne reçoit pas la [**commande \_ OPENSTATUSWINDOW IMN**](imn-openstatuswindow.md) correspondante.</span><span class="sxs-lookup"><span data-stu-id="4de54-118">Although the application can send this command to the IME window, the application does not receive the corresponding [**IMN\_OPENSTATUSWINDOW**](imn-openstatuswindow.md) command.</span></span>

## <a name="requirements"></a><span data-ttu-id="4de54-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4de54-119">Requirements</span></span>



| <span data-ttu-id="4de54-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4de54-120">Requirement</span></span> | <span data-ttu-id="4de54-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="4de54-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4de54-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4de54-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4de54-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4de54-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4de54-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4de54-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4de54-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4de54-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4de54-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="4de54-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4de54-127"><dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4de54-127"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4de54-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4de54-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4de54-129">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="4de54-129">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="4de54-130">Commandes du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="4de54-130">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="4de54-131">**contrôle de l' \_ IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="4de54-131">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 




