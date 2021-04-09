---
description: Indique à une fenêtre IME de spécifier la police logique à utiliser pour afficher les caractères intermédiaires dans la fenêtre de composition. Pour envoyer cette commande, l’application utilise le \_ message de \_ contrôle de l’IME WM avec les paramètres indiqués ci-dessous.
ms.assetid: 17b222e7-bf57-4cdd-8475-d9a8be03ab7f
title: Commande IMC_SETCOMPOSITIONFONT (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbb84c9e05ab19206064988a71b0ffc39b21a44b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862922"
---
# <a name="imc_setcompositionfont-command"></a><span data-ttu-id="d9122-104">\_Commande IMC SETCOMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="d9122-104">IMC\_SETCOMPOSITIONFONT command</span></span>

<span data-ttu-id="d9122-105">Indique à une fenêtre IME de spécifier la police logique à utiliser pour afficher les caractères intermédiaires dans la fenêtre de composition.</span><span class="sxs-lookup"><span data-stu-id="d9122-105">Instructs an IME window to specify the logical font to use for displaying intermediate characters in the composition window.</span></span> <span data-ttu-id="d9122-106">Pour envoyer cette commande, l’application utilise le message de [**\_ \_ contrôle de l’IME WM**](wm-ime-control.md) avec les paramètres indiqués ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="d9122-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_SETCOMPOSITIONFONT
```



## <a name="parameters"></a><span data-ttu-id="d9122-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d9122-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9122-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="d9122-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="d9122-109">Défini sur IMC \_ SETCOMPOSITIONFONT.</span><span class="sxs-lookup"><span data-stu-id="d9122-109">Set to IMC\_SETCOMPOSITIONFONT.</span></span>

</dd> <dt>

<span data-ttu-id="d9122-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9122-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="d9122-111">Pointeur vers une structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) qui contient des informations sur la police logique.</span><span class="sxs-lookup"><span data-stu-id="d9122-111">Pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that contains information about the logical font.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9122-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d9122-112">Return Value</span></span>

<span data-ttu-id="d9122-113">Retourne 0 en cas de réussite, ou une valeur différente de zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d9122-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9122-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d9122-114">Remarks</span></span>

<span data-ttu-id="d9122-115">Lors du traitement de cette commande, la fenêtre IME modifie la police actuellement sélectionnée dans le contexte d’entrée.</span><span class="sxs-lookup"><span data-stu-id="d9122-115">When processing this command, the IME window changes the current selected font in the input context.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9122-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9122-116">Requirements</span></span>



| <span data-ttu-id="d9122-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d9122-117">Requirement</span></span> | <span data-ttu-id="d9122-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d9122-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9122-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9122-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d9122-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d9122-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d9122-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9122-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d9122-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d9122-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d9122-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="d9122-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9122-124"><dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d9122-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9122-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9122-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9122-126">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="d9122-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="d9122-127">Commandes du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="d9122-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="d9122-128">**contrôle de l' \_ IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="d9122-128">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 
