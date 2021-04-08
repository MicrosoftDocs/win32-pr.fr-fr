---
title: Message EM_GETEDITSTYLEEX (RichEdit. h)
description: Récupère les indicateurs de style de modification étendus actuels.
ms.assetid: 3E81F7BB-404D-4465-982A-3CF6FD9359DA
keywords:
- EM_GETEDITSTYLEEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETEDITSTYLEEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb4077abaedd0c5ec720603d6b23e77950fd5307
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843685"
---
# <a name="em_geteditstyleex-message"></a><span data-ttu-id="5f31a-104">\_Message GETEDITSTYLEEX em</span><span class="sxs-lookup"><span data-stu-id="5f31a-104">EM\_GETEDITSTYLEEX message</span></span>

<span data-ttu-id="5f31a-105">Récupère les indicateurs de style de modification étendus actuels.</span><span class="sxs-lookup"><span data-stu-id="5f31a-105">Retrieves the current extended edit style flags.</span></span>


```C++
#define EM_GETEDITSTYLEEX       (WM_USER + 276)
```



## <a name="parameters"></a><span data-ttu-id="5f31a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f31a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f31a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5f31a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f31a-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="5f31a-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5f31a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f31a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f31a-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="5f31a-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f31a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5f31a-111">Return value</span></span>

<span data-ttu-id="5f31a-112">Retourne les indicateurs de style de modification étendus, qui peuvent inclure une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="5f31a-112">Returns the extended edit style flags, which can include one or more of the following values.</span></span>



| <span data-ttu-id="5f31a-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5f31a-113">Return code</span></span>                                                                                                | <span data-ttu-id="5f31a-114">Description</span><span class="sxs-lookup"><span data-stu-id="5f31a-114">Description</span></span>                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5f31a-115"><dt>**SES \_ ex \_ HANDLEFRIENDLYURL**</dt></span><span class="sxs-lookup"><span data-stu-id="5f31a-115"><dt>**SES\_EX\_HANDLEFRIENDLYURL**</dt></span></span> </dl>  | <span data-ttu-id="5f31a-116">Affichez des liens de nom convivial avec la même couleur de texte et le soulignement que les liens automatiques, à condition que la mise en forme temporaire n’utilise pas ou utilise la couleur automatique de texte (valeur par défaut : 0).</span><span class="sxs-lookup"><span data-stu-id="5f31a-116">Display friendly name links with the same text color and underlining as automatic links, provided that temporary formatting isn t used or uses text autocolor (default: 0).</span></span><br/>                                                                       |
| <dl> <span data-ttu-id="5f31a-117"><dt>**SES \_ par \_ multipoint**</dt></span><span class="sxs-lookup"><span data-stu-id="5f31a-117"><dt>**SES\_EX\_MULTITOUCH**</dt></span></span> </dl>         | <span data-ttu-id="5f31a-118">Activez la prise en charge tactile en Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="5f31a-118">Enable touch support in Rich Edit.</span></span> <span data-ttu-id="5f31a-119">Cela comprend la sélection, le positionnement du signe insertion et l’appel du menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="5f31a-119">This includes selection, caret placement, and context-menu invocation.</span></span> <span data-ttu-id="5f31a-120">Lorsque cet indicateur n’est pas défini, la fonction tactile est émulée par les commandes de la souris, qui ne prennent pas en compte les spécificités en mode tactile (valeur par défaut : 0).</span><span class="sxs-lookup"><span data-stu-id="5f31a-120">When this flag is not set, touch is emulated by mouse commands, which do not take touch-mode specifics into account (default: 0).</span></span> <br/>      |
| <dl> <span data-ttu-id="5f31a-121"><dt>**SES \_ ex \_ NOACETATESELECTION**</dt></span><span class="sxs-lookup"><span data-stu-id="5f31a-121"><dt>**SES\_EX\_NOACETATESELECTION**</dt></span></span> </dl> | <span data-ttu-id="5f31a-122">Affichez le texte sélectionné à l’aide de la sélection Windows classique texte et couleurs d’arrière-plan au lieu de couleur d’acétate d’arrière-plan (par défaut : 0).</span><span class="sxs-lookup"><span data-stu-id="5f31a-122">Display selected text using classic Windows selection text and background colors instead of background acetate color (default: 0).</span></span> <br/>                                                                                                               |
| <dl> <span data-ttu-id="5f31a-123"><dt>**SES \_ ex \_ maths**</dt></span><span class="sxs-lookup"><span data-stu-id="5f31a-123"><dt>**SES\_EX\_NOMATH**</dt></span></span> </dl>             | <span data-ttu-id="5f31a-124">Désactivez l’insertion de zones mathématiques (valeur par défaut : 1).</span><span class="sxs-lookup"><span data-stu-id="5f31a-124">Disable insertion of math zones (default: 1).</span></span> <span data-ttu-id="5f31a-125">Pour activer la modification et l’affichage des mathématiques, envoyez le message [**em \_ SETEDITSTYLEEX**](em-seteditstyleex.md) avec *wParam* défini sur 0, et *lParam* défini sur **ses \_ ex \_ maths**.</span><span class="sxs-lookup"><span data-stu-id="5f31a-125">To enable math editing and display, send the [**EM\_SETEDITSTYLEEX**](em-seteditstyleex.md) message with *wParam* set to 0, and *lParam* set to **SES\_EX\_NOMATH**.</span></span> <br/>                              |
| <dl> <span data-ttu-id="5f31a-126"><dt>**SES \_ ex \_ table**</dt></span><span class="sxs-lookup"><span data-stu-id="5f31a-126"><dt>**SES\_EX\_NOTABLE**</dt></span></span> </dl>            | <span data-ttu-id="5f31a-127">Désactive l’insertion de tables.</span><span class="sxs-lookup"><span data-stu-id="5f31a-127">Disable insertion of tables.</span></span> <span data-ttu-id="5f31a-128">Le message [**em \_ INSERTTABLE**](em-inserttable.md) retourne **E \_ Fail** et les tables RTF sont ignorées (valeur par défaut : 0).</span><span class="sxs-lookup"><span data-stu-id="5f31a-128">The [**EM\_INSERTTABLE**](em-inserttable.md) message returns **E\_FAIL** and RTF tables are skipped (default: 0).</span></span> <br/>                                                                                                  |
| <dl> <span data-ttu-id="5f31a-129"><dt>**SES \_ ex \_ USESINGLELINE**</dt></span><span class="sxs-lookup"><span data-stu-id="5f31a-129"><dt>**SES\_EX\_USESINGLELINE**</dt></span></span> </dl>      | <span data-ttu-id="5f31a-130">Permet à un contrôle multiligne d’agir comme un contrôle sur une seule ligne, avec la possibilité de faire défiler verticalement lorsque la hauteur d’une seule ligne est supérieure à la hauteur de la fenêtre (valeur par défaut : 0).</span><span class="sxs-lookup"><span data-stu-id="5f31a-130">Enable a multiline control to act like a single-line control with the ability to scroll vertically when the single-line height is greater than the window height (default: 0).</span></span> <br/>                                                                   |
| <dl> <span data-ttu-id="5f31a-131"><dt>**\_HIDETEMPFORMAT ses**</dt></span><span class="sxs-lookup"><span data-stu-id="5f31a-131"><dt>**SES\_HIDETEMPFORMAT**</dt></span></span> </dl>         | <span data-ttu-id="5f31a-132">Masquer la mise en forme temporaire qui est créée quand [**ITextFont. Reset**](/windows/desktop/api/Tom/nf-tom-itextfont-reset) est appelé avec **tomApplyTmp**.</span><span class="sxs-lookup"><span data-stu-id="5f31a-132">Hide temporary formatting that is created when [**ITextFont.Reset**](/windows/desktop/api/Tom/nf-tom-itextfont-reset) is called with **tomApplyTmp**.</span></span> <span data-ttu-id="5f31a-133">Par exemple, une telle mise en forme est utilisée par les vérificateurs d’orthographe pour afficher un soulignement ondulé sous des mots éventuellement mal orthographiés.</span><span class="sxs-lookup"><span data-stu-id="5f31a-133">For example, such formatting is used by spell checkers to display a squiggly underline under possibly misspelled words.</span></span><br/> |
| <dl> <span data-ttu-id="5f31a-134"><dt>**SES \_ ex \_ USEMOUSEWPARAM**</dt></span><span class="sxs-lookup"><span data-stu-id="5f31a-134"><dt>**SES\_EX\_USEMOUSEWPARAM**</dt></span></span> </dl>     | <span data-ttu-id="5f31a-135">Utilisez *wParam* lors du traitement du message [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) et n’appelez pas [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).</span><span class="sxs-lookup"><span data-stu-id="5f31a-135">Use *wParam* when handling the [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message and do not call [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).</span></span><br/>                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="5f31a-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f31a-136">Requirements</span></span>



| <span data-ttu-id="5f31a-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f31a-137">Requirement</span></span> | <span data-ttu-id="5f31a-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f31a-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f31a-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f31a-139">Minimum supported client</span></span><br/> | <span data-ttu-id="5f31a-140">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f31a-140">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="5f31a-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f31a-141">Minimum supported server</span></span><br/> | <span data-ttu-id="5f31a-142">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f31a-142">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5f31a-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="5f31a-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f31a-144"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f31a-144"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f31a-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f31a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f31a-146">**\_SETEDITSTYLEEX em**</span><span class="sxs-lookup"><span data-stu-id="5f31a-146">**EM\_SETEDITSTYLEEX**</span></span>](em-seteditstyleex.md)
</dt> </dl>

 

