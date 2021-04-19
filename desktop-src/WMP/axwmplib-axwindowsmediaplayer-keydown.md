---
title: Événement KeyOut de l’objet AxWindowsMediaPlayer
description: L’événement KeyOut se produit lorsqu’une touche est enfoncée. | Événement KeyOut de l’objet AxWindowsMediaPlayer
ms.assetid: e67b9628-6c53-4893-921a-9487ebfc1cd5
keywords:
- Événement KeyOut de l’objet AxWindowsMediaPlayer lecteur Windows Media
topic_type:
- apiref
api_name:
- KeyDown Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc89814063e1a43badd22e658b5f19ece7abb074
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535346"
---
# <a name="keydown-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="ce54f-105">Événement KeyOut de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="ce54f-105">KeyDown Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="ce54f-106">L’événement KeyOut se produit lorsqu’une touche est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="ce54f-106">The KeyDown event occurs when a key is pressed.</span></span>

``` syntax
[C#]
private void player_KeyDownEvent(
  object sender,
  _WMPOCXEvents_KeyDownEvent e
)

[Visual Basic]
Private Sub player_KeyDownEvent(  
  sender As Object, 
  e As _WMPOCXEvents_KeyDownEvent
) Handles player.KeyDownEvent
```

## <a name="event-data"></a><span data-ttu-id="ce54f-107">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="ce54f-107">Event Data</span></span>

<span data-ttu-id="ce54f-108">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ KeyDownEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="ce54f-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_KeyDownEventHandler**.</span></span> <span data-ttu-id="ce54f-109">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ KeyDownEvent**, qui contient les propriétés suivantes relatives à cet événement.</span><span class="sxs-lookup"><span data-stu-id="ce54f-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_KeyDownEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="ce54f-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="ce54f-110">Property</span></span>    | <span data-ttu-id="ce54f-111">Description</span><span class="sxs-lookup"><span data-stu-id="ce54f-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce54f-112">nKeyCode</span><span class="sxs-lookup"><span data-stu-id="ce54f-112">nKeyCode</span></span>    | <span data-ttu-id="ce54f-113">System. Int16Specifies quelle touche physique est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="ce54f-113">System.Int16Specifies which physical key is pressed.</span></span> <span data-ttu-id="ce54f-114">Pour connaître les valeurs possibles, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="ce54f-114">For possible values, see Remarks.</span></span><br/>                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="ce54f-115">nShiftState</span><span class="sxs-lookup"><span data-stu-id="ce54f-115">nShiftState</span></span> | <span data-ttu-id="ce54f-116">Champ de bits System. Int16a avec les bits les moins significatifs correspondant à la touche Maj (bit 0), la touche CTRL (bit 1) et la touche ALT (bit 2).</span><span class="sxs-lookup"><span data-stu-id="ce54f-116">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="ce54f-117">Ces bits correspondent respectivement aux valeurs 1, 2 et 4.</span><span class="sxs-lookup"><span data-stu-id="ce54f-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="ce54f-118">L’argument Shift indique l’état de ces clés.</span><span class="sxs-lookup"><span data-stu-id="ce54f-118">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="ce54f-119">Certains, tous ou aucun des bits peuvent être définis, ce qui indique qu’une partie, la totalité ou aucune des touches est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="ce54f-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ce54f-120">Notes</span><span class="sxs-lookup"><span data-stu-id="ce54f-120">Remarks</span></span>

<span data-ttu-id="ce54f-121">La propriété **nKeyCode** spécifie une clé physique.</span><span class="sxs-lookup"><span data-stu-id="ce54f-121">The **nKeyCode** property specifies a physical key.</span></span> <span data-ttu-id="ce54f-122">Les tableaux suivants indiquent les valeurs possibles pour les clés principales sur un clavier standard.</span><span class="sxs-lookup"><span data-stu-id="ce54f-122">The following tables show the possible values for the major keys on a standard keyboard.</span></span>

<span data-ttu-id="ce54f-123">Valeurs pour les clés principales.</span><span class="sxs-lookup"><span data-stu-id="ce54f-123">Values for the main keys.</span></span>



| <span data-ttu-id="ce54f-124">Clé</span><span class="sxs-lookup"><span data-stu-id="ce54f-124">Key</span></span>                     | <span data-ttu-id="ce54f-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce54f-125">Value</span></span>   |
|-------------------------|---------|
| <span data-ttu-id="ce54f-126">A-Z</span><span class="sxs-lookup"><span data-stu-id="ce54f-126">A-Z</span></span>                     | <span data-ttu-id="ce54f-127">65-90</span><span class="sxs-lookup"><span data-stu-id="ce54f-127">65-90</span></span>   |
| <span data-ttu-id="ce54f-128">0-9</span><span class="sxs-lookup"><span data-stu-id="ce54f-128">0-9</span></span>                     | <span data-ttu-id="ce54f-129">48-56</span><span class="sxs-lookup"><span data-stu-id="ce54f-129">48-56</span></span>   |
| <span data-ttu-id="ce54f-130">F1-F12</span><span class="sxs-lookup"><span data-stu-id="ce54f-130">F1-F12</span></span>                  | <span data-ttu-id="ce54f-131">112-123</span><span class="sxs-lookup"><span data-stu-id="ce54f-131">112-123</span></span> |
| <span data-ttu-id="ce54f-132">ÉCHAP</span><span class="sxs-lookup"><span data-stu-id="ce54f-132">ESC</span></span>                     | <span data-ttu-id="ce54f-133">27</span><span class="sxs-lookup"><span data-stu-id="ce54f-133">27</span></span>      |
| <span data-ttu-id="ce54f-134">Tab</span><span class="sxs-lookup"><span data-stu-id="ce54f-134">TAB</span></span>                     | <span data-ttu-id="ce54f-135">9</span><span class="sxs-lookup"><span data-stu-id="ce54f-135">9</span></span>       |
| <span data-ttu-id="ce54f-136">Verr. Maj</span><span class="sxs-lookup"><span data-stu-id="ce54f-136">CAPS LOCK</span></span>               | <span data-ttu-id="ce54f-137">20</span><span class="sxs-lookup"><span data-stu-id="ce54f-137">20</span></span>      |
| <span data-ttu-id="ce54f-138">SHIFT (gauche ou droite)</span><span class="sxs-lookup"><span data-stu-id="ce54f-138">SHIFT (left or right)</span></span>   | <span data-ttu-id="ce54f-139">16</span><span class="sxs-lookup"><span data-stu-id="ce54f-139">16</span></span>      |
| <span data-ttu-id="ce54f-140">CTRL (gauche ou droite)</span><span class="sxs-lookup"><span data-stu-id="ce54f-140">CTRL (left or right)</span></span>    | <span data-ttu-id="ce54f-141">17</span><span class="sxs-lookup"><span data-stu-id="ce54f-141">17</span></span>      |
| <span data-ttu-id="ce54f-142">ALT (gauche ou droite)</span><span class="sxs-lookup"><span data-stu-id="ce54f-142">ALT (left or right)</span></span>     | <span data-ttu-id="ce54f-143">18</span><span class="sxs-lookup"><span data-stu-id="ce54f-143">18</span></span>      |
| <span data-ttu-id="ce54f-144">SPACE</span><span class="sxs-lookup"><span data-stu-id="ce54f-144">SPACE</span></span>                   | <span data-ttu-id="ce54f-145">32</span><span class="sxs-lookup"><span data-stu-id="ce54f-145">32</span></span>      |
| <span data-ttu-id="ce54f-146">Ret.arr</span><span class="sxs-lookup"><span data-stu-id="ce54f-146">BACKSPACE</span></span>               | <span data-ttu-id="ce54f-147">8</span><span class="sxs-lookup"><span data-stu-id="ce54f-147">8</span></span>       |
| <span data-ttu-id="ce54f-148">ENTRÉE</span><span class="sxs-lookup"><span data-stu-id="ce54f-148">ENTER</span></span>                   | <span data-ttu-id="ce54f-149">13</span><span class="sxs-lookup"><span data-stu-id="ce54f-149">13</span></span>      |
| <span data-ttu-id="ce54f-150">Touche de logo Windows, à gauche</span><span class="sxs-lookup"><span data-stu-id="ce54f-150">Windows logo key, left</span></span>  | <span data-ttu-id="ce54f-151">91</span><span class="sxs-lookup"><span data-stu-id="ce54f-151">91</span></span>      |
| <span data-ttu-id="ce54f-152">Touche du logo Windows, droite</span><span class="sxs-lookup"><span data-stu-id="ce54f-152">Windows logo key, right</span></span> | <span data-ttu-id="ce54f-153">92</span><span class="sxs-lookup"><span data-stu-id="ce54f-153">92</span></span>      |
| <span data-ttu-id="ce54f-154">Clé de l'application</span><span class="sxs-lookup"><span data-stu-id="ce54f-154">Application key</span></span>         | <span data-ttu-id="ce54f-155">93</span><span class="sxs-lookup"><span data-stu-id="ce54f-155">93</span></span>      |



 

<span data-ttu-id="ce54f-156">Valeurs des touches du pavé numérique.</span><span class="sxs-lookup"><span data-stu-id="ce54f-156">Values for the number pad keys.</span></span>



| <span data-ttu-id="ce54f-157">Clé</span><span class="sxs-lookup"><span data-stu-id="ce54f-157">Key</span></span>               | <span data-ttu-id="ce54f-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce54f-158">Value</span></span>  |
|-------------------|--------|
| <span data-ttu-id="ce54f-159">0-9</span><span class="sxs-lookup"><span data-stu-id="ce54f-159">0-9</span></span>               | <span data-ttu-id="ce54f-160">96-105</span><span class="sxs-lookup"><span data-stu-id="ce54f-160">96-105</span></span> |
| <span data-ttu-id="ce54f-161">VERR. NUM</span><span class="sxs-lookup"><span data-stu-id="ce54f-161">NUM LOCK</span></span>          | <span data-ttu-id="ce54f-162">144</span><span class="sxs-lookup"><span data-stu-id="ce54f-162">144</span></span>    |
| <span data-ttu-id="ce54f-163">Division (/)</span><span class="sxs-lookup"><span data-stu-id="ce54f-163">DIVIDE (/)</span></span>        | <span data-ttu-id="ce54f-164">111</span><span class="sxs-lookup"><span data-stu-id="ce54f-164">111</span></span>    |
| <span data-ttu-id="ce54f-165">MULTIPLIER ( \* )</span><span class="sxs-lookup"><span data-stu-id="ce54f-165">MULTIPLY (\*)</span></span>     | <span data-ttu-id="ce54f-166">106</span><span class="sxs-lookup"><span data-stu-id="ce54f-166">106</span></span>    |
| <span data-ttu-id="ce54f-167">SOUSTRAIre (-)</span><span class="sxs-lookup"><span data-stu-id="ce54f-167">SUBTRACT (-)</span></span>      | <span data-ttu-id="ce54f-168">109</span><span class="sxs-lookup"><span data-stu-id="ce54f-168">109</span></span>    |
| <span data-ttu-id="ce54f-169">AJOUTER (+)</span><span class="sxs-lookup"><span data-stu-id="ce54f-169">ADD (+)</span></span>           | <span data-ttu-id="ce54f-170">107</span><span class="sxs-lookup"><span data-stu-id="ce54f-170">107</span></span>    |
| <span data-ttu-id="ce54f-171">SÉPARATEUR (entrée)</span><span class="sxs-lookup"><span data-stu-id="ce54f-171">SEPARATOR (Enter)</span></span> | <span data-ttu-id="ce54f-172">108</span><span class="sxs-lookup"><span data-stu-id="ce54f-172">108</span></span>    |
| <span data-ttu-id="ce54f-173">DÉCIMAL (.)</span><span class="sxs-lookup"><span data-stu-id="ce54f-173">DECIMAL (.)</span></span>       | <span data-ttu-id="ce54f-174">110</span><span class="sxs-lookup"><span data-stu-id="ce54f-174">110</span></span>    |



 

<span data-ttu-id="ce54f-175">Valeurs des touches de navigation.</span><span class="sxs-lookup"><span data-stu-id="ce54f-175">Values for the navigation keys.</span></span>



| <span data-ttu-id="ce54f-176">Clé</span><span class="sxs-lookup"><span data-stu-id="ce54f-176">Key</span></span>         | <span data-ttu-id="ce54f-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce54f-177">Value</span></span> |
|-------------|-------|
| <span data-ttu-id="ce54f-178">INSERT</span><span class="sxs-lookup"><span data-stu-id="ce54f-178">INSERT</span></span>      | <span data-ttu-id="ce54f-179">45</span><span class="sxs-lookup"><span data-stu-id="ce54f-179">45</span></span>    |
| <span data-ttu-id="ce54f-180">Suppression</span><span class="sxs-lookup"><span data-stu-id="ce54f-180">DELETE</span></span>      | <span data-ttu-id="ce54f-181">46</span><span class="sxs-lookup"><span data-stu-id="ce54f-181">46</span></span>    |
| <span data-ttu-id="ce54f-182">Origine</span><span class="sxs-lookup"><span data-stu-id="ce54f-182">HOME</span></span>        | <span data-ttu-id="ce54f-183">36</span><span class="sxs-lookup"><span data-stu-id="ce54f-183">36</span></span>    |
| <span data-ttu-id="ce54f-184">FIN</span><span class="sxs-lookup"><span data-stu-id="ce54f-184">END</span></span>         | <span data-ttu-id="ce54f-185">35</span><span class="sxs-lookup"><span data-stu-id="ce54f-185">35</span></span>    |
| <span data-ttu-id="ce54f-186">Pg. préc</span><span class="sxs-lookup"><span data-stu-id="ce54f-186">PAGE UP</span></span>     | <span data-ttu-id="ce54f-187">33</span><span class="sxs-lookup"><span data-stu-id="ce54f-187">33</span></span>    |
| <span data-ttu-id="ce54f-188">Pg. suiv</span><span class="sxs-lookup"><span data-stu-id="ce54f-188">PAGE DOWN</span></span>   | <span data-ttu-id="ce54f-189">34</span><span class="sxs-lookup"><span data-stu-id="ce54f-189">34</span></span>    |
| <span data-ttu-id="ce54f-190">Flèche haut</span><span class="sxs-lookup"><span data-stu-id="ce54f-190">UP ARROW</span></span>    | <span data-ttu-id="ce54f-191">38</span><span class="sxs-lookup"><span data-stu-id="ce54f-191">38</span></span>    |
| <span data-ttu-id="ce54f-192">Bas</span><span class="sxs-lookup"><span data-stu-id="ce54f-192">DOWN ARROW</span></span>  | <span data-ttu-id="ce54f-193">40</span><span class="sxs-lookup"><span data-stu-id="ce54f-193">40</span></span>    |
| <span data-ttu-id="ce54f-194">Gauche</span><span class="sxs-lookup"><span data-stu-id="ce54f-194">LEFT ARROW</span></span>  | <span data-ttu-id="ce54f-195">37</span><span class="sxs-lookup"><span data-stu-id="ce54f-195">37</span></span>    |
| <span data-ttu-id="ce54f-196">Flèche droite</span><span class="sxs-lookup"><span data-stu-id="ce54f-196">RIGHT ARROW</span></span> | <span data-ttu-id="ce54f-197">39</span><span class="sxs-lookup"><span data-stu-id="ce54f-197">39</span></span>    |



 

## <a name="requirements"></a><span data-ttu-id="ce54f-198">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce54f-198">Requirements</span></span>



| <span data-ttu-id="ce54f-199">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce54f-199">Requirement</span></span> | <span data-ttu-id="ce54f-200">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce54f-200">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce54f-201">Version</span><span class="sxs-lookup"><span data-stu-id="ce54f-201">Version</span></span><br/>   | <span data-ttu-id="ce54f-202">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="ce54f-202">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="ce54f-203">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ce54f-203">Namespace</span></span><br/> | <span data-ttu-id="ce54f-204">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="ce54f-204">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="ce54f-205">Assembly</span><span class="sxs-lookup"><span data-stu-id="ce54f-205">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ce54f-206"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ce54f-206"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce54f-207">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce54f-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce54f-208">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="ce54f-208">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





