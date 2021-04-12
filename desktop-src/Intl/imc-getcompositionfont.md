---
description: Fait en sorte qu’une fenêtre IME récupère la police logique utilisée pour l’affichage des caractères intermédiaires dans la fenêtre de composition. Pour envoyer cette commande, l’application utilise le \_ message de \_ contrôle de l’IME WM avec les paramètres indiqués ci-dessous.
ms.assetid: 43db70b6-f8bc-4241-9096-5d91fd1e332b
title: Commande IMC_GETCOMPOSITIONFONT (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696d9809cadbe4f2c0e632719401e882777888dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201600"
---
# <a name="imc_getcompositionfont-command"></a><span data-ttu-id="6a763-104">\_Commande IMC GETCOMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="6a763-104">IMC\_GETCOMPOSITIONFONT command</span></span>

<span data-ttu-id="6a763-105">Fait en sorte qu’une fenêtre IME récupère la police logique utilisée pour l’affichage des caractères intermédiaires dans la fenêtre de composition.</span><span class="sxs-lookup"><span data-stu-id="6a763-105">Instructs an IME window to retrieve the logical font used for displaying intermediate characters in the composition window.</span></span> <span data-ttu-id="6a763-106">Pour envoyer cette commande, l’application utilise le message de [**\_ \_ contrôle de l’IME WM**](wm-ime-control.md) avec les paramètres indiqués ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="6a763-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_GETCOMPOSITIONFONT
```



## <a name="parameters"></a><span data-ttu-id="6a763-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a763-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a763-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="6a763-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="6a763-109">Défini sur IMC \_ GETCOMPOSITIONFONT.</span><span class="sxs-lookup"><span data-stu-id="6a763-109">Set to IMC\_GETCOMPOSITIONFONT.</span></span>

</dd> <dt>

<span data-ttu-id="6a763-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="6a763-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="6a763-111">Pointeur vers une structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) qui reçoit des informations sur la police logique.</span><span class="sxs-lookup"><span data-stu-id="6a763-111">Pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that receives information about the logical font.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a763-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6a763-112">Return Value</span></span>

<span data-ttu-id="6a763-113">Retourne 0 en cas de réussite, ou une valeur différente de zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6a763-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a763-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a763-114">Requirements</span></span>



| <span data-ttu-id="6a763-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a763-115">Requirement</span></span> | <span data-ttu-id="6a763-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a763-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a763-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a763-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6a763-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a763-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6a763-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a763-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6a763-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a763-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6a763-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="6a763-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a763-122"><dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6a763-122"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a763-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a763-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a763-124">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="6a763-124">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="6a763-125">Commandes du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="6a763-125">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> </dl>

 

 
