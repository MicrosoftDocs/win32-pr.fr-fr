---
title: Message EM_SETELLIPSISMODE (RichEdit. h)
description: Ce message définit le mode de sélection en cours.
ms.assetid: C77263E8-424B-4EDE-ACBF-BA85248FC31F
keywords:
- EM_SETELLIPSISMODE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETELLIPSISMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81ae3b51dc80ed11d71f4af9c292657b2cf16728
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033150"
---
# <a name="em_setellipsismode-message"></a><span data-ttu-id="c7bf6-104">\_Message SETELLIPSISMODE em</span><span class="sxs-lookup"><span data-stu-id="c7bf6-104">EM\_SETELLIPSISMODE message</span></span>

<span data-ttu-id="c7bf6-105">Ce message définit le mode de sélection en cours.</span><span class="sxs-lookup"><span data-stu-id="c7bf6-105">This message sets the current ellipsis mode.</span></span> <span data-ttu-id="c7bf6-106">Quand cette option est activée, des points de suspension () s’affichent pour le texte qui ne tient pas dans la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="c7bf6-106">When enabled, an ellipsis ( ) is displayed for text that doesn t fit in the display window.</span></span> <span data-ttu-id="c7bf6-107">Les points de suspension sont utilisés uniquement lorsque le contrôle n’est pas actif.</span><span class="sxs-lookup"><span data-stu-id="c7bf6-107">The ellipsis is only used when the control isn t active.</span></span> <span data-ttu-id="c7bf6-108">Lorsqu’elles sont actives, les barres de défilement sont utilisées pour révéler le texte qui ne tient pas dans la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="c7bf6-108">When active, scroll bars are used to reveal text that doesn t fit into the display window.</span></span>


```C++
#define EM_SETELLIPSISMODE       (WM_USER + 306)
```



## <a name="parameters"></a><span data-ttu-id="c7bf6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7bf6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7bf6-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c7bf6-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7bf6-111">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="c7bf6-111">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c7bf6-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c7bf6-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7bf6-113">Valeur DWORD qui reçoit l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c7bf6-113">A DWORD which receives one of the following values.</span></span>



| <span data-ttu-id="c7bf6-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7bf6-114">Value</span></span>                                                                                                                                                         | <span data-ttu-id="c7bf6-115">Signification</span><span class="sxs-lookup"><span data-stu-id="c7bf6-115">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <span data-ttu-id="c7bf6-116"><dt>**POINTS de suspension \_ aucun**</dt></span><span class="sxs-lookup"><span data-stu-id="c7bf6-116"><dt>**ELLIPSIS\_NONE**</dt></span></span> </dl> | <span data-ttu-id="c7bf6-117">Aucun bouton de sélection n’est utilisé.</span><span class="sxs-lookup"><span data-stu-id="c7bf6-117">No ellipsis is used.</span></span><br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <span data-ttu-id="c7bf6-118"><dt>**fin des points de suspension \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c7bf6-118"><dt>**ELLIPSIS\_END**</dt></span></span> </dl>    | <span data-ttu-id="c7bf6-119">Points de suspension à la fin (arrêt forcé).</span><span class="sxs-lookup"><span data-stu-id="c7bf6-119">Ellipsis at the end (forced break).</span></span><br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <span data-ttu-id="c7bf6-120"><dt>**mot de points de suspension \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c7bf6-120"><dt>**ELLIPSIS\_WORD**</dt></span></span> </dl> | <span data-ttu-id="c7bf6-121">Points de suspension à la fin (saut de mot).</span><span class="sxs-lookup"><span data-stu-id="c7bf6-121">Ellipsis at the end (word break).</span></span><br/>   |



 

<span data-ttu-id="c7bf6-122">Les bits de ces valeurs tiennent tous dans le **\_ masque des points de suspension**.</span><span class="sxs-lookup"><span data-stu-id="c7bf6-122">The bits for these values all fit in the **ELLIPSIS\_MASK**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7bf6-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c7bf6-123">Return value</span></span>

<span data-ttu-id="c7bf6-124">Si wParam est 0 et lParam est l’une des valeurs du tableau ci-dessus, la valeur de retour est égale à TRUE ; Sinon, la valeur de retour est FALSe.</span><span class="sxs-lookup"><span data-stu-id="c7bf6-124">If wparam is 0 and lparam is one of the values in the table above, the return value equals TRUE; otherwise, the return value equals FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7bf6-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7bf6-125">Requirements</span></span>



| <span data-ttu-id="c7bf6-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7bf6-126">Requirement</span></span> | <span data-ttu-id="c7bf6-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7bf6-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c7bf6-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7bf6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c7bf6-129">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7bf6-129">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c7bf6-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7bf6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c7bf6-131">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7bf6-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c7bf6-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="c7bf6-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7bf6-133"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7bf6-133"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7bf6-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7bf6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7bf6-135">**\_GETELLIPSISMODE em**</span><span class="sxs-lookup"><span data-stu-id="c7bf6-135">**EM\_GETELLIPSISMODE**</span></span>](em-getellipsismode.md)
</dt> <dt>

[<span data-ttu-id="c7bf6-136">**\_GETELLIPSISSTATE em**</span><span class="sxs-lookup"><span data-stu-id="c7bf6-136">**EM\_GETELLIPSISSTATE**</span></span>](em-getellipsisstate.md)
</dt> </dl>

 

 





