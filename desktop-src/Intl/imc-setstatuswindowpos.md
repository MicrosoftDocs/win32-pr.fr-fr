---
description: Demande à une fenêtre IME de définir la position de la fenêtre d’État. Pour envoyer cette commande, l’application utilise le \_ \_ message de contrôle de l’IME WM avec les paramètres de paramètre, comme indiqué ci-dessous.
ms.assetid: d77de7ab-1fbc-42f4-829e-e9fb51668d21
title: Commande IMC_SETSTATUSWINDOWPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f99c57eef1a4748bb58018ee47aaee21eb677016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034057"
---
# <a name="imc_setstatuswindowpos-command"></a><span data-ttu-id="85054-104">\_Commande IMC SETSTATUSWINDOWPOS</span><span class="sxs-lookup"><span data-stu-id="85054-104">IMC\_SETSTATUSWINDOWPOS command</span></span>

<span data-ttu-id="85054-105">Demande à une fenêtre IME de définir la position de la fenêtre d’État.</span><span class="sxs-lookup"><span data-stu-id="85054-105">Instructs an IME window to set the position of the status window.</span></span> <span data-ttu-id="85054-106">Pour envoyer cette commande, l’application utilise le message de [**\_ \_ contrôle de l’IME WM**](wm-ime-control.md) avec les paramètres de paramètre, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="85054-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMC_SETSTATUSWINDOWPOS
```



## <a name="parameters"></a><span data-ttu-id="85054-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="85054-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85054-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="85054-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="85054-109">Défini sur IMC \_ SETSTATUSWINDOWPOS.</span><span class="sxs-lookup"><span data-stu-id="85054-109">Set to IMC\_SETSTATUSWINDOWPOS.</span></span>

</dd> <dt>

<span data-ttu-id="85054-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="85054-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="85054-111">Pointeur vers une structure de [**points**](/previous-versions//dd162808(v=vs.85)) qui contient la coordonnée x et la coordonnée y de la position de la fenêtre d’État.</span><span class="sxs-lookup"><span data-stu-id="85054-111">Pointer to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x coordinate and y coordinate of the position of the status window.</span></span> <span data-ttu-id="85054-112">Les coordonnées sont exprimées en coordonnées d’écran, par rapport à l’angle supérieur gauche de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="85054-112">The coordinates are in screen coordinates, relative to the upper left corner of the display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85054-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="85054-113">Return Value</span></span>

<span data-ttu-id="85054-114">Retourne 0 en cas de réussite, ou une valeur différente de zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="85054-114">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="85054-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85054-115">Requirements</span></span>



| <span data-ttu-id="85054-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85054-116">Requirement</span></span> | <span data-ttu-id="85054-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="85054-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85054-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85054-118">Minimum supported client</span></span><br/> | <span data-ttu-id="85054-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85054-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="85054-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85054-120">Minimum supported server</span></span><br/> | <span data-ttu-id="85054-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85054-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="85054-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="85054-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="85054-123"><dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="85054-123"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85054-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85054-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85054-125">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="85054-125">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="85054-126">Commandes du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="85054-126">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="85054-127">**contrôle de l' \_ IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="85054-127">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 
