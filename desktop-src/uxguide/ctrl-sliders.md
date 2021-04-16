---
title: Curseurs (concepts de base de la conception)
description: Avec un curseur, les utilisateurs peuvent choisir parmi une plage de valeurs continue.
ms.assetid: dee70fbc-6f18-43c7-9d41-4e97eac41e53
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 7ff9791ab49c338e4c11e014a3e996771571add9
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104556300"
---
# <a name="sliders-design-basics"></a><span data-ttu-id="4616f-103">Curseurs (concepts de base de la conception)</span><span class="sxs-lookup"><span data-stu-id="4616f-103">Sliders (Design basics)</span></span>

> [!NOTE]
> <span data-ttu-id="4616f-104">Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows.</span><span class="sxs-lookup"><span data-stu-id="4616f-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="4616f-105">La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.</span><span class="sxs-lookup"><span data-stu-id="4616f-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="4616f-106">Avec un curseur, les utilisateurs peuvent choisir parmi une plage de valeurs continue.</span><span class="sxs-lookup"><span data-stu-id="4616f-106">With a slider, users can choose from a continuous range of values.</span></span> <span data-ttu-id="4616f-107">Un curseur a une barre qui affiche la plage et un indicateur qui affiche la valeur actuelle.</span><span class="sxs-lookup"><span data-stu-id="4616f-107">A slider has a bar that shows the range and an indicator that shows the current value.</span></span> <span data-ttu-id="4616f-108">Les graduations facultatives affichent des valeurs.</span><span class="sxs-lookup"><span data-stu-id="4616f-108">Optional tick marks show values.</span></span>

![<span data-ttu-id="4616f-109">figure qui illustre la barre, le curseur et les graduations</span><span class="sxs-lookup"><span data-stu-id="4616f-109">figure showing bar, slider, and tick marks</span></span> ](images/ctrl-sliders-image1.png)

<span data-ttu-id="4616f-110">Curseur classique.</span><span class="sxs-lookup"><span data-stu-id="4616f-110">A typical slider.</span></span>

> [!Note]  
> <span data-ttu-id="4616f-111">Les instructions relatives à la [disposition](vis-layout.md) sont présentées dans un article distinct.</span><span class="sxs-lookup"><span data-stu-id="4616f-111">Guidelines related to [layout](vis-layout.md) are presented in a separate article.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="4616f-112">Est-ce le contrôle approprié ?</span><span class="sxs-lookup"><span data-stu-id="4616f-112">Is this the right control?</span></span>

<span data-ttu-id="4616f-113">Utilisez un curseur lorsque vous souhaitez que vos utilisateurs puissent **définir des valeurs contiguës définies (telles que le volume ou la luminosité) ou une plage de valeurs discrètes (telles que les paramètres de résolution d’écran).**</span><span class="sxs-lookup"><span data-stu-id="4616f-113">Use a slider when you want your users to be able to **set defined, contiguous values (such as volume or brightness) or a range of discrete values (such as screen resolution settings).**</span></span>

<span data-ttu-id="4616f-114">Un curseur représente un bon choix lorsque vous savez que les utilisateurs considèrent la valeur comme une quantité relative, et non comme une valeur numérique.</span><span class="sxs-lookup"><span data-stu-id="4616f-114">A slider is a good choice when you know that users think of the value as a relative quantity, not a numeric value.</span></span> <span data-ttu-id="4616f-115">Par exemple, dans le cas du volume, ils le régleront sur faible ou moyen, et pas sur 2 ou 5.</span><span class="sxs-lookup"><span data-stu-id="4616f-115">For example, users think about setting their audio volume to low or medium—not about setting the value to 2 or 5.</span></span>

<span data-ttu-id="4616f-116">Pour vous décider, posez-vous les questions suivantes :</span><span class="sxs-lookup"><span data-stu-id="4616f-116">To decide, consider these questions:</span></span>

-   <span data-ttu-id="4616f-117">**Le paramètre s’apparente-t-il à une quantité relative ?**</span><span class="sxs-lookup"><span data-stu-id="4616f-117">**Does the setting seem like a relative quantity?**</span></span> <span data-ttu-id="4616f-118">Si ce n’est pas le cas, utilisez des [cases d’option](ctrl-radio-buttons.md)ou une liste [déroulante](/windows/desktop/uxguide/ctrl-drop) ou [à sélection unique](ctrl-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="4616f-118">If not, use [radio buttons](ctrl-radio-buttons.md), or a [drop-down](/windows/desktop/uxguide/ctrl-drop) or [single-selection list](ctrl-list-boxes.md).</span></span>
-   <span data-ttu-id="4616f-119">**Le paramètre est-il une valeur numérique exacte connue ?**</span><span class="sxs-lookup"><span data-stu-id="4616f-119">**Is the setting an exact, known numeric value?**</span></span> <span data-ttu-id="4616f-120">Si c’est le cas, utilisez des [zones de texte numériques](ctrl-text-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="4616f-120">If so, use a [numeric text boxes](ctrl-text-boxes.md).</span></span>
-   <span data-ttu-id="4616f-121">**Un utilisateur va-t-il bénéficier d’un feedback instantané sur l’effet des modifications apportées aux paramètres ?**</span><span class="sxs-lookup"><span data-stu-id="4616f-121">**Would a user benefit from instant feedback on the effect of setting changes?**</span></span> <span data-ttu-id="4616f-122">Si tel est le cas, utilisez un curseur.</span><span class="sxs-lookup"><span data-stu-id="4616f-122">If so, use a slider.</span></span> <span data-ttu-id="4616f-123">Par exemple, les utilisateurs choisissent plus facilement une couleur lorsqu’ils voient immédiatement le résultat des modifications qu’ils ont apportées aux valeurs de teinte, de saturation ou de luminosité.</span><span class="sxs-lookup"><span data-stu-id="4616f-123">For example, users can choose a color more easily by immediately seeing the effect of changes to hue, saturation, or luminosity values.</span></span>
-   <span data-ttu-id="4616f-124">**Le paramètre a-t-il une plage de quatre valeurs ou plus ?**</span><span class="sxs-lookup"><span data-stu-id="4616f-124">**Does the setting have a range of four or more values?**</span></span> <span data-ttu-id="4616f-125">Si ce n’est pas le cas, utilisez des cases d’option.</span><span class="sxs-lookup"><span data-stu-id="4616f-125">If not, use radio buttons.</span></span>
-   <span data-ttu-id="4616f-126">**L’utilisateur peut-il changer la valeur ?**</span><span class="sxs-lookup"><span data-stu-id="4616f-126">**Can the user change the value?**</span></span> <span data-ttu-id="4616f-127">Les curseurs sont pour l’interaction utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4616f-127">Sliders are for user interaction.</span></span> <span data-ttu-id="4616f-128">Si un utilisateur ne peut pas modifier la valeur, utilisez plutôt une [zone de texte](ctrl-text-boxes.md) en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="4616f-128">If a user can't ever change the value, use a read-only [text box](ctrl-text-boxes.md) instead.</span></span>

<span data-ttu-id="4616f-129">Si un curseur ou une zone de texte numérique est possible, utilisez une zone de texte numérique si :</span><span class="sxs-lookup"><span data-stu-id="4616f-129">If a slider or a numeric text box is possible, use a numeric text box if:</span></span>

-   <span data-ttu-id="4616f-130">l’espace de l’écran est réduit ;</span><span class="sxs-lookup"><span data-stu-id="4616f-130">Screen space is tight.</span></span>
-   <span data-ttu-id="4616f-131">Il est probable qu’un utilisateur préfère utiliser le clavier.</span><span class="sxs-lookup"><span data-stu-id="4616f-131">A user is likely to prefer using the keyboard.</span></span>

<span data-ttu-id="4616f-132">Utilisez un curseur si :</span><span class="sxs-lookup"><span data-stu-id="4616f-132">Use a slider if:</span></span>

-   <span data-ttu-id="4616f-133">les utilisateurs bénéficieront d’un résultat instantané.</span><span class="sxs-lookup"><span data-stu-id="4616f-133">Users will benefit from instant feedback.</span></span>

## <a name="guidelines"></a><span data-ttu-id="4616f-134">Consignes</span><span class="sxs-lookup"><span data-stu-id="4616f-134">Guidelines</span></span>

-   <span data-ttu-id="4616f-135">**Utilisez une orientation naturelle.**</span><span class="sxs-lookup"><span data-stu-id="4616f-135">**Use a natural orientation.**</span></span> <span data-ttu-id="4616f-136">Par exemple, si le curseur représente une valeur du monde réelle qui est normalement affichée à la verticale (telle que la température), utilisez une orientation verticale.</span><span class="sxs-lookup"><span data-stu-id="4616f-136">For example, if the slider represents a real-world value that is normally shown vertically (such as temperature), use a vertical orientation.</span></span>
-   <span data-ttu-id="4616f-137">**Orientez le curseur pour refléter la culture de vos utilisateurs.**</span><span class="sxs-lookup"><span data-stu-id="4616f-137">**Orient the slider to reflect the culture of your users.**</span></span> <span data-ttu-id="4616f-138">Par exemple, les cultures occidentales se lisent de gauche à droite, donc pour les curseurs horizontaux, placez l’extrémité inférieure de la plage à gauche et l’extrémité supérieure à droite.</span><span class="sxs-lookup"><span data-stu-id="4616f-138">For example, Western cultures read from left to right, so for horizontal sliders, put the low end of the range on the left and the high end on the right.</span></span> <span data-ttu-id="4616f-139">Pour les cultures qui lisent de droite à gauche, effectuez l’inverse.</span><span class="sxs-lookup"><span data-stu-id="4616f-139">For cultures that read from right to left, do the opposite.</span></span>
-   <span data-ttu-id="4616f-140">**Dimensionnez le contrôle afin qu’un utilisateur puisse facilement définir la valeur souhaitée.**</span><span class="sxs-lookup"><span data-stu-id="4616f-140">**Size the control so that a user can easily set the desired value.**</span></span> <span data-ttu-id="4616f-141">Pour les paramètres ayant des valeurs distinctes, assurez-vous que l’utilisateur peut facilement sélectionner n’importe quelle valeur à l’aide de la souris.</span><span class="sxs-lookup"><span data-stu-id="4616f-141">For settings with discrete values, make sure the user can easily select any value using the mouse.</span></span>
-   <span data-ttu-id="4616f-142">**Envisagez d’utiliser une échelle non linéaire si la plage de valeurs est importante et que les utilisateurs sélectionneront probablement des valeurs à une extrémité de la plage.**</span><span class="sxs-lookup"><span data-stu-id="4616f-142">**Consider using a non-linear scale if the range of values is large and users will likely select values at one end of the range.**</span></span> <span data-ttu-id="4616f-143">Par exemple, la valeur de temps peut être 1 minute, 1 heure, 1 jour ou 1 mois.</span><span class="sxs-lookup"><span data-stu-id="4616f-143">For example, time value might be 1 minute, 1 hour, 1 day, or 1 month.</span></span>
-   <span data-ttu-id="4616f-144">**Chaque fois que cela est possible, donnez des commentaires immédiats pendant ou après qu’un utilisateur a fait une sélection.**</span><span class="sxs-lookup"><span data-stu-id="4616f-144">**Whenever practical, give immediate feedback while or after a user makes a selection.**</span></span> <span data-ttu-id="4616f-145">Par exemple, le contrôle du volume Microsoft Windows émet un signal sonore pour indiquer le volume audio qui en résulte.</span><span class="sxs-lookup"><span data-stu-id="4616f-145">For example, the Microsoft Windows volume control beeps to indicate the resulting audio volume.</span></span>
-   <span data-ttu-id="4616f-146">**Utilisez des étiquettes pour afficher les différentes valeurs de la plage.**</span><span class="sxs-lookup"><span data-stu-id="4616f-146">**Use labels to show the range of values.**</span></span>

    <span data-ttu-id="4616f-147">**Exception :** Si le curseur est orienté verticalement et que l’étiquette supérieure est maximale, haute, plus ou équivalente, vous pouvez omettre les autres étiquettes, car la signification est claire.</span><span class="sxs-lookup"><span data-stu-id="4616f-147">**Exception:** If the slider is vertically oriented and the top label is Maximum, High, More, or equivalent, you can omit the other labels since the meaning is clear.</span></span>

    ![<span data-ttu-id="4616f-148">figure d’un curseur vertical</span><span class="sxs-lookup"><span data-stu-id="4616f-148">figure of a vertical slider</span></span> ](images/ctrl-sliders-image2.png)

    <span data-ttu-id="4616f-149">Dans cet exemple, l’orientation verticale du curseur rend les étiquettes de plage inutiles.</span><span class="sxs-lookup"><span data-stu-id="4616f-149">In this example, the slider's vertical orientation makes the range labels unnecessary.</span></span>

-   <span data-ttu-id="4616f-150">**Utilisez des graduations lorsque les utilisateurs doivent connaître la valeur approximative du paramètre.**</span><span class="sxs-lookup"><span data-stu-id="4616f-150">**Use tick marks when users need to know the approximate value of the setting.**</span></span>
-   <span data-ttu-id="4616f-151">**Utilisez des graduations et une étiquette de valeur lorsque les utilisateurs doivent connaître la valeur exacte du paramètre de leur choix.**</span><span class="sxs-lookup"><span data-stu-id="4616f-151">**Use tick marks and a value label when users need to know the exact value of the setting they choose.**</span></span> <span data-ttu-id="4616f-152">Utilisez toujours une étiquette de valeur si un utilisateur doit connaître les unités pour avoir un sens du paramètre.</span><span class="sxs-lookup"><span data-stu-id="4616f-152">Always use a value label if a user needs to know the units to make sense of the setting.</span></span>

    ![<span data-ttu-id="4616f-153">figure du curseur qui indique le nombre de pixels sélectionnés</span><span class="sxs-lookup"><span data-stu-id="4616f-153">figure of slider showing number of pixels selected</span></span> ](images/ctrl-sliders-image3.png)

    <span data-ttu-id="4616f-154">Dans cet exemple, une étiquette est utilisée pour indiquer clairement la valeur sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="4616f-154">In this example, a label is used to clearly indicate the selected value.</span></span>

-   <span data-ttu-id="4616f-155">**Pour les curseurs orientés horizontalement, placez les graduations sous le curseur.**</span><span class="sxs-lookup"><span data-stu-id="4616f-155">**For horizontally-oriented sliders, place tick marks under the slider.**</span></span> <span data-ttu-id="4616f-156">Pour les curseurs orientés verticalement, placez les graduations à droite pour les cultures occidentales ; pour les cultures qui lisent de droite à gauche, effectuez l’inverse.</span><span class="sxs-lookup"><span data-stu-id="4616f-156">For vertically-oriented sliders, place tick marks to the right for Western cultures; for cultures that read from right to left, do the opposite.</span></span>
-   <span data-ttu-id="4616f-157">**Placez l’étiquette de valeur complètement sous le contrôle Slider afin que la relation soit claire.**</span><span class="sxs-lookup"><span data-stu-id="4616f-157">**Place the value label completely under the slider control so that the relationship is clear.**</span></span>

    <span data-ttu-id="4616f-158">**Incorrect :**</span><span class="sxs-lookup"><span data-stu-id="4616f-158">**Incorrect:**</span></span>

    ![<span data-ttu-id="4616f-159">figure d’une étiquette qui est plus longue que son curseur</span><span class="sxs-lookup"><span data-stu-id="4616f-159">figure of a label that is longer than its slider</span></span> ](images/ctrl-sliders-image4.png)

    <span data-ttu-id="4616f-160">Dans cet exemple, l’étiquette de la valeur n’est pas alignée sous le curseur.</span><span class="sxs-lookup"><span data-stu-id="4616f-160">In this example, the value label isn't aligned under the slider.</span></span>

-   <span data-ttu-id="4616f-161">**Lorsque vous désactivez un curseur, désactivez également les étiquettes associées.**</span><span class="sxs-lookup"><span data-stu-id="4616f-161">**When disabling a slider, also disable any associated labels.**</span></span>
-   <span data-ttu-id="4616f-162">**N’utilisez pas à la fois un curseur et une zone de texte numérique pour le même paramètre.**</span><span class="sxs-lookup"><span data-stu-id="4616f-162">**Don't use both a slider and a numeric text box for the same setting.**</span></span> <span data-ttu-id="4616f-163">Utilisez uniquement le contrôle le plus approprié.</span><span class="sxs-lookup"><span data-stu-id="4616f-163">Use only the more appropriate control.</span></span>

    <span data-ttu-id="4616f-164">**Exception :** Utilisez les deux contrôles lorsque l’utilisateur a besoin de commentaires immédiats et de la possibilité de définir une valeur numérique exacte.</span><span class="sxs-lookup"><span data-stu-id="4616f-164">**Exception:** Use both controls when the user needs both immediate feedback and the ability to set an exact numeric value.</span></span>

-   <span data-ttu-id="4616f-165">**N’utilisez pas un curseur comme indicateur de progression.**</span><span class="sxs-lookup"><span data-stu-id="4616f-165">**Don't use a slider as a progress indicator.**</span></span>
-   <span data-ttu-id="4616f-166">**Ne modifiez pas la taille par défaut de l’indicateur de curseur.**</span><span class="sxs-lookup"><span data-stu-id="4616f-166">**Don't change the size of the slider indicator from the default size.**</span></span>

    <span data-ttu-id="4616f-167">**Incorrect :**</span><span class="sxs-lookup"><span data-stu-id="4616f-167">**Incorrect:**</span></span>

    ![<span data-ttu-id="4616f-168">figure du curseur plus petit que la valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="4616f-168">figure of slider that is smaller than the default</span></span> ](images/ctrl-sliders-image5.png)

    <span data-ttu-id="4616f-169">Dans cet exemple, une taille plus petite que la valeur par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="4616f-169">In this example, a size smaller than the default is used.</span></span>

    <span data-ttu-id="4616f-170">**Correct :**</span><span class="sxs-lookup"><span data-stu-id="4616f-170">**Correct:**</span></span>

    ![<span data-ttu-id="4616f-171">Figure représentant le curseur par défaut</span><span class="sxs-lookup"><span data-stu-id="4616f-171">figure showing the default slider</span></span> ](images/ctrl-sliders-image6.png)

    <span data-ttu-id="4616f-172">Dans cet exemple, la taille par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="4616f-172">In this example, the default size is used.</span></span>

-   <span data-ttu-id="4616f-173">**N’étiquetez pas toutes les graduations.**</span><span class="sxs-lookup"><span data-stu-id="4616f-173">**Don't label every tick mark.**</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="4616f-174">Dimensionnement et espacement recommandés</span><span class="sxs-lookup"><span data-stu-id="4616f-174">Recommended sizing and spacing</span></span>

![<span data-ttu-id="4616f-175">figure du dimensionnement et de l’espacement de curseur recommandés</span><span class="sxs-lookup"><span data-stu-id="4616f-175">figure of recommended slider sizing and spacing</span></span> ](images/ctrl-sliders-image7.png)

<span data-ttu-id="4616f-176">Dimensionnement et espacement recommandés pour les curseurs.</span><span class="sxs-lookup"><span data-stu-id="4616f-176">Recommended sizing and spacing for sliders.</span></span>

## <a name="labels"></a><span data-ttu-id="4616f-177">Étiquettes</span><span class="sxs-lookup"><span data-stu-id="4616f-177">Labels</span></span>

### <a name="slider-labels"></a><span data-ttu-id="4616f-178">Étiquettes de curseur</span><span class="sxs-lookup"><span data-stu-id="4616f-178">Slider labels</span></span>

-   <span data-ttu-id="4616f-179">Utilisez une étiquette de texte statique se terminant par un signe deux-points, ou une étiquette de zone de groupe sans ponctuation finale.</span><span class="sxs-lookup"><span data-stu-id="4616f-179">Use a static text label ending with a colon, or a group box label with no ending punctuation.</span></span>
-   <span data-ttu-id="4616f-180">Attribuez une clé d’accès unique à chaque étiquette.</span><span class="sxs-lookup"><span data-stu-id="4616f-180">Assign a unique access key to each label.</span></span> <span data-ttu-id="4616f-181">Pour connaître les instructions d’affectation, consultez [clavier](inter-keyboard.md).</span><span class="sxs-lookup"><span data-stu-id="4616f-181">For assignment guidelines, see [Keyboard](inter-keyboard.md).</span></span>
-   <span data-ttu-id="4616f-182">Utilisez les majuscules comme pour les phrases.</span><span class="sxs-lookup"><span data-stu-id="4616f-182">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="4616f-183">Placez l’étiquette du curseur à gauche du curseur ou au-dessus et alignée sur le bord gauche du curseur (ou sur son identificateur de plage de gauche, le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="4616f-183">Position the slider label either to the left of the slider, or above and aligned with the left edge of the slider (or its left range identifier, if present).</span></span>

### <a name="range-labels"></a><span data-ttu-id="4616f-184">Étiquettes de plage</span><span class="sxs-lookup"><span data-stu-id="4616f-184">Range labels</span></span>

-   <span data-ttu-id="4616f-185">Étiquetez les deux extrémités de la plage du curseur, à moins que cela ne soit pas nécessaire avec une orientation verticale.</span><span class="sxs-lookup"><span data-stu-id="4616f-185">Label the two ends of the slider range, unless a vertical orientation makes this unnecessary.</span></span>
-   <span data-ttu-id="4616f-186">Utilisez uniquement Word, si possible, pour chaque étiquette.</span><span class="sxs-lookup"><span data-stu-id="4616f-186">Use only word, if possible, for each label.</span></span>
-   <span data-ttu-id="4616f-187">N’utilisez pas de ponctuation finale.</span><span class="sxs-lookup"><span data-stu-id="4616f-187">Don't use ending punctuation.</span></span>
-   <span data-ttu-id="4616f-188">Veillez à ce que ces étiquettes soient descriptives et balancées.</span><span class="sxs-lookup"><span data-stu-id="4616f-188">Make sure these labels are descriptive and parallel.</span></span> <span data-ttu-id="4616f-189">Exemples : Maximum/Minimum, Plus/Moins, Bas/Haut, Faible/Fort.</span><span class="sxs-lookup"><span data-stu-id="4616f-189">Examples: Maximum/Minimum, More/Less, Low/High, Soft/Loud.</span></span>
-   <span data-ttu-id="4616f-190">Utilisez les majuscules comme pour les phrases.</span><span class="sxs-lookup"><span data-stu-id="4616f-190">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="4616f-191">N’affectez pas de clés d’accès.</span><span class="sxs-lookup"><span data-stu-id="4616f-191">Don't assign access keys.</span></span>

### <a name="value-labels"></a><span data-ttu-id="4616f-192">Étiquettes de valeur</span><span class="sxs-lookup"><span data-stu-id="4616f-192">Value labels</span></span>

-   <span data-ttu-id="4616f-193">Si vous nécessitez une étiquette de valeur, affichez-la sous le curseur.</span><span class="sxs-lookup"><span data-stu-id="4616f-193">If you need a value label, display it below the slider.</span></span>
-   <span data-ttu-id="4616f-194">Centrez le texte relatif au contrôle et ajoutez les unités (telles que pixels).</span><span class="sxs-lookup"><span data-stu-id="4616f-194">Center the text relative to the control and include the units (such as pixels).</span></span>

    ![<span data-ttu-id="4616f-195">figure de l’étiquette centrée sous le curseur</span><span class="sxs-lookup"><span data-stu-id="4616f-195">figure of label centered under the slider</span></span> ](images/ctrl-sliders-image8.png)

    <span data-ttu-id="4616f-196">Dans cet exemple, l’étiquette de valeur est centrée sous le curseur et comprend les unités.</span><span class="sxs-lookup"><span data-stu-id="4616f-196">In this example, the value label is centered under the slider and includes the units.</span></span>

## <a name="documentation"></a><span data-ttu-id="4616f-197">Documentation</span><span class="sxs-lookup"><span data-stu-id="4616f-197">Documentation</span></span>

<span data-ttu-id="4616f-198">Lorsque vous faites référence à des curseurs :</span><span class="sxs-lookup"><span data-stu-id="4616f-198">When referring to sliders:</span></span>

-   <span data-ttu-id="4616f-199">Utilisez le texte d’étiquette exact, y compris sa mise en majuscules, et incluez le curseur de mot.</span><span class="sxs-lookup"><span data-stu-id="4616f-199">Use the exact label text, including its capitalization, and include the word slider.</span></span> <span data-ttu-id="4616f-200">N’incluez pas le trait de soulignement ou le signe deux-points.</span><span class="sxs-lookup"><span data-stu-id="4616f-200">Don't include the access key underscore or colon.</span></span>
-   <span data-ttu-id="4616f-201">Pour décrire l’interaction de l’utilisateur, utilisez Move.</span><span class="sxs-lookup"><span data-stu-id="4616f-201">To describe user interaction, use move.</span></span>
-   <span data-ttu-id="4616f-202">Dans la mesure du possible, mettez en forme l’étiquette à l’aide de texte en gras.</span><span class="sxs-lookup"><span data-stu-id="4616f-202">When possible, format the label using bold text.</span></span> <span data-ttu-id="4616f-203">Sinon, placez l’étiquette entre guillemets uniquement si nécessaire pour éviter toute confusion.</span><span class="sxs-lookup"><span data-stu-id="4616f-203">Otherwise, put the label in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="4616f-204">Exemple : pour augmenter la résolution de l’écran, déplacez le curseur **résolution d’écran** vers la droite.</span><span class="sxs-lookup"><span data-stu-id="4616f-204">Example: To increase your screen resolution, move the **Screen resolution** slider to the right.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4616f-205">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4616f-205">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4616f-206">Glossaire</span><span class="sxs-lookup"><span data-stu-id="4616f-206">Glossary</span></span>](glossary.md)
</dt> </dl>

 

 