---
title: Message SB_GETTEXT (commctrl. h)
description: Récupère le texte à partir de la partie spécifiée d’une fenêtre d’État.
ms.assetid: 95bef9ff-04e5-431e-bc79-06d8498fcab0
keywords:
- SB_GETTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- SB_GETTEXT
- SB_GETTEXTA
- SB_GETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e90b132c3f934188aea36afd86d53ab8f75bdadb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033097"
---
# <a name="sb_gettext-message"></a><span data-ttu-id="f71c9-104">\_Message SB GETTEXT</span><span class="sxs-lookup"><span data-stu-id="f71c9-104">SB\_GETTEXT message</span></span>

<span data-ttu-id="f71c9-105">Récupère le texte à partir de la partie spécifiée d’une fenêtre d’État.</span><span class="sxs-lookup"><span data-stu-id="f71c9-105">Retrieves the text from the specified part of a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="f71c9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f71c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f71c9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f71c9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f71c9-108">Index de base zéro du composant à partir duquel récupérer du texte.</span><span class="sxs-lookup"><span data-stu-id="f71c9-108">Zero-based index of the part from which to retrieve text.</span></span>

</dd> <dt>

<span data-ttu-id="f71c9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f71c9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f71c9-110">Pointeur vers la mémoire tampon qui reçoit le texte sous la forme d’une chaîne terminée par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="f71c9-110">Pointer to the buffer that receives the text as a null-terminated string.</span></span> <span data-ttu-id="f71c9-111">Utilisez le message [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) pour déterminer la taille requise pour la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="f71c9-111">Use the [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) message to determine the required size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f71c9-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f71c9-112">Return value</span></span>

<span data-ttu-id="f71c9-113">Retourne une valeur 32 bits qui se compose de valeurs 2 16 bits.</span><span class="sxs-lookup"><span data-stu-id="f71c9-113">Returns a 32-bit value that consists of two 16-bit values.</span></span> <span data-ttu-id="f71c9-114">Le mot de poids faible spécifie la longueur, en caractères, du texte.</span><span class="sxs-lookup"><span data-stu-id="f71c9-114">The low word specifies the length, in characters, of the text.</span></span> <span data-ttu-id="f71c9-115">Le mot de poids fort spécifie le type d’opération utilisé pour dessiner le texte.</span><span class="sxs-lookup"><span data-stu-id="f71c9-115">The high word specifies the type of operation used to draw the text.</span></span> <span data-ttu-id="f71c9-116">Le type peut prendre l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f71c9-116">The type can be one of the following values.</span></span>



| <span data-ttu-id="f71c9-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f71c9-117">Return code</span></span>                                                                                    | <span data-ttu-id="f71c9-118">Description</span><span class="sxs-lookup"><span data-stu-id="f71c9-118">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f71c9-119"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="f71c9-119"><dt>**0**</dt></span></span> </dl>               | <span data-ttu-id="f71c9-120">Le texte est dessiné avec une bordure qui apparaît plus bas que le plan de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f71c9-120">The text is drawn with a border to appear lower than the plane of the window.</span></span><br/>  |
| <dl> <span data-ttu-id="f71c9-121"><dt>**SBT \_ NOfrontières**</dt></span><span class="sxs-lookup"><span data-stu-id="f71c9-121"><dt>**SBT\_NOBORDERS**</dt></span></span> </dl>  | <span data-ttu-id="f71c9-122">Le texte est dessiné sans bordures.</span><span class="sxs-lookup"><span data-stu-id="f71c9-122">The text is drawn without borders.</span></span><br/>                                             |
| <dl> <span data-ttu-id="f71c9-123"><dt>**SBT \_ fenêtre indépendante**</dt></span><span class="sxs-lookup"><span data-stu-id="f71c9-123"><dt>**SBT\_POPOUT**</dt></span></span> </dl>     | <span data-ttu-id="f71c9-124">Le texte est dessiné avec une bordure qui doit apparaître plus haut que le plan de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f71c9-124">The text is drawn with a border to appear higher than the plane of the window.</span></span><br/> |
| <dl> <span data-ttu-id="f71c9-125"><dt>**SBT \_ RTLREADING**</dt></span><span class="sxs-lookup"><span data-stu-id="f71c9-125"><dt>**SBT\_RTLREADING**</dt></span></span> </dl> | <span data-ttu-id="f71c9-126">Le texte s’affiche dans la direction opposée du texte dans la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="f71c9-126">The text displays in the opposite direction of the text in the parent window.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="f71c9-127">Notes</span><span class="sxs-lookup"><span data-stu-id="f71c9-127">Remarks</span></span>

<span data-ttu-id="f71c9-128">**Avertissement de sécurité :** L’utilisation incorrecte de ce message peut compromettre la sécurité de votre programme.</span><span class="sxs-lookup"><span data-stu-id="f71c9-128">**Security Warning:** Using this message incorrectly can compromise the security of your program.</span></span> <span data-ttu-id="f71c9-129">Ce message n’offre aucun moyen de connaître la taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="f71c9-129">This message does not provide a way for you to know the size of the buffer.</span></span> <span data-ttu-id="f71c9-130">Si vous utilisez ce message, appelez d’abord [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) pour obtenir le nombre de caractères requis, puis appelez le message pour récupérer la chaîne.</span><span class="sxs-lookup"><span data-stu-id="f71c9-130">If you use this message, first call [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) to get the number of characters that are required and then call the message to retrieve the string.</span></span> <span data-ttu-id="f71c9-131">Si vous attendez avant d’appeler SB, le texte pourrait changer, invalidant ainsi la valeur de retour de **SB \_ GETTEXTLENGTH**. **\_**</span><span class="sxs-lookup"><span data-stu-id="f71c9-131">If you wait before calling **SB\_GETTEXT** the text could change, thereby invalidating the return value of **SB\_GETTEXTLENGTH**.</span></span> <span data-ttu-id="f71c9-132">Vous devez examiner les [considérations relatives à la sécurité : contrôles Microsoft Windows](sec-comctls.md) avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="f71c9-132">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="f71c9-133">Ce message retourne un maximum de 65 535 caractères.</span><span class="sxs-lookup"><span data-stu-id="f71c9-133">This message returns a maximum of 65,535 characters.</span></span> <span data-ttu-id="f71c9-134">Si la chaîne de texte est plus longue, elle est tronquée.</span><span class="sxs-lookup"><span data-stu-id="f71c9-134">If the text string is longer than that, it is truncated.</span></span>

<span data-ttu-id="f71c9-135">Si le texte a le \_ type de dessin SBT OwnerDraw, ce message retourne la valeur 32 bits associée au texte au lieu de la longueur et du type d’opération.</span><span class="sxs-lookup"><span data-stu-id="f71c9-135">If the text has the SBT\_OWNERDRAW drawing type, this message returns the 32-bit value associated with the text instead of the length and operation type.</span></span>

<span data-ttu-id="f71c9-136">Les fenêtres normales affichent le texte de gauche à droite (LTR).</span><span class="sxs-lookup"><span data-stu-id="f71c9-136">Normal windows display text left-to-right (LTR).</span></span> <span data-ttu-id="f71c9-137">Les fenêtres peuvent être *mises en miroir* pour afficher des langues telles que l’hébreu ou l’arabe, qui sont lues de droite à gauche (RTL).</span><span class="sxs-lookup"><span data-stu-id="f71c9-137">Windows can be *mirrored* to display languages such as Hebrew or Arabic that read right-to-left (RTL).</span></span> <span data-ttu-id="f71c9-138">Si SBT \_ RTLREADING est défini, la chaîne *lParam* lit dans le sens opposé du texte dans la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="f71c9-138">If SBT\_RTLREADING is set, the *lParam* string reads in the opposite direction from the text in the parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="f71c9-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f71c9-139">Requirements</span></span>



| <span data-ttu-id="f71c9-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f71c9-140">Requirement</span></span> | <span data-ttu-id="f71c9-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="f71c9-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f71c9-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f71c9-142">Minimum supported client</span></span><br/> | <span data-ttu-id="f71c9-143">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f71c9-143">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f71c9-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f71c9-144">Minimum supported server</span></span><br/> | <span data-ttu-id="f71c9-145">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f71c9-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f71c9-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="f71c9-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="f71c9-147"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f71c9-147"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f71c9-148">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="f71c9-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f71c9-149">**SB \_ GETTEXTW** (Unicode) et **SB \_ gettexta** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f71c9-149">**SB\_GETTEXTW** (Unicode) and **SB\_GETTEXTA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="f71c9-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f71c9-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f71c9-151">**unisettext SB \_**</span><span class="sxs-lookup"><span data-stu-id="f71c9-151">**SB\_SETTEXT**</span></span>](sb-settext.md)
</dt> </dl>

 

 





