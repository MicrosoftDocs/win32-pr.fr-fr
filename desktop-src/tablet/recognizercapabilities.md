---
description: Spécifie les attributs d’un IInkAnalysisRecognizer.
ms.assetid: e9577d83-0212-4f2f-88d7-e9153ec9fae5
title: Énumération RecognizerCapabilities (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkAnalysisRecognizerCapabilities
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: b2471e77fec02900804de831fc1197c071b9f566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519975"
---
# <a name="recognizercapabilities-enumeration"></a><span data-ttu-id="e5615-103">Énumération RecognizerCapabilities</span><span class="sxs-lookup"><span data-stu-id="e5615-103">RecognizerCapabilities enumeration</span></span>

<span data-ttu-id="e5615-104">Spécifie les attributs d’un [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="e5615-104">Specifies the attributes of an [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e5615-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5615-105">Syntax</span></span>


```C++
typedef enum RecognizerCapabilities { 
  RC_None                            = 0,
  RC_DoNotCare                       = 0x1,
  RC_Object                          = 0x2,
  RC_FreeInput                       = 0x4,
  RC_LinedInput                      = 0x8,
  RC_BoxedInput                      = 0x10,
  RC_CharacterAutoCompletionInput    = 0x20,
  RC_RightAndDown                    = 0x40,
  RC_LeftAndDown                     = 0x80,
  RC_DownAndLeft                     = 0x100,
  RC_DownAndRight                    = 0x200,
  RC_ArbitraryAngle                  = 0x400,
  RC_Lattice                         = 0x800,
  RC_AdviseInkChange                 = 0x1000,
  RC_StrokeReorder                   = 0x2000,
  RC_Personalizable                  = 0x4000,
  RC_PrefersArbitraryAngle           = 0x8000,
  RC_PrefersParagraphBreaking        = 0x10000,
  RC_PrefersSegmentationRecognition  = 0x20000
} InkAnalysisRecognizerCapabilities;
```



## <a name="constants"></a><span data-ttu-id="e5615-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="e5615-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e5615-107"><span id="RC_None"></span><span id="rc_none"></span><span id="RC_NONE"></span>**RC \_ aucun**</span><span class="sxs-lookup"><span data-stu-id="e5615-107"><span id="RC_None"></span><span id="rc_none"></span><span id="RC_NONE"></span>**RC\_None**</span></span>
</dt> <dd>

<span data-ttu-id="e5615-108">Aucune fonctionnalité n’est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e5615-108">No capabilities specified.</span></span>

</dd> <dt>

<span data-ttu-id="e5615-109"><span id="RC_DoNotCare"></span><span id="rc_donotcare"></span><span id="RC_DONOTCARE"></span>**RC \_ DoNotCare**</span><span class="sxs-lookup"><span data-stu-id="e5615-109"><span id="RC_DoNotCare"></span><span id="rc_donotcare"></span><span id="RC_DONOTCARE"></span>**RC\_DoNotCare**</span></span>
</dt> <dd>

<span data-ttu-id="e5615-110">Ignore tous les autres indicateurs définis.</span><span class="sxs-lookup"><span data-stu-id="e5615-110">Ignores all other flags that are set.</span></span>

</dd> <dt>

<span data-ttu-id="e5615-111"><span id="RC_Object"></span><span id="rc_object"></span><span id="RC_OBJECT"></span>**\_Objet RC**</span><span class="sxs-lookup"><span data-stu-id="e5615-111"><span id="RC_Object"></span><span id="rc_object"></span><span id="RC_OBJECT"></span>**RC\_Object**</span></span>
</dt> <dd>

<span data-ttu-id="e5615-112">Prend en charge la reconnaissance d’objets ; Sinon, reconnaît uniquement le texte.</span><span class="sxs-lookup"><span data-stu-id="e5615-112">Supports object recognition; otherwise, recognizes only text.</span></span>

</dd> <dt>

<span data-ttu-id="e5615-113"><span id="RC_FreeInput"></span><span id="rc_freeinput"></span><span id="RC_FREEINPUT"></span>**RC \_ FreeInput**</span><span class="sxs-lookup"><span data-stu-id="e5615-113"><span id="RC_FreeInput"></span><span id="rc_freeinput"></span><span id="RC_FREEINPUT"></span>**RC\_FreeInput**</span></span>
</dt> <dd>

<span data-ttu-id="e5615-114">Prend en charge l’entrée gratuite, où l’encre est entrée sans utiliser de guide de reconnaissance, tel qu’une ligne ou une zone.</span><span class="sxs-lookup"><span data-stu-id="e5615-114">Supports free input, where ink is entered without the use of a recognition guide, such as a line or a box.</span></span>

</dd> <dt>

<span data-ttu-id="e5615-115"><span id="RC_LinedInput"></span><span id="rc_linedinput"></span><span id="RC_LINEDINPUT"></span>**RC \_ LinedInput**</span><span class="sxs-lookup"><span data-stu-id="e5615-115"><span id="RC_LinedInput"></span><span id="rc_linedinput"></span><span id="RC_LINEDINPUT"></span>**RC\_LinedInput**</span></span>
</dt> <dd>

<span data-ttu-id="e5615-116">Prend en charge l’entrée en ligne, qui est semblable à l’écriture sur le papier en courbes.</span><span class="sxs-lookup"><span data-stu-id="e5615-116">Supports lined input, which is similar to writing on lined paper.</span></span>

</dd> <dt>

<span data-ttu-id="e5615-117"><span id="RC_BoxedInput"></span><span id="rc_boxedinput"></span><span id="RC_BOXEDINPUT"></span>**RC \_ BoxedInput**</span><span class="sxs-lookup"><span data-stu-id="e5615-117"><span id="RC_BoxedInput"></span><span id="rc_boxedinput"></span><span id="RC_BOXEDINPUT"></span>**RC\_BoxedInput**</span></span>
</dt> <dd>

<span data-ttu-id="e5615-118">Prend en charge les entrées boxed, où chaque caractère ou mot est entré dans une zone.</span><span class="sxs-lookup"><span data-stu-id="e5615-118">Supports boxed input, where each character or word is entered in a box.</span></span>

</dd> <dt>

<span data-ttu-id="e5615-119"><span id="RC_CharacterAutoCompletionInput"></span><span id="rc_characterautocompletioninput"></span><span id="RC_CHARACTERAUTOCOMPLETIONINPUT"></span>**RC \_ CharacterAutoCompletionInput**</span><span class="sxs-lookup"><span data-stu-id="e5615-119"><span id="RC_CharacterAutoCompletionInput"></span><span id="rc_characterautocompletioninput"></span><span id="RC_CHARACTERAUTOCOMPLETIONINPUT"></span>**RC\_CharacterAutoCompletionInput**</span></span>
</dt> <dd>

<span data-ttu-id="e5615-120">Prend en charge la saisie semi-automatique de caractères.</span><span class="sxs-lookup"><span data-stu-id="e5615-120">Supports character Autocomplete.</span></span> <span data-ttu-id="e5615-121">Les détecteurs qui prennent en charge la saisie semi-automatique des caractères nécessitent une entrée boxed.</span><span class="sxs-lookup"><span data-stu-id="e5615-121">Recognizers that support character Autocomplete require boxed input.</span></span>

</dd> <dt>

<span data-ttu-id="e5615-122"><span id="RC_RightAndDown"></span><span id="rc_rightanddown"></span><span id="RC_RIGHTANDDOWN"></span>**RC \_ RightAndDown**</span><span class="sxs-lookup"><span data-stu-id="e5615-122"><span id="RC_RightAndDown"></span><span id="rc_rightanddown"></span><span id="RC_RIGHTANDDOWN"></span>**RC\_RightAndDown**</span></span>
</dt> <dd>

<span data-ttu-id="e5615-123">Prend en charge les entrées d’écriture manuscrite dans l’ordre de droite et de baisse, par exemple dans les langues occidentales et les langues d’Extrême-Orient.</span><span class="sxs-lookup"><span data-stu-id="e5615-123">Supports handwriting input in right and down order, such as in western languages and some East Asian languages.</span></span>

</dd> <dt>

<span data-ttu-id="e5615-124"><span id="RC_LeftAndDown"></span><span id="rc_leftanddown"></span><span id="RC_LEFTANDDOWN"></span>**RC \_ LeftAndDown**</span><span class="sxs-lookup"><span data-stu-id="e5615-124"><span id="RC_LeftAndDown"></span><span id="rc_leftanddown"></span><span id="RC_LEFTANDDOWN"></span>**RC\_LeftAndDown**</span></span>
</dt> <dd>

<span data-ttu-id="e5615-125">Prend en charge l’entrée manuscrite dans l’ordre de gauche et de droite, comme dans les langues hébreu et arabe.</span><span class="sxs-lookup"><span data-stu-id="e5615-125">Supports handwriting input in left and down order, such as in Hebrew and Arabic languages.</span></span>

</dd> <dt>

<span data-ttu-id="e5615-126"><span id="RC_DownAndLeft"></span><span id="rc_downandleft"></span><span id="RC_DOWNANDLEFT"></span>**RC \_ DownAndLeft**</span><span class="sxs-lookup"><span data-stu-id="e5615-126"><span id="RC_DownAndLeft"></span><span id="rc_downandleft"></span><span id="RC_DOWNANDLEFT"></span>**RC\_DownAndLeft**</span></span>
</dt> <dd>

<span data-ttu-id="e5615-127">Prend en charge l’entrée de l’écriture manuscrite dans le sens le plus à gauche, par exemple dans certaines langues d’Extrême-Orient.</span><span class="sxs-lookup"><span data-stu-id="e5615-127">Supports handwriting input in down and left order, such as in some East Asian languages.</span></span>

</dd> <dt>

<span data-ttu-id="e5615-128"><span id="RC_DownAndRight"></span><span id="rc_downandright"></span><span id="RC_DOWNANDRIGHT"></span>**RC \_ DownAndRight**</span><span class="sxs-lookup"><span data-stu-id="e5615-128"><span id="RC_DownAndRight"></span><span id="rc_downandright"></span><span id="RC_DOWNANDRIGHT"></span>**RC\_DownAndRight**</span></span>
</dt> <dd>

<span data-ttu-id="e5615-129">Prend en charge l’entrée d’écriture manuscrite dans le sens le plus approprié, par exemple dans certaines langues d’Extrême-Orient.</span><span class="sxs-lookup"><span data-stu-id="e5615-129">Supports handwriting input in down and right order, such as in some East Asian languages.</span></span>

</dd> <dt>

<span data-ttu-id="e5615-130"><span id="RC_ArbitraryAngle"></span><span id="rc_arbitraryangle"></span><span id="RC_ARBITRARYANGLE"></span>**RC \_ ArbitraryAngle**</span><span class="sxs-lookup"><span data-stu-id="e5615-130"><span id="RC_ArbitraryAngle"></span><span id="rc_arbitraryangle"></span><span id="RC_ARBITRARYANGLE"></span>**RC\_ArbitraryAngle**</span></span>
</dt> <dd>

<span data-ttu-id="e5615-131">Prend en charge le texte écrit à des angles arbitraires.</span><span class="sxs-lookup"><span data-stu-id="e5615-131">Supports text written at arbitrary angles.</span></span>

</dd> <dt>

<span data-ttu-id="e5615-132"><span id="RC_Lattice"></span><span id="rc_lattice"></span><span id="RC_LATTICE"></span>**\_Treillis RC**</span><span class="sxs-lookup"><span data-stu-id="e5615-132"><span id="RC_Lattice"></span><span id="rc_lattice"></span><span id="RC_LATTICE"></span>**RC\_Lattice**</span></span>
</dt> <dd>

<span data-ttu-id="e5615-133">Prend en charge le retour d’un treillis comme alternative à une chaîne pour les résultats de reconnaissance de l’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="e5615-133">Supports returning a lattice as an alternative a string for handwriting recognition results.</span></span>

</dd> <dt>

<span data-ttu-id="e5615-134"><span id="RC_AdviseInkChange"></span><span id="rc_adviseinkchange"></span><span id="RC_ADVISEINKCHANGE"></span>**RC \_ AdviseInkChange**</span><span class="sxs-lookup"><span data-stu-id="e5615-134"><span id="RC_AdviseInkChange"></span><span id="rc_adviseinkchange"></span><span id="RC_ADVISEINKCHANGE"></span>**RC\_AdviseInkChange**</span></span>
</dt> <dd>

<span data-ttu-id="e5615-135">Prend en charge l’interruption de la reconnaissance en arrière-plan, par exemple lorsque l’encre a changé.</span><span class="sxs-lookup"><span data-stu-id="e5615-135">Supports interrupting background recognition, such as when the ink has changed.</span></span>

</dd> <dt>

<span data-ttu-id="e5615-136"><span id="RC_StrokeReorder"></span><span id="rc_strokereorder"></span><span id="RC_STROKEREORDER"></span>**RC \_ StrokeReorder**</span><span class="sxs-lookup"><span data-stu-id="e5615-136"><span id="RC_StrokeReorder"></span><span id="rc_strokereorder"></span><span id="RC_STROKEREORDER"></span>**RC\_StrokeReorder**</span></span>
</dt> <dd>

<span data-ttu-id="e5615-137">Prend en charge l’ordre des traits, l’spatial et le temporal, est géré dans le cadre de l’opération de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="e5615-137">Supports that stroke order, spatial and temporal, is handled as part of the recognition operation.</span></span> <span data-ttu-id="e5615-138">[**IInkAnalyzer**](iinkanalyzer.md) ne réorganise pas les traits avant l’envoi de l’encre au [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="e5615-138">The [**IInkAnalyzer**](iinkanalyzer.md) does not reorder strokes before sending ink to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5615-139"><span id="RC_Personalizable"></span><span id="rc_personalizable"></span><span id="RC_PERSONALIZABLE"></span>**RC \_ personnalisable**</span><span class="sxs-lookup"><span data-stu-id="e5615-139"><span id="RC_Personalizable"></span><span id="rc_personalizable"></span><span id="RC_PERSONALIZABLE"></span>**RC\_Personalizable**</span></span>
</dt> <dd>

<span data-ttu-id="e5615-140">Prend en charge l’écriture manuscrite personnalisée, où le module de reconnaissance améliore la reconnaissance lorsqu’il est exposé à la même écriture manuscrite dans le temps.</span><span class="sxs-lookup"><span data-stu-id="e5615-140">Supports personalized handwriting, where the recognizer improves recognition when exposed to the same handwriting over time.</span></span>

</dd> <dt>

<span data-ttu-id="e5615-141"><span id="RC_PrefersArbitraryAngle"></span><span id="rc_prefersarbitraryangle"></span><span id="RC_PREFERSARBITRARYANGLE"></span>**RC \_ PrefersArbitraryAngle**</span><span class="sxs-lookup"><span data-stu-id="e5615-141"><span id="RC_PrefersArbitraryAngle"></span><span id="rc_prefersarbitraryangle"></span><span id="RC_PREFERSARBITRARYANGLE"></span>**RC\_PrefersArbitraryAngle**</span></span>
</dt> <dd>

<span data-ttu-id="e5615-142">Les [**IInkAnalyzer**](iinkanalyzer.md) n’ont pas besoin de faire pivoter l’écriture manuscrite vers l’orientation horizontale avant d’envoyer l’encre au [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="e5615-142">The [**IInkAnalyzer**](iinkanalyzer.md) need not rotate the handwriting to a horizontal orientation before sending the ink to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5615-143"><span id="RC_PrefersParagraphBreaking"></span><span id="rc_prefersparagraphbreaking"></span><span id="RC_PREFERSPARAGRAPHBREAKING"></span>**RC \_ PrefersParagraphBreaking**</span><span class="sxs-lookup"><span data-stu-id="e5615-143"><span id="RC_PrefersParagraphBreaking"></span><span id="rc_prefersparagraphbreaking"></span><span id="RC_PREFERSPARAGRAPHBREAKING"></span>**RC\_PrefersParagraphBreaking**</span></span>
</dt> <dd>

<span data-ttu-id="e5615-144">Le [**IInkAnalyzer**](iinkanalyzer.md) doit envoyer des paragraphes entiers d’encre au [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md), ce qui permet au **IInkAnalysisRecognizer** d’effectuer les sauts de ligne et de mot (ou caractère).</span><span class="sxs-lookup"><span data-stu-id="e5615-144">The [**IInkAnalyzer**](iinkanalyzer.md) should send entire paragraphs of ink to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md), allowing the **IInkAnalysisRecognizer** to do the line breaking and word (or character) breaking.</span></span>

</dd> <dt>

<span data-ttu-id="e5615-145"><span id="RC_PrefersSegmentationRecognition"></span><span id="rc_preferssegmentationrecognition"></span><span id="RC_PREFERSSEGMENTATIONRECOGNITION"></span>**RC \_ PrefersSegmentationRecognition**</span><span class="sxs-lookup"><span data-stu-id="e5615-145"><span id="RC_PrefersSegmentationRecognition"></span><span id="rc_preferssegmentationrecognition"></span><span id="RC_PREFERSSEGMENTATIONRECOGNITION"></span>**RC\_PrefersSegmentationRecognition**</span></span>
</dt> <dd>

<span data-ttu-id="e5615-146">Reconnaît un seul mot ou caractère par opération de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="e5615-146">Recognizes only one word or character per recognition operation.</span></span> <span data-ttu-id="e5615-147">Le [**IInkAnalyzer**](iinkanalyzer.md) effectue la segmentation de l’écriture manuscrite et envoie un seul segment à la fois au [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="e5615-147">The [**IInkAnalyzer**](iinkanalyzer.md) performs segmentation on the handwriting and sends only one segment at a time to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5615-148">Notes</span><span class="sxs-lookup"><span data-stu-id="e5615-148">Remarks</span></span>

<span data-ttu-id="e5615-149">Cette énumération permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="e5615-149">This enumeration allows a bitwise combination of its member values.</span></span> <span data-ttu-id="e5615-150">Utilisez cette énumération pour rechercher un module de reconnaissance d’encre installée qui prend en charge les attributs dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="e5615-150">Use this enumeration to find an installed ink recognizer that supports the attributes you need.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5615-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e5615-151">Requirements</span></span>



| <span data-ttu-id="e5615-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e5615-152">Requirement</span></span> | <span data-ttu-id="e5615-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5615-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5615-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5615-154">Minimum supported client</span></span><br/> | <span data-ttu-id="e5615-155">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e5615-155">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e5615-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5615-156">Minimum supported server</span></span><br/> | <span data-ttu-id="e5615-157">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5615-157">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e5615-158">En-tête</span><span class="sxs-lookup"><span data-stu-id="e5615-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5615-159"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e5615-159"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5615-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5615-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5615-161">**IInkAnalysisRecognizer :: GetCapabilities**</span><span class="sxs-lookup"><span data-stu-id="e5615-161">**IInkAnalysisRecognizer::GetCapabilities**</span></span>](iinkanalysisrecognizer-getcapabilities.md)
</dt> <dt>

[<span data-ttu-id="e5615-162">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="e5615-162">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




