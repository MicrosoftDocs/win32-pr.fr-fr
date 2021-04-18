---
description: Demande à une fenêtre IME d’afficher la position de la fenêtre d’État. Pour envoyer cette commande, l’application utilise le \_ message de \_ contrôle de l’IME WM avec les paramètres indiqués ci-dessous.
ms.assetid: 59c7baae-1b8a-4761-9814-31afd8d39691
title: Commande IMC_GETSTATUSWINDOWPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfd17c5787d9ef8c787e62a556afa2f136bd65c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519338"
---
# <a name="imc_getstatuswindowpos-command"></a><span data-ttu-id="86774-104">\_Commande IMC GETSTATUSWINDOWPOS</span><span class="sxs-lookup"><span data-stu-id="86774-104">IMC\_GETSTATUSWINDOWPOS command</span></span>

<span data-ttu-id="86774-105">Demande à une fenêtre IME d’afficher la position de la fenêtre d’État.</span><span class="sxs-lookup"><span data-stu-id="86774-105">Instructs an IME window to get the position of the status window.</span></span> <span data-ttu-id="86774-106">Pour envoyer cette commande, l’application utilise le message de [**\_ \_ contrôle de l’IME WM**](wm-ime-control.md) avec les paramètres indiqués ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="86774-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_GETSTATUSWINDOWPOS
```



## <a name="parameters"></a><span data-ttu-id="86774-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86774-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86774-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="86774-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="86774-109">Défini sur IMC \_ GETSTATUSWINDOWPOS.</span><span class="sxs-lookup"><span data-stu-id="86774-109">Set to IMC\_GETSTATUSWINDOWPOS.</span></span>

</dd> <dt>

<span data-ttu-id="86774-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="86774-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="86774-111">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="86774-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86774-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="86774-112">Return Value</span></span>

<span data-ttu-id="86774-113">Retourne une structure de [**points**](/previous-versions//dd162808(v=vs.85)) qui contient la coordonnée x et la coordonnée y de la position de la fenêtre d’État en coordonnées d’écran, par rapport à l’angle supérieur gauche de l’écran.</span><span class="sxs-lookup"><span data-stu-id="86774-113">Returns a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x coordinate and y coordinate of the status window position in screen coordinates, relative to the upper left corner of the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="86774-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86774-114">Requirements</span></span>



| <span data-ttu-id="86774-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86774-115">Requirement</span></span> | <span data-ttu-id="86774-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="86774-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86774-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86774-117">Minimum supported client</span></span><br/> | <span data-ttu-id="86774-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="86774-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="86774-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86774-119">Minimum supported server</span></span><br/> | <span data-ttu-id="86774-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="86774-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="86774-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="86774-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="86774-122"><dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86774-122"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86774-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86774-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86774-124">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="86774-124">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="86774-125">Commandes du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="86774-125">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="86774-126">**contrôle de l' \_ IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="86774-126">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 
