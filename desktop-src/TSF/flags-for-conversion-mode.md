---
title: Indicateurs pour le mode de conversion (Ctffunc. h)
description: Les indicateurs suivants sont utilisés comme valeur de la \_ conversion de \_ INPUTMODE clavier de compartiment de GUID \_ \_ . Cela équivaut aux \_ valeurs CMODE IME pour imm32.
ms.assetid: 6e545af5-5fdb-49de-b24e-aaee82b51326
keywords:
- Indicateurs pour le mode de conversion Text Services Framework
topic_type:
- apiref
api_name:
- Flags for Conversion Mode
api_location:
- Ctffunc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 022712ff45f213992bf3d40bd0149959e4864faa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104122"
---
# <a name="flags-for-conversion-mode"></a><span data-ttu-id="96366-105">Indicateurs pour le mode de conversion</span><span class="sxs-lookup"><span data-stu-id="96366-105">Flags for Conversion Mode</span></span>

<span data-ttu-id="96366-106">Les indicateurs suivants sont utilisés comme valeur de la [ \_ conversion de \_ \_ INPUTMODE clavier \_ de compartiment de GUID](predefined-compartments.md).</span><span class="sxs-lookup"><span data-stu-id="96366-106">The following flags are used as a value of [GUID\_COMPARTMENT\_KEYBOARD\_INPUTMODE\_CONVERSION](predefined-compartments.md).</span></span> <span data-ttu-id="96366-107">Cela équivaut aux valeurs [ \_ CMODE IME](../intl/ime-conversion-mode-values.md) pour imm32.</span><span class="sxs-lookup"><span data-stu-id="96366-107">This is equivalent with [IME\_CMODE](../intl/ime-conversion-mode-values.md) values for IMM32.</span></span>



| <span data-ttu-id="96366-108">Indicateur</span><span class="sxs-lookup"><span data-stu-id="96366-108">Flag</span></span>                             | <span data-ttu-id="96366-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="96366-109">Value</span></span>  | <span data-ttu-id="96366-110">Description</span><span class="sxs-lookup"><span data-stu-id="96366-110">Description</span></span>                                                     |
|----------------------------------|--------|-----------------------------------------------------------------|
| <span data-ttu-id="96366-111">\_CONVERSIONMODE TF \_</span><span class="sxs-lookup"><span data-stu-id="96366-111">TF\_CONVERSIONMODE\_ALPHANUMERIC</span></span> | <span data-ttu-id="96366-112">0x0000</span><span class="sxs-lookup"><span data-stu-id="96366-112">0x0000</span></span> | <span data-ttu-id="96366-113">Affectez la valeur 1 à en mode alphanumérique.</span><span class="sxs-lookup"><span data-stu-id="96366-113">Set to 1 if ALPHANUMERIC mode.</span></span>                                  |
| <span data-ttu-id="96366-114">CONVERSIONMODE TF en \_ \_ mode natif</span><span class="sxs-lookup"><span data-stu-id="96366-114">TF\_CONVERSIONMODE\_NATIVE</span></span>       | <span data-ttu-id="96366-115">0x0001</span><span class="sxs-lookup"><span data-stu-id="96366-115">0x0001</span></span> | <span data-ttu-id="96366-116">Défini sur 1 en mode natif ; 0 si le mode est alphanumérique.</span><span class="sxs-lookup"><span data-stu-id="96366-116">Set to 1 if NATIVE mode; 0 if ALPHANUMERIC mode.</span></span>                |
| <span data-ttu-id="96366-117">TF \_ CONVERSIONMODE \_ Katakana</span><span class="sxs-lookup"><span data-stu-id="96366-117">TF\_CONVERSIONMODE\_KATAKANA</span></span>     | <span data-ttu-id="96366-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="96366-118">0x0002</span></span> | <span data-ttu-id="96366-119">Défini sur 1 si le mode KATAKANA ; 0 en mode HIRAGANA.</span><span class="sxs-lookup"><span data-stu-id="96366-119">Set to 1 if KATAKANA mode; 0 if HIRAGANA mode.</span></span>                  |
| <span data-ttu-id="96366-120">TF \_ CONVERSIONMODE \_ FULLSHAPE</span><span class="sxs-lookup"><span data-stu-id="96366-120">TF\_CONVERSIONMODE\_FULLSHAPE</span></span>    | <span data-ttu-id="96366-121">0x0008</span><span class="sxs-lookup"><span data-stu-id="96366-121">0x0008</span></span> | <span data-ttu-id="96366-122">Défini sur 1 en mode de forme complète ; 0 s’il s’agit du mode demi-forme.</span><span class="sxs-lookup"><span data-stu-id="96366-122">Set to 1 if full shape mode; 0 if half shape mode.</span></span>              |
| <span data-ttu-id="96366-123">TF \_ CONVERSIONMODE \_ roman</span><span class="sxs-lookup"><span data-stu-id="96366-123">TF\_CONVERSIONMODE\_ROMAN</span></span>        | <span data-ttu-id="96366-124">0x0010</span><span class="sxs-lookup"><span data-stu-id="96366-124">0x0010</span></span> | <span data-ttu-id="96366-125">Défini sur 1 pour empêcher le traitement des conversions par l’IME ; 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="96366-125">Set to 1 to prevent processing of conversions by IME; 0 if not.</span></span> |
| <span data-ttu-id="96366-126">TF \_ CONVERSIONMODE \_ CHARCODE</span><span class="sxs-lookup"><span data-stu-id="96366-126">TF\_CONVERSIONMODE\_CHARCODE</span></span>     | <span data-ttu-id="96366-127">0x0020</span><span class="sxs-lookup"><span data-stu-id="96366-127">0x0020</span></span> | <span data-ttu-id="96366-128">Défini sur 1 si le mode de saisie du code du caractère ; 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="96366-128">Set to 1 if character code input mode; 0 if not.</span></span>                |
| <span data-ttu-id="96366-129">TF \_ CONVERSIONMODE \_</span><span class="sxs-lookup"><span data-stu-id="96366-129">TF\_CONVERSIONMODE\_SOFTKEYBOARD</span></span> | <span data-ttu-id="96366-130">0x0080</span><span class="sxs-lookup"><span data-stu-id="96366-130">0x0080</span></span> | <span data-ttu-id="96366-131">Défini sur 1 si le mode de clavier logiciel est activé ; 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="96366-131">Set to 1 if Soft Keyboard mode; 0 if not.</span></span>                       |
| <span data-ttu-id="96366-132">TF \_ CONVERSIONMODE \_ noconversion</span><span class="sxs-lookup"><span data-stu-id="96366-132">TF\_CONVERSIONMODE\_NOCONVERSION</span></span> | <span data-ttu-id="96366-133">0x0100</span><span class="sxs-lookup"><span data-stu-id="96366-133">0x0100</span></span> | <span data-ttu-id="96366-134">Défini sur 1 pour empêcher le traitement des conversions par l’IME ; 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="96366-134">Set to 1 to prevent processing of conversions by IME; 0 if not.</span></span> |
| <span data-ttu-id="96366-135">\_symbole TF CONVERSIONMODE \_</span><span class="sxs-lookup"><span data-stu-id="96366-135">TF\_CONVERSIONMODE\_SYMBOL</span></span>       | <span data-ttu-id="96366-136">0x0400</span><span class="sxs-lookup"><span data-stu-id="96366-136">0x0400</span></span> | <span data-ttu-id="96366-137">Défini sur 1 si le mode de conversion des symboles ; 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="96366-137">Set to 1 if SYMBOL conversion mode; 0 if not.</span></span>                   |
| <span data-ttu-id="96366-138">\_CONVERSIONMODE TF \_ fixe</span><span class="sxs-lookup"><span data-stu-id="96366-138">TF\_CONVERSIONMODE\_FIXED</span></span>        | <span data-ttu-id="96366-139">0x0800</span><span class="sxs-lookup"><span data-stu-id="96366-139">0x0800</span></span> | <span data-ttu-id="96366-140">Défini sur 1 si le mode de conversion est fixe ; 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="96366-140">Set to 1 if fixed conversion mode; 0 if not.</span></span>                    |



 

<span data-ttu-id="96366-141">Les valeurs suivantes sont utilisées comme valeur de la [ \_ \_ \_ \_ phrase INPUTMODE du clavier du compartiment GUID](predefined-compartments.md).</span><span class="sxs-lookup"><span data-stu-id="96366-141">The following values are used as a value of [GUID\_COMPARTMENT\_KEYBOARD\_INPUTMODE\_SENTENCE](predefined-compartments.md).</span></span> <span data-ttu-id="96366-142">Cela équivaut aux valeurs [ \_ SMODE IME](../intl/ime-composition-string-values.md) pour imm32.</span><span class="sxs-lookup"><span data-stu-id="96366-142">This is equivalent with [IME\_SMODE](../intl/ime-composition-string-values.md) values for IMM32.</span></span>



| <span data-ttu-id="96366-143">Indicateur</span><span class="sxs-lookup"><span data-stu-id="96366-143">Flag</span></span>                            | <span data-ttu-id="96366-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="96366-144">Value</span></span>  | <span data-ttu-id="96366-145">Description</span><span class="sxs-lookup"><span data-stu-id="96366-145">Description</span></span>                                                                |
|---------------------------------|--------|----------------------------------------------------------------------------|
| <span data-ttu-id="96366-146">TF \_ SENTENCEMODE \_ aucun</span><span class="sxs-lookup"><span data-stu-id="96366-146">TF\_SENTENCEMODE\_NONE</span></span>          | <span data-ttu-id="96366-147">0x0000</span><span class="sxs-lookup"><span data-stu-id="96366-147">0x0000</span></span> | <span data-ttu-id="96366-148">Aucune information pour la phrase.</span><span class="sxs-lookup"><span data-stu-id="96366-148">No information for sentence.</span></span>                                               |
| <span data-ttu-id="96366-149">TF \_ SENTENCEMODE \_ PLAURALCLAUSE</span><span class="sxs-lookup"><span data-stu-id="96366-149">TF\_SENTENCEMODE\_PLAURALCLAUSE</span></span> | <span data-ttu-id="96366-150">0x0001</span><span class="sxs-lookup"><span data-stu-id="96366-150">0x0001</span></span> | <span data-ttu-id="96366-151">L’IME utilise des informations de clause pluriel pour effectuer le traitement de la conversion.</span><span class="sxs-lookup"><span data-stu-id="96366-151">The IME uses plural clause information to carry out conversion processing.</span></span> |
| <span data-ttu-id="96366-152">TF \_ SENTENCEMODE \_ SINGLECONVERT</span><span class="sxs-lookup"><span data-stu-id="96366-152">TF\_SENTENCEMODE\_SINGLECONVERT</span></span> | <span data-ttu-id="96366-153">0x0002</span><span class="sxs-lookup"><span data-stu-id="96366-153">0x0002</span></span> | <span data-ttu-id="96366-154">L’IME effectue le traitement de la conversion en mode à un seul caractère.</span><span class="sxs-lookup"><span data-stu-id="96366-154">The IME carries out conversion processing in single-character mode.</span></span>        |
| <span data-ttu-id="96366-155">\_SENTENCEMODE TF \_ automatique</span><span class="sxs-lookup"><span data-stu-id="96366-155">TF\_SENTENCEMODE\_AUTOMATIC</span></span>     | <span data-ttu-id="96366-156">0x0004</span><span class="sxs-lookup"><span data-stu-id="96366-156">0x0004</span></span> | <span data-ttu-id="96366-157">L’IME effectue le traitement de la conversion en mode automatique.</span><span class="sxs-lookup"><span data-stu-id="96366-157">The IME carries out conversion processing in automatic mode.</span></span>               |
| <span data-ttu-id="96366-158">TF \_ SENTENCEMODE \_ PHRASEPREDICT</span><span class="sxs-lookup"><span data-stu-id="96366-158">TF\_SENTENCEMODE\_PHRASEPREDICT</span></span> | <span data-ttu-id="96366-159">0x0008</span><span class="sxs-lookup"><span data-stu-id="96366-159">0x0008</span></span> | <span data-ttu-id="96366-160">L’IME utilise les informations d’expression pour prédire le caractère suivant.</span><span class="sxs-lookup"><span data-stu-id="96366-160">The IME uses phrase information to predict the next character.</span></span>             |
| <span data-ttu-id="96366-161">\_conversation TF SENTENCEMODE \_</span><span class="sxs-lookup"><span data-stu-id="96366-161">TF\_SENTENCEMODE\_CONVERSATION</span></span>  | <span data-ttu-id="96366-162">0x0010</span><span class="sxs-lookup"><span data-stu-id="96366-162">0x0010</span></span> | <span data-ttu-id="96366-163">L’IME utilise le mode conversation.</span><span class="sxs-lookup"><span data-stu-id="96366-163">The IME uses conversation mode.</span></span> <span data-ttu-id="96366-164">Cela est utile pour les applications de conversation.</span><span class="sxs-lookup"><span data-stu-id="96366-164">This is useful for chat applications.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="96366-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="96366-165">Requirements</span></span>



| <span data-ttu-id="96366-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="96366-166">Requirement</span></span> | <span data-ttu-id="96366-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="96366-167">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="96366-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96366-168">Minimum supported client</span></span><br/> | <span data-ttu-id="96366-169">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="96366-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="96366-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96366-170">Minimum supported server</span></span><br/> | <span data-ttu-id="96366-171">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="96366-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="96366-172">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="96366-172">Redistributable</span></span><br/>          | <span data-ttu-id="96366-173">TSF 1,0 onWindows NT 4.0, Windows 2000 ProfessionalandWindows MeWindows 98</span><span class="sxs-lookup"><span data-stu-id="96366-173">TSF 1.0 onWindows NT 4.0,Windows 2000 ProfessionalandWindows MeWindows 98</span></span><br/>   |
| <span data-ttu-id="96366-174">En-tête</span><span class="sxs-lookup"><span data-stu-id="96366-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="96366-175"><dt>Ctffunc. h</dt></span><span class="sxs-lookup"><span data-stu-id="96366-175"><dt>Ctffunc.h</dt></span></span> </dl>   |
| <span data-ttu-id="96366-176">MIDL</span><span class="sxs-lookup"><span data-stu-id="96366-176">IDL</span></span><br/>                      | <dl> <span data-ttu-id="96366-177"><dt>Ctffunc. idl</dt></span><span class="sxs-lookup"><span data-stu-id="96366-177"><dt>Ctffunc.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96366-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96366-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96366-179">Compartiments prédéfinis</span><span class="sxs-lookup"><span data-stu-id="96366-179">Predefined Compartments</span></span>](predefined-compartments.md)
</dt> </dl>

 

