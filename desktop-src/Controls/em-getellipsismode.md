---
title: Message EM_GETELLIPSISMODE (RichEdit. h)
description: Récupère le mode de sélection en cours.
ms.assetid: 01A755F3-6C6E-4974-9866-76BF15E0F3AD
keywords:
- EM_GETELLIPSISMODE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETELLIPSISMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09b7273cbfd6e87b4591c00267860c9a164aad5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103786"
---
# <a name="em_getellipsismode-message"></a><span data-ttu-id="9e459-104">\_Message GETELLIPSISMODE em</span><span class="sxs-lookup"><span data-stu-id="9e459-104">EM\_GETELLIPSISMODE message</span></span>

<span data-ttu-id="9e459-105">Récupère le mode de sélection en cours.</span><span class="sxs-lookup"><span data-stu-id="9e459-105">Retrieves the current ellipsis mode.</span></span> <span data-ttu-id="9e459-106">Quand cette option est activée, des points de suspension () s’affichent pour le texte qui ne tient pas dans la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="9e459-106">When enabled, an ellipsis ( ) is displayed for text that doesn t fit in the display window.</span></span> <span data-ttu-id="9e459-107">Les points de suspension sont utilisés uniquement lorsque le contrôle n’est pas actif.</span><span class="sxs-lookup"><span data-stu-id="9e459-107">The ellipsis is only used when the control is not active.</span></span> <span data-ttu-id="9e459-108">Lorsqu’elles sont actives, les barres de défilement sont utilisées pour révéler le texte qui ne tient pas dans la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="9e459-108">When active, scroll bars are used to reveal text that doesn t fit into the display window.</span></span>


```C++
#define EM_GETELLIPSISMODE       (WM_USER + 305)
```



## <a name="parameters"></a><span data-ttu-id="9e459-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e459-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e459-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9e459-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e459-111">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="9e459-111">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9e459-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9e459-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e459-113">Pointeur vers une valeur DWORD qui reçoit l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="9e459-113">Pointer to a DWORD which receives one of the following values.</span></span>



| <span data-ttu-id="9e459-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e459-114">Value</span></span>                                                                                                                                                         | <span data-ttu-id="9e459-115">Signification</span><span class="sxs-lookup"><span data-stu-id="9e459-115">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <span data-ttu-id="9e459-116"><dt>**POINTS de suspension \_ aucun**</dt></span><span class="sxs-lookup"><span data-stu-id="9e459-116"><dt>**ELLIPSIS\_NONE**</dt></span></span> </dl> | <span data-ttu-id="9e459-117">Aucun bouton de sélection n’est utilisé.</span><span class="sxs-lookup"><span data-stu-id="9e459-117">No ellipsis is used.</span></span><br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <span data-ttu-id="9e459-118"><dt>**fin des points de suspension \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9e459-118"><dt>**ELLIPSIS\_END**</dt></span></span> </dl>    | <span data-ttu-id="9e459-119">Points de suspension à la fin (arrêt forcé).</span><span class="sxs-lookup"><span data-stu-id="9e459-119">Ellipsis at the end (forced break).</span></span><br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <span data-ttu-id="9e459-120"><dt>**mot de points de suspension \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9e459-120"><dt>**ELLIPSIS\_WORD**</dt></span></span> </dl> | <span data-ttu-id="9e459-121">Points de suspension à la fin (saut de mot).</span><span class="sxs-lookup"><span data-stu-id="9e459-121">Ellipsis at the end (word break).</span></span><br/>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e459-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9e459-122">Return value</span></span>

<span data-ttu-id="9e459-123">Si wParam est 0 et lParam n’est pas NULL, la valeur de retour est égale à TRUE ; Sinon, la valeur de retour est FALSe.</span><span class="sxs-lookup"><span data-stu-id="9e459-123">If wparam is 0 and lparam is not NULL, the return value equals TRUE; otherwise, the return value equals FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e459-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e459-124">Requirements</span></span>



| <span data-ttu-id="9e459-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e459-125">Requirement</span></span> | <span data-ttu-id="9e459-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e459-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e459-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e459-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9e459-128">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9e459-128">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="9e459-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e459-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9e459-130">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9e459-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9e459-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="9e459-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e459-132"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e459-132"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e459-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e459-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e459-134">**\_SETELLIPSISMODE em**</span><span class="sxs-lookup"><span data-stu-id="9e459-134">**EM\_SETELLIPSISMODE**</span></span>](em-setellipsismode.md)
</dt> <dt>

[<span data-ttu-id="9e459-135">**\_GETELLIPSISSTATE em**</span><span class="sxs-lookup"><span data-stu-id="9e459-135">**EM\_GETELLIPSISSTATE**</span></span>](em-getellipsisstate.md)
</dt> </dl>

 

 





