---
title: Message SB_GETTEXTLENGTH (commctrl. h)
description: Récupère la longueur, en caractères, du texte à partir de la partie spécifiée d’une fenêtre d’État.
ms.assetid: 2cd43106-dd43-499e-b595-760e9ededab5
keywords:
- SB_GETTEXTLENGTH les contrôles de message Windows
topic_type:
- apiref
api_name:
- SB_GETTEXTLENGTH
- SB_GETTEXTLENGTHA
- SB_GETTEXTLENGTHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b08dd3b870c3c59e5aafbeb9d53baef3816a726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942548"
---
# <a name="sb_gettextlength-message"></a><span data-ttu-id="bfcb1-104">\_Message SB GETTEXTLENGTH</span><span class="sxs-lookup"><span data-stu-id="bfcb1-104">SB\_GETTEXTLENGTH message</span></span>

<span data-ttu-id="bfcb1-105">Récupère la longueur, en caractères, du texte à partir de la partie spécifiée d’une fenêtre d’État.</span><span class="sxs-lookup"><span data-stu-id="bfcb1-105">Retrieves the length, in characters, of the text from the specified part of a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="bfcb1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bfcb1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfcb1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bfcb1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bfcb1-108">Index de base zéro du composant à partir duquel récupérer du texte.</span><span class="sxs-lookup"><span data-stu-id="bfcb1-108">Zero-based index of the part from which to retrieve text.</span></span>

</dd> <dt>

<span data-ttu-id="bfcb1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bfcb1-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bfcb1-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="bfcb1-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfcb1-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bfcb1-111">Return value</span></span>

<span data-ttu-id="bfcb1-112">Retourne une valeur 32 bits qui se compose de valeurs 2 16 bits.</span><span class="sxs-lookup"><span data-stu-id="bfcb1-112">Returns a 32-bit value that consists of two 16-bit values.</span></span> <span data-ttu-id="bfcb1-113">Le mot de poids faible spécifie la longueur, en caractères, du texte.</span><span class="sxs-lookup"><span data-stu-id="bfcb1-113">The low word specifies the length, in characters, of the text.</span></span> <span data-ttu-id="bfcb1-114">Le mot de poids fort spécifie le type d’opération utilisé pour dessiner le texte.</span><span class="sxs-lookup"><span data-stu-id="bfcb1-114">The high word specifies the type of operation used to draw the text.</span></span> <span data-ttu-id="bfcb1-115">Le type peut prendre l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="bfcb1-115">The type can be one of the following values:</span></span>



| <span data-ttu-id="bfcb1-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="bfcb1-116">Return code</span></span>                                                                                    | <span data-ttu-id="bfcb1-117">Description</span><span class="sxs-lookup"><span data-stu-id="bfcb1-117">Description</span></span>                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bfcb1-118"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="bfcb1-118"><dt>**0**</dt></span></span> </dl>               | <span data-ttu-id="bfcb1-119">Le texte est dessiné avec une bordure qui apparaît plus bas que le plan de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="bfcb1-119">The text is drawn with a border to appear lower than the plane of the window.</span></span><br/>          |
| <dl> <span data-ttu-id="bfcb1-120"><dt>**SBT \_ NOfrontières**</dt></span><span class="sxs-lookup"><span data-stu-id="bfcb1-120"><dt>**SBT\_NOBORDERS**</dt></span></span> </dl>  | <span data-ttu-id="bfcb1-121">Le texte est dessiné sans bordures.</span><span class="sxs-lookup"><span data-stu-id="bfcb1-121">The text is drawn without borders.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="bfcb1-122"><dt>**SBT \_ OwnerDraw**</dt></span><span class="sxs-lookup"><span data-stu-id="bfcb1-122"><dt>**SBT\_OWNERDRAW**</dt></span></span> </dl>  | <span data-ttu-id="bfcb1-123">Le texte est dessiné par la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="bfcb1-123">The text is drawn by the parent window.</span></span><br/>                                                |
| <dl> <span data-ttu-id="bfcb1-124"><dt>**SBT \_ fenêtre indépendante**</dt></span><span class="sxs-lookup"><span data-stu-id="bfcb1-124"><dt>**SBT\_POPOUT**</dt></span></span> </dl>     | <span data-ttu-id="bfcb1-125">Le texte est dessiné avec une bordure qui doit apparaître plus haut que le plan de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="bfcb1-125">The text is drawn with a border to appear higher than the plane of the window.</span></span><br/>         |
| <dl> <span data-ttu-id="bfcb1-126"><dt>**SBT \_ RTLREADING**</dt></span><span class="sxs-lookup"><span data-stu-id="bfcb1-126"><dt>**SBT\_RTLREADING**</dt></span></span> </dl> | <span data-ttu-id="bfcb1-127">Le texte s’affiche dans le sens inverse du texte de la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="bfcb1-127">The text will be displayed in the opposite direction to the text in the parent window.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bfcb1-128">Notes</span><span class="sxs-lookup"><span data-stu-id="bfcb1-128">Remarks</span></span>

<span data-ttu-id="bfcb1-129">Les fenêtres normales affichent le texte de gauche à droite (LTR).</span><span class="sxs-lookup"><span data-stu-id="bfcb1-129">Normal windows display text left-to-right (LTR).</span></span> <span data-ttu-id="bfcb1-130">Les fenêtres peuvent être *mises en miroir* pour afficher des langues telles que l’hébreu ou l’arabe, qui sont lues de droite à gauche (RTL).</span><span class="sxs-lookup"><span data-stu-id="bfcb1-130">Windows can be *mirrored* to display languages such as Hebrew or Arabic that read right-to-left (RTL).</span></span> <span data-ttu-id="bfcb1-131">Si SBT \_ RTLREADING est défini, le texte de la fenêtre d’état spécifié est lu dans le sens inverse à partir du texte de la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="bfcb1-131">If SBT\_RTLREADING is set, the specified status window text will read in the opposite direction from the text in the parent window.</span></span>

<span data-ttu-id="bfcb1-132">Ce message retourne une longueur de chaîne maximale de 65 535 caractères.</span><span class="sxs-lookup"><span data-stu-id="bfcb1-132">This message returns a maximum string length of 65,535 characters.</span></span> <span data-ttu-id="bfcb1-133">Si la chaîne de texte réelle est plus longue, le message [**SB \_ GETTEXT**](sb-gettext.md) le tronque.</span><span class="sxs-lookup"><span data-stu-id="bfcb1-133">If the actual text string is longer than that, the [**SB\_GETTEXT**](sb-gettext.md) message truncates it.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfcb1-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bfcb1-134">Requirements</span></span>



| <span data-ttu-id="bfcb1-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bfcb1-135">Requirement</span></span> | <span data-ttu-id="bfcb1-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfcb1-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bfcb1-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfcb1-137">Minimum supported client</span></span><br/> | <span data-ttu-id="bfcb1-138">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bfcb1-138">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bfcb1-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfcb1-139">Minimum supported server</span></span><br/> | <span data-ttu-id="bfcb1-140">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bfcb1-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bfcb1-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="bfcb1-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfcb1-142"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfcb1-142"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="bfcb1-143">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="bfcb1-143">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bfcb1-144">**SB \_ GETTEXTLENGTHW** (Unicode) et **SB \_ GETTEXTLENGTHA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bfcb1-144">**SB\_GETTEXTLENGTHW** (Unicode) and **SB\_GETTEXTLENGTHA** (ANSI)</span></span><br/>         |



 

 





