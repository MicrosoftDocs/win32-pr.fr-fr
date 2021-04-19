---
title: Player. KeyOut, événement
description: L’événement KeyOut se produit lorsqu’une touche est enfoncée. | Player. KeyOut, événement
ms.assetid: a34dafca-5db2-4065-bcfe-d66e633b26fb
keywords:
- Événement KeyOut Windows Media Player
- Événement KeyOut Windows Media Player, classe Player
- Classe de lecteur Windows Media Player, KeyOut (événement)
topic_type:
- apiref
api_name:
- Player.KeyDown
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 226430421977a58eca02b7a42cf0349f2a5ff520
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535344"
---
# <a name="playerkeydown-event"></a><span data-ttu-id="3d98a-107">Player. KeyOut, événement</span><span class="sxs-lookup"><span data-stu-id="3d98a-107">Player.KeyDown event</span></span>

<span data-ttu-id="3d98a-108">L’événement KeyOut se produit lorsqu’une touche est **enfoncée** .</span><span class="sxs-lookup"><span data-stu-id="3d98a-108">The **KeyDown** event occurs when a key is pressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d98a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d98a-109">Syntax</span></span>


```JScript
Player.KeyDown(
  nKeyCode,
  nShiftState
)
```



## <a name="parameters"></a><span data-ttu-id="3d98a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3d98a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d98a-111">*nKeyCode*</span><span class="sxs-lookup"><span data-stu-id="3d98a-111">*nKeyCode*</span></span> 
</dt> <dd>

<span data-ttu-id="3d98a-112">**Nombre** (**int**) spécifiant la touche physique qui est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="3d98a-112">**Number** (**int**) specifying which physical key is pressed.</span></span> <span data-ttu-id="3d98a-113">Pour connaître les valeurs possibles, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="3d98a-113">For possible values, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="3d98a-114">*nShiftState*</span><span class="sxs-lookup"><span data-stu-id="3d98a-114">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="3d98a-115">**Nombre** (**int**) spécifiant un champ de bits avec les bits les moins significatifs correspondant à la touche Maj (bit 0), la touche Ctrl (bit 1) et la touche Alt (bit 2).</span><span class="sxs-lookup"><span data-stu-id="3d98a-115">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="3d98a-116">Ces bits correspondent respectivement aux valeurs 1, 2 et 4.</span><span class="sxs-lookup"><span data-stu-id="3d98a-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="3d98a-117">L’argument Shift indique l’état de ces clés.</span><span class="sxs-lookup"><span data-stu-id="3d98a-117">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="3d98a-118">Certains, tous ou aucun des bits peuvent être définis, ce qui indique qu’une partie, la totalité ou aucune des touches est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="3d98a-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d98a-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3d98a-119">Return value</span></span>

<span data-ttu-id="3d98a-120">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="3d98a-120">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d98a-121">Notes</span><span class="sxs-lookup"><span data-stu-id="3d98a-121">Remarks</span></span>

<span data-ttu-id="3d98a-122">L’argument *nKeyCode* spécifie une clé physique.</span><span class="sxs-lookup"><span data-stu-id="3d98a-122">The *nKeyCode* argument specifies a physical key.</span></span> <span data-ttu-id="3d98a-123">Les tableaux suivants indiquent les valeurs possibles pour les clés principales sur un clavier standard.</span><span class="sxs-lookup"><span data-stu-id="3d98a-123">The following tables show the possible values for the major keys on a standard keyboard.</span></span>

<span data-ttu-id="3d98a-124">Valeurs pour les clés principales.</span><span class="sxs-lookup"><span data-stu-id="3d98a-124">Values for the main keys.</span></span>



| <span data-ttu-id="3d98a-125">Clé</span><span class="sxs-lookup"><span data-stu-id="3d98a-125">Key</span></span>                     | <span data-ttu-id="3d98a-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d98a-126">Value</span></span>   |
|-------------------------|---------|
| <span data-ttu-id="3d98a-127">A-Z</span><span class="sxs-lookup"><span data-stu-id="3d98a-127">A-Z</span></span>                     | <span data-ttu-id="3d98a-128">65-90</span><span class="sxs-lookup"><span data-stu-id="3d98a-128">65-90</span></span>   |
| <span data-ttu-id="3d98a-129">0-9</span><span class="sxs-lookup"><span data-stu-id="3d98a-129">0-9</span></span>                     | <span data-ttu-id="3d98a-130">48-56</span><span class="sxs-lookup"><span data-stu-id="3d98a-130">48-56</span></span>   |
| <span data-ttu-id="3d98a-131">F1-F12</span><span class="sxs-lookup"><span data-stu-id="3d98a-131">F1-F12</span></span>                  | <span data-ttu-id="3d98a-132">112-123</span><span class="sxs-lookup"><span data-stu-id="3d98a-132">112-123</span></span> |
| <span data-ttu-id="3d98a-133">ÉCHAP</span><span class="sxs-lookup"><span data-stu-id="3d98a-133">ESC</span></span>                     | <span data-ttu-id="3d98a-134">27</span><span class="sxs-lookup"><span data-stu-id="3d98a-134">27</span></span>      |
| <span data-ttu-id="3d98a-135">Tab</span><span class="sxs-lookup"><span data-stu-id="3d98a-135">TAB</span></span>                     | <span data-ttu-id="3d98a-136">9</span><span class="sxs-lookup"><span data-stu-id="3d98a-136">9</span></span>       |
| <span data-ttu-id="3d98a-137">Verr. Maj</span><span class="sxs-lookup"><span data-stu-id="3d98a-137">CAPS LOCK</span></span>               | <span data-ttu-id="3d98a-138">20</span><span class="sxs-lookup"><span data-stu-id="3d98a-138">20</span></span>      |
| <span data-ttu-id="3d98a-139">SHIFT (gauche ou droite)</span><span class="sxs-lookup"><span data-stu-id="3d98a-139">SHIFT (left or right)</span></span>   | <span data-ttu-id="3d98a-140">16</span><span class="sxs-lookup"><span data-stu-id="3d98a-140">16</span></span>      |
| <span data-ttu-id="3d98a-141">CTRL (gauche ou droite)</span><span class="sxs-lookup"><span data-stu-id="3d98a-141">CTRL (left or right)</span></span>    | <span data-ttu-id="3d98a-142">17</span><span class="sxs-lookup"><span data-stu-id="3d98a-142">17</span></span>      |
| <span data-ttu-id="3d98a-143">ALT (gauche ou droite)</span><span class="sxs-lookup"><span data-stu-id="3d98a-143">ALT (left or right)</span></span>     | <span data-ttu-id="3d98a-144">18</span><span class="sxs-lookup"><span data-stu-id="3d98a-144">18</span></span>      |
| <span data-ttu-id="3d98a-145">SPACE</span><span class="sxs-lookup"><span data-stu-id="3d98a-145">SPACE</span></span>                   | <span data-ttu-id="3d98a-146">32</span><span class="sxs-lookup"><span data-stu-id="3d98a-146">32</span></span>      |
| <span data-ttu-id="3d98a-147">Ret.arr</span><span class="sxs-lookup"><span data-stu-id="3d98a-147">BACKSPACE</span></span>               | <span data-ttu-id="3d98a-148">8</span><span class="sxs-lookup"><span data-stu-id="3d98a-148">8</span></span>       |
| <span data-ttu-id="3d98a-149">ENTRÉE</span><span class="sxs-lookup"><span data-stu-id="3d98a-149">ENTER</span></span>                   | <span data-ttu-id="3d98a-150">13</span><span class="sxs-lookup"><span data-stu-id="3d98a-150">13</span></span>      |
| <span data-ttu-id="3d98a-151">Touche de logo Windows, à gauche</span><span class="sxs-lookup"><span data-stu-id="3d98a-151">Windows logo key, left</span></span>  | <span data-ttu-id="3d98a-152">91</span><span class="sxs-lookup"><span data-stu-id="3d98a-152">91</span></span>      |
| <span data-ttu-id="3d98a-153">Touche du logo Windows, droite</span><span class="sxs-lookup"><span data-stu-id="3d98a-153">Windows logo key, right</span></span> | <span data-ttu-id="3d98a-154">92</span><span class="sxs-lookup"><span data-stu-id="3d98a-154">92</span></span>      |
| <span data-ttu-id="3d98a-155">Clé de l'application</span><span class="sxs-lookup"><span data-stu-id="3d98a-155">Application key</span></span>         | <span data-ttu-id="3d98a-156">93</span><span class="sxs-lookup"><span data-stu-id="3d98a-156">93</span></span>      |



 

<span data-ttu-id="3d98a-157">Valeurs des touches du pavé numérique.</span><span class="sxs-lookup"><span data-stu-id="3d98a-157">Values for the number pad keys.</span></span>



| <span data-ttu-id="3d98a-158">Clé</span><span class="sxs-lookup"><span data-stu-id="3d98a-158">Key</span></span>               | <span data-ttu-id="3d98a-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d98a-159">Value</span></span>  |
|-------------------|--------|
| <span data-ttu-id="3d98a-160">0-9</span><span class="sxs-lookup"><span data-stu-id="3d98a-160">0-9</span></span>               | <span data-ttu-id="3d98a-161">96-105</span><span class="sxs-lookup"><span data-stu-id="3d98a-161">96-105</span></span> |
| <span data-ttu-id="3d98a-162">VERR. NUM</span><span class="sxs-lookup"><span data-stu-id="3d98a-162">NUM LOCK</span></span>          | <span data-ttu-id="3d98a-163">144</span><span class="sxs-lookup"><span data-stu-id="3d98a-163">144</span></span>    |
| <span data-ttu-id="3d98a-164">Division (/)</span><span class="sxs-lookup"><span data-stu-id="3d98a-164">DIVIDE (/)</span></span>        | <span data-ttu-id="3d98a-165">111</span><span class="sxs-lookup"><span data-stu-id="3d98a-165">111</span></span>    |
| <span data-ttu-id="3d98a-166">MULTIPLIER ( \* )</span><span class="sxs-lookup"><span data-stu-id="3d98a-166">MULTIPLY (\*)</span></span>     | <span data-ttu-id="3d98a-167">106</span><span class="sxs-lookup"><span data-stu-id="3d98a-167">106</span></span>    |
| <span data-ttu-id="3d98a-168">SOUSTRAIre (-)</span><span class="sxs-lookup"><span data-stu-id="3d98a-168">SUBTRACT (-)</span></span>      | <span data-ttu-id="3d98a-169">109</span><span class="sxs-lookup"><span data-stu-id="3d98a-169">109</span></span>    |
| <span data-ttu-id="3d98a-170">AJOUTER (+)</span><span class="sxs-lookup"><span data-stu-id="3d98a-170">ADD (+)</span></span>           | <span data-ttu-id="3d98a-171">107</span><span class="sxs-lookup"><span data-stu-id="3d98a-171">107</span></span>    |
| <span data-ttu-id="3d98a-172">SÉPARATEUR (entrée)</span><span class="sxs-lookup"><span data-stu-id="3d98a-172">SEPARATOR (Enter)</span></span> | <span data-ttu-id="3d98a-173">108</span><span class="sxs-lookup"><span data-stu-id="3d98a-173">108</span></span>    |
| <span data-ttu-id="3d98a-174">DÉCIMAL (.)</span><span class="sxs-lookup"><span data-stu-id="3d98a-174">DECIMAL (.)</span></span>       | <span data-ttu-id="3d98a-175">110</span><span class="sxs-lookup"><span data-stu-id="3d98a-175">110</span></span>    |



 

<span data-ttu-id="3d98a-176">Valeurs des touches de navigation.</span><span class="sxs-lookup"><span data-stu-id="3d98a-176">Values for the navigation keys.</span></span>



| <span data-ttu-id="3d98a-177">Clé</span><span class="sxs-lookup"><span data-stu-id="3d98a-177">Key</span></span>         | <span data-ttu-id="3d98a-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d98a-178">Value</span></span> |
|-------------|-------|
| <span data-ttu-id="3d98a-179">INSERT</span><span class="sxs-lookup"><span data-stu-id="3d98a-179">INSERT</span></span>      | <span data-ttu-id="3d98a-180">45</span><span class="sxs-lookup"><span data-stu-id="3d98a-180">45</span></span>    |
| <span data-ttu-id="3d98a-181">Suppression</span><span class="sxs-lookup"><span data-stu-id="3d98a-181">DELETE</span></span>      | <span data-ttu-id="3d98a-182">46</span><span class="sxs-lookup"><span data-stu-id="3d98a-182">46</span></span>    |
| <span data-ttu-id="3d98a-183">Origine</span><span class="sxs-lookup"><span data-stu-id="3d98a-183">HOME</span></span>        | <span data-ttu-id="3d98a-184">36</span><span class="sxs-lookup"><span data-stu-id="3d98a-184">36</span></span>    |
| <span data-ttu-id="3d98a-185">FIN</span><span class="sxs-lookup"><span data-stu-id="3d98a-185">END</span></span>         | <span data-ttu-id="3d98a-186">35</span><span class="sxs-lookup"><span data-stu-id="3d98a-186">35</span></span>    |
| <span data-ttu-id="3d98a-187">Pg. préc</span><span class="sxs-lookup"><span data-stu-id="3d98a-187">PAGE UP</span></span>     | <span data-ttu-id="3d98a-188">33</span><span class="sxs-lookup"><span data-stu-id="3d98a-188">33</span></span>    |
| <span data-ttu-id="3d98a-189">Pg. suiv</span><span class="sxs-lookup"><span data-stu-id="3d98a-189">PAGE DOWN</span></span>   | <span data-ttu-id="3d98a-190">34</span><span class="sxs-lookup"><span data-stu-id="3d98a-190">34</span></span>    |
| <span data-ttu-id="3d98a-191">Flèche haut</span><span class="sxs-lookup"><span data-stu-id="3d98a-191">UP ARROW</span></span>    | <span data-ttu-id="3d98a-192">38</span><span class="sxs-lookup"><span data-stu-id="3d98a-192">38</span></span>    |
| <span data-ttu-id="3d98a-193">Bas</span><span class="sxs-lookup"><span data-stu-id="3d98a-193">DOWN ARROW</span></span>  | <span data-ttu-id="3d98a-194">40</span><span class="sxs-lookup"><span data-stu-id="3d98a-194">40</span></span>    |
| <span data-ttu-id="3d98a-195">Gauche</span><span class="sxs-lookup"><span data-stu-id="3d98a-195">LEFT ARROW</span></span>  | <span data-ttu-id="3d98a-196">37</span><span class="sxs-lookup"><span data-stu-id="3d98a-196">37</span></span>    |
| <span data-ttu-id="3d98a-197">Flèche droite</span><span class="sxs-lookup"><span data-stu-id="3d98a-197">RIGHT ARROW</span></span> | <span data-ttu-id="3d98a-198">39</span><span class="sxs-lookup"><span data-stu-id="3d98a-198">39</span></span>    |



 

<span data-ttu-id="3d98a-199">La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné.</span><span class="sxs-lookup"><span data-stu-id="3d98a-199">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="3d98a-200">Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="3d98a-200">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="3d98a-201">**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3d98a-201">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d98a-202">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d98a-202">Requirements</span></span>



| <span data-ttu-id="3d98a-203">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d98a-203">Requirement</span></span> | <span data-ttu-id="3d98a-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d98a-204">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3d98a-205">Version</span><span class="sxs-lookup"><span data-stu-id="3d98a-205">Version</span></span><br/> | <span data-ttu-id="3d98a-206">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3d98a-206">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="3d98a-207">DLL</span><span class="sxs-lookup"><span data-stu-id="3d98a-207">DLL</span></span><br/>     | <dl> <span data-ttu-id="3d98a-208"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d98a-208"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d98a-209">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d98a-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d98a-210">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="3d98a-210">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





