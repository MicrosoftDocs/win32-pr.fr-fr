---
description: Avertit une application quand un IME sélectionné a besoin d’une chaîne pour la reconversion. L’application reçoit cette commande via le \_ \_ message de demande de l’IME WM avec les paramètres de paramètre, comme indiqué ci-dessous.
ms.assetid: 82ef20b5-bdfa-4bde-abb4-3d14ae35c116
title: IMR_RECONVERTSTRING le code de notification (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cbb1caeedb729b176f116a15e64879d79d519fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864882"
---
# <a name="imr_reconvertstring-notification-code"></a><span data-ttu-id="8e09e-104">\_Code de notification IMR RECONVERTSTRING</span><span class="sxs-lookup"><span data-stu-id="8e09e-104">IMR\_RECONVERTSTRING notification code</span></span>

<span data-ttu-id="8e09e-105">Avertit une application quand un IME sélectionné a besoin d’une chaîne pour la reconversion.</span><span class="sxs-lookup"><span data-stu-id="8e09e-105">Notifies an application when a selected IME needs a string for reconversion.</span></span> <span data-ttu-id="8e09e-106">L’application reçoit cette commande via le message de [**\_ \_ demande de l’IME WM**](wm-ime-request.md) avec les paramètres de paramètre, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="8e09e-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMR_RECONVERTSTRING
```



## <a name="parameters"></a><span data-ttu-id="8e09e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e09e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e09e-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="8e09e-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="8e09e-109">Définissez sur IMR \_ RECONVERTSTRING.</span><span class="sxs-lookup"><span data-stu-id="8e09e-109">Set to IMR\_RECONVERTSTRING.</span></span>

</dd> <dt>

<span data-ttu-id="8e09e-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="8e09e-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="8e09e-111">Pointeur vers une mémoire tampon contenant la structure et les chaînes [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) .</span><span class="sxs-lookup"><span data-stu-id="8e09e-111">Pointer to a buffer containing the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure and strings.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e09e-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8e09e-112">Return Value</span></span>

<span data-ttu-id="8e09e-113">Retourne la structure actuelle de la chaîne de reconversion.</span><span class="sxs-lookup"><span data-stu-id="8e09e-113">Returns the current reconversion string structure.</span></span> <span data-ttu-id="8e09e-114">Si *lParam* a la valeur **null**, l’application retourne la taille de la mémoire tampon requise pour contenir la structure.</span><span class="sxs-lookup"><span data-stu-id="8e09e-114">If *lParam* is set to **NULL**, the application returns the size for the buffer required to hold the structure.</span></span> <span data-ttu-id="8e09e-115">La commande retourne 0 en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="8e09e-115">The command returns 0 if it does not succeed.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e09e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e09e-116">Requirements</span></span>



| <span data-ttu-id="8e09e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e09e-117">Requirement</span></span> | <span data-ttu-id="8e09e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e09e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e09e-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e09e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8e09e-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8e09e-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8e09e-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e09e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8e09e-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8e09e-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8e09e-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="8e09e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e09e-124"><dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8e09e-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e09e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e09e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e09e-126">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="8e09e-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="8e09e-127">Commandes du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="8e09e-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="8e09e-128">**RECONVERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="8e09e-128">**RECONVERTSTRING**</span></span>](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[<span data-ttu-id="8e09e-129">**demande de l' \_ IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="8e09e-129">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> </dl>

 

 




