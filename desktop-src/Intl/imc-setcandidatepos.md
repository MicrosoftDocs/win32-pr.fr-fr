---
description: Demande à une fenêtre IME de définir la position de la fenêtre candidats. Pour envoyer cette commande, l’application utilise le \_ message de \_ contrôle de l’IME WM avec les paramètres indiqués ci-dessous.
ms.assetid: 7a2f9958-4a4e-462a-9737-e7796fd90216
title: Commande IMC_SETCANDIDATEPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8ac05890e4c720c5b671faa7f20a68a96b24a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752348"
---
# <a name="imc_setcandidatepos-command"></a><span data-ttu-id="d7b59-104">\_Commande IMC SETCANDIDATEPOS</span><span class="sxs-lookup"><span data-stu-id="d7b59-104">IMC\_SETCANDIDATEPOS command</span></span>

<span data-ttu-id="d7b59-105">Demande à une fenêtre IME de définir la position de la fenêtre candidats.</span><span class="sxs-lookup"><span data-stu-id="d7b59-105">Instructs an IME window to set the position of the candidates window.</span></span> <span data-ttu-id="d7b59-106">Pour envoyer cette commande, l’application utilise le message de [**\_ \_ contrôle de l’IME WM**](wm-ime-control.md) avec les paramètres indiqués ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="d7b59-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_SETCANDIDATEPOS
```



## <a name="parameters"></a><span data-ttu-id="d7b59-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7b59-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7b59-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="d7b59-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="d7b59-109">Défini sur IMC \_ SETCANDIDATEPOS.</span><span class="sxs-lookup"><span data-stu-id="d7b59-109">Set to IMC\_SETCANDIDATEPOS.</span></span>

</dd> <dt>

<span data-ttu-id="d7b59-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7b59-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="d7b59-111">Pointeur vers une structure [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) qui contient la coordonnée x et la coordonnée y de la fenêtre candidats.</span><span class="sxs-lookup"><span data-stu-id="d7b59-111">Pointer to a [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) structure that contains the x coordinate and y coordinate for the candidates window.</span></span> <span data-ttu-id="d7b59-112">L’application doit définir le membre **dwIndex** de cette structure.</span><span class="sxs-lookup"><span data-stu-id="d7b59-112">The application should set the **dwIndex** member of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7b59-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d7b59-113">Return Value</span></span>

<span data-ttu-id="d7b59-114">Retourne 0 en cas de réussite, ou une valeur différente de zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d7b59-114">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7b59-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d7b59-115">Remarks</span></span>

<span data-ttu-id="d7b59-116">Cette commande est destinée aux applications qui affichent des caractères de composition seuls, mais qui utilisent la fenêtre IME pour afficher les candidats.</span><span class="sxs-lookup"><span data-stu-id="d7b59-116">This command is intended for applications that display composition characters on their own but use the IME window to display candidates.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7b59-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7b59-117">Requirements</span></span>



| <span data-ttu-id="d7b59-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7b59-118">Requirement</span></span> | <span data-ttu-id="d7b59-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7b59-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7b59-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7b59-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d7b59-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7b59-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d7b59-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7b59-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d7b59-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7b59-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d7b59-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7b59-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7b59-125"><dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d7b59-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7b59-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7b59-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7b59-127">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="d7b59-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="d7b59-128">Commandes du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="d7b59-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="d7b59-129">**CANDIDATEFORM**</span><span class="sxs-lookup"><span data-stu-id="d7b59-129">**CANDIDATEFORM**</span></span>](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[<span data-ttu-id="d7b59-130">**contrôle de l' \_ IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="d7b59-130">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 




