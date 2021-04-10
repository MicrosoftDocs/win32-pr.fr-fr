---
description: Indique à la fenêtre IME de masquer la fenêtre d’État. Pour envoyer cette commande, l’application utilise le \_ message de \_ contrôle de l’IME WM avec les paramètres indiqués ci-dessous.
ms.assetid: e3da5962-a652-409e-b0ec-eb93671049b4
title: Commande IMC_CLOSESTATUSWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 207f04d53f269318f87ed11038cbd6817d5e607e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869262"
---
# <a name="imc_closestatuswindow-command"></a><span data-ttu-id="61cbb-104">\_Commande IMC CLOSESTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="61cbb-104">IMC\_CLOSESTATUSWINDOW command</span></span>

<span data-ttu-id="61cbb-105">Indique à la fenêtre IME de masquer la fenêtre d’État.</span><span class="sxs-lookup"><span data-stu-id="61cbb-105">Instructs the IME window to hide the status window.</span></span> <span data-ttu-id="61cbb-106">Pour envoyer cette commande, l’application utilise le message de [**\_ \_ contrôle de l’IME WM**](wm-ime-control.md) avec les paramètres indiqués ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="61cbb-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_CLOSESTATUSWINDOW
```



## <a name="parameters"></a><span data-ttu-id="61cbb-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61cbb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61cbb-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="61cbb-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="61cbb-109">Défini sur IMC \_ CLOSESTATUSWINDOW.</span><span class="sxs-lookup"><span data-stu-id="61cbb-109">Set to IMC\_CLOSESTATUSWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="61cbb-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="61cbb-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="61cbb-111">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="61cbb-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61cbb-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="61cbb-112">Return Value</span></span>

<span data-ttu-id="61cbb-113">Retourne 0 en cas de réussite, ou une valeur différente de zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="61cbb-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="61cbb-114">Notes</span><span class="sxs-lookup"><span data-stu-id="61cbb-114">Remarks</span></span>

<span data-ttu-id="61cbb-115">Lorsque la fenêtre d’État IME est déjà masquée, cette commande ne fait rien.</span><span class="sxs-lookup"><span data-stu-id="61cbb-115">When the IME status window is already hidden, this command does nothing.</span></span> <span data-ttu-id="61cbb-116">Bien qu’une application puisse envoyer cette commande à la fenêtre IME, l’application ne reçoit pas la [commande \_ CLOSESTATUSWINDOW IMN](imn-closestatuswindow.md) correspondante.</span><span class="sxs-lookup"><span data-stu-id="61cbb-116">Although an application can send this command to the IME window, the application does not receive the corresponding [IMN\_CLOSESTATUSWINDOW](imn-closestatuswindow.md) command.</span></span>

## <a name="requirements"></a><span data-ttu-id="61cbb-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61cbb-117">Requirements</span></span>



| <span data-ttu-id="61cbb-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61cbb-118">Requirement</span></span> | <span data-ttu-id="61cbb-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="61cbb-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61cbb-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61cbb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="61cbb-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61cbb-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="61cbb-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61cbb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="61cbb-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61cbb-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="61cbb-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="61cbb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="61cbb-125"><dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="61cbb-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61cbb-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61cbb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61cbb-127">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="61cbb-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="61cbb-128">Commandes du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="61cbb-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> </dl>

 

 




