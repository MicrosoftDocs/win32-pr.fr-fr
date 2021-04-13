---
title: Contrôles spin
description: Avec un contrôle spin, les utilisateurs peuvent cliquer sur les boutons fléchés pour modifier de manière incrémentielle la valeur dans la zone de texte numérique qui lui est associée.
ms.assetid: 5f791fb9-1354-41b9-a9de-ddab35302d50
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 54ce622983e52d65fa58ef05aca783ff67ebce66
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104321417"
---
# <a name="spin-controls"></a><span data-ttu-id="0ef47-103">Contrôles spin</span><span class="sxs-lookup"><span data-stu-id="0ef47-103">Spin Controls</span></span>

> [!NOTE]
> <span data-ttu-id="0ef47-104">Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows.</span><span class="sxs-lookup"><span data-stu-id="0ef47-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="0ef47-105">La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.</span><span class="sxs-lookup"><span data-stu-id="0ef47-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="0ef47-106">Avec un contrôle spin, les utilisateurs peuvent cliquer sur les boutons fléchés pour modifier de manière incrémentielle la valeur dans la [zone de texte numérique](ctrl-text-boxes.md)qui lui est associée.</span><span class="sxs-lookup"><span data-stu-id="0ef47-106">With a spin control, users can click arrow buttons to change incrementally the value within its associated [numeric text box](ctrl-text-boxes.md).</span></span> <span data-ttu-id="0ef47-107">Le terme zone de sélection numérique fait référence à la combinaison d’une zone de texte et de son contrôle spin associé.</span><span class="sxs-lookup"><span data-stu-id="0ef47-107">The term spin box refers to the combination of a text box and its associated spin control.</span></span>

![<span data-ttu-id="0ef47-108">capture d’écran de la zone de texte et du contrôle spin</span><span class="sxs-lookup"><span data-stu-id="0ef47-108">screen shot of spin control and text box</span></span> ](images/ctrl-spin-controls-image1.png)

<span data-ttu-id="0ef47-109">Zone de sélection numérique classique.</span><span class="sxs-lookup"><span data-stu-id="0ef47-109">A typical spin box.</span></span>

<span data-ttu-id="0ef47-110">Les utilisateurs préfèrent souvent les contrôles spin, car ils peuvent apporter des modifications sans déplacer les mains de la souris.</span><span class="sxs-lookup"><span data-stu-id="0ef47-110">Users often prefer spin controls because they can make changes without moving their hands from the mouse.</span></span> <span data-ttu-id="0ef47-111">Lorsque le contrôle spin est associé à une zone de texte, les utilisateurs peuvent taper ou coller une entrée directement dans la zone de texte, de sorte que l’utilisation du contrôle spin est facultative.</span><span class="sxs-lookup"><span data-stu-id="0ef47-111">When the spin control is paired with a text box, users can type or paste input directly in the text box, so use of the spin control is optional.</span></span>

<span data-ttu-id="0ef47-112">Alors que les contrôles spin sont utilisés pour l’entrée numérique, l’entrée n’a pas besoin d’être un nombre entier pur.</span><span class="sxs-lookup"><span data-stu-id="0ef47-112">While spin controls are used for numeric input, the input doesn't have to be a pure whole number.</span></span> <span data-ttu-id="0ef47-113">L’entrée peut être un nombre décimal et peut avoir des signes négatifs, des délimiteurs (tels que les signes deux-points ou des traits d’Union) et des modificateurs d’unités.</span><span class="sxs-lookup"><span data-stu-id="0ef47-113">The input can be decimal numbers and it can have negative signs, delimiters (such as colons or hyphens), and unit modifiers.</span></span>

> [!Note]  
> <span data-ttu-id="0ef47-114">Les instructions relatives aux [zones de texte](ctrl-text-boxes.md) et à la [mise en page](vis-layout.md) sont présentées dans des articles distincts.</span><span class="sxs-lookup"><span data-stu-id="0ef47-114">Guidelines related to [text boxes](ctrl-text-boxes.md) and [layout](vis-layout.md) are presented in separate articles.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="0ef47-115">Est-ce le contrôle approprié ?</span><span class="sxs-lookup"><span data-stu-id="0ef47-115">Is this the right control?</span></span>

<span data-ttu-id="0ef47-116">Pour vous décider, posez-vous les questions suivantes :</span><span class="sxs-lookup"><span data-stu-id="0ef47-116">To decide, consider these questions:</span></span>

-   <span data-ttu-id="0ef47-117">**Le contrôle est-il utilisé pour les entrées numériques ?**</span><span class="sxs-lookup"><span data-stu-id="0ef47-117">**Is the control used for numeric input?**</span></span> <span data-ttu-id="0ef47-118">Si ce n’est pas le cas, utilisez un autre contrôle, tel qu’une [liste déroulante](/windows/desktop/uxguide/ctrl-drop) ou un [curseur](ctrl-sliders.md), pour effectuer une sélection à partir d’un ensemble fixe de valeurs.</span><span class="sxs-lookup"><span data-stu-id="0ef47-118">If not, use another control, such as a [drop-down list](/windows/desktop/uxguide/ctrl-drop) or [slider](ctrl-sliders.md), to select from a fixed set of values.</span></span> <span data-ttu-id="0ef47-119">Utilisez des barres de défilement pour le défilement.</span><span class="sxs-lookup"><span data-stu-id="0ef47-119">Use scroll bars for scrolling.</span></span>
-   <span data-ttu-id="0ef47-120">**Les utilisateurs considèrent-ils la valeur comme une quantité relative, et non une valeur numérique ?**</span><span class="sxs-lookup"><span data-stu-id="0ef47-120">**Do users think of the value as a relative quantity, not a numeric value?**</span></span> <span data-ttu-id="0ef47-121">Dans ce cas, utilisez un curseur à la place.</span><span class="sxs-lookup"><span data-stu-id="0ef47-121">If so, use a slider instead.</span></span> <span data-ttu-id="0ef47-122">Utilisez des zones de sélection numérique uniquement pour les valeurs numériques exactes et connues.</span><span class="sxs-lookup"><span data-stu-id="0ef47-122">Use spin boxes only for exact, known numeric values.</span></span> <span data-ttu-id="0ef47-123">Par exemple, dans le cas du volume, ils le régleront sur faible ou moyen, et pas sur 2 ou 5.</span><span class="sxs-lookup"><span data-stu-id="0ef47-123">For example, users think about setting their audio volume to low or medium—not about setting the value to 2 or 5.</span></span>
-   <span data-ttu-id="0ef47-124">**Le contrôle est-il associé à une zone de texte ?**</span><span class="sxs-lookup"><span data-stu-id="0ef47-124">**Is the control paired with a text box?**</span></span> <span data-ttu-id="0ef47-125">Si ce n’est pas le cas, n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="0ef47-125">If not, don't use.</span></span> <span data-ttu-id="0ef47-126">Les contrôles spin ne doivent pas être utilisés seuls ou avec d’autres types de contrôles en dehors d’une zone de texte.</span><span class="sxs-lookup"><span data-stu-id="0ef47-126">Spin controls shouldn't be used alone or with other types of controls besides a text box.</span></span>

    <span data-ttu-id="0ef47-127">**Incorrect :**</span><span class="sxs-lookup"><span data-stu-id="0ef47-127">**Incorrect:**</span></span>

    ![<span data-ttu-id="0ef47-128">capture d’écran du contrôle spin, graphique, aucune zone de texte</span><span class="sxs-lookup"><span data-stu-id="0ef47-128">screen shot of spin control, graphic, no text box</span></span> ](images/ctrl-spin-controls-image2.png)

    <span data-ttu-id="0ef47-129">Dans cet exemple, un contrôle spin est utilisé pour contrôler un graphique dynamique.</span><span class="sxs-lookup"><span data-stu-id="0ef47-129">In this example, a spin control is used to control a dynamic graphic.</span></span>

-   <span data-ttu-id="0ef47-130">**Les plages de valeurs contiguës sont-elles valides ?**</span><span class="sxs-lookup"><span data-stu-id="0ef47-130">**Are contiguous value ranges valid?**</span></span> <span data-ttu-id="0ef47-131">Si ce n’est pas le cas, utilisez plutôt une liste déroulante de valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="0ef47-131">If not, use a drop-down list of valid values instead.</span></span>

    ![<span data-ttu-id="0ef47-132">capture d’écran de la liste déroulante</span><span class="sxs-lookup"><span data-stu-id="0ef47-132">screen shot of drop-down list</span></span> ](images/ctrl-spin-controls-image3.png)

    <span data-ttu-id="0ef47-133">Dans cet exemple, tous les lecteurs de disque ne sont pas valides, donc une liste déroulante est un meilleur choix.</span><span class="sxs-lookup"><span data-stu-id="0ef47-133">In this example, not all disk drive numbers are valid, so a drop-down list is a better choice.</span></span>

-   <span data-ttu-id="0ef47-134">**L’utilisation du contrôle spin est-elle pratique ?**</span><span class="sxs-lookup"><span data-stu-id="0ef47-134">**Is using the spin control practical?**</span></span> <span data-ttu-id="0ef47-135">L’utilisation d’un contrôle spin est pratique pour :</span><span class="sxs-lookup"><span data-stu-id="0ef47-135">Using a spin control is practical for:</span></span>

    -   <span data-ttu-id="0ef47-136">En entrant un petit nombre, généralement sous 100.</span><span class="sxs-lookup"><span data-stu-id="0ef47-136">Entering a small number, typically under 100.</span></span>
    -   <span data-ttu-id="0ef47-137">Apporter de petites modifications à une valeur existante ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="0ef47-137">Making small changes to an existing or default value.</span></span>

    <span data-ttu-id="0ef47-138">Alors que les contrôles spin peuvent être utilisés pour n’importe quelle entrée numérique, ils sont inefficaces dans les situations autres que celles-ci.</span><span class="sxs-lookup"><span data-stu-id="0ef47-138">While spin controls can be used for any numeric input, they are inefficient in situations other than these.</span></span>

-   <span data-ttu-id="0ef47-139">**Le contrôle spin est-il utile ?**</span><span class="sxs-lookup"><span data-stu-id="0ef47-139">**Is the spin control helpful?**</span></span> <span data-ttu-id="0ef47-140">Le contrôle est-il utilisé dans un contexte où les utilisateurs sont susceptibles d’utiliser leur souris ?</span><span class="sxs-lookup"><span data-stu-id="0ef47-140">Is the control used in a context where users are likely to be using their mouse?</span></span> <span data-ttu-id="0ef47-141">Si ce n’est pas le cas, envisagez d’utiliser un contrôle spin facultatif.</span><span class="sxs-lookup"><span data-stu-id="0ef47-141">If not, consider a spin control optional.</span></span>
-   <span data-ttu-id="0ef47-142">**Les listes déroulantes des contrôles frères sont-elles ?**</span><span class="sxs-lookup"><span data-stu-id="0ef47-142">**Are the sibling controls drop-down lists?**</span></span> <span data-ttu-id="0ef47-143">S’il existe d’autres listes déroulantes, envisagez d’utiliser une liste déroulante pour la cohérence.</span><span class="sxs-lookup"><span data-stu-id="0ef47-143">If there are other drop-down lists, consider using a drop-down list for consistency.</span></span>

    ![<span data-ttu-id="0ef47-144">capture d’écran de la boîte de dialogue avec des listes déroulantes</span><span class="sxs-lookup"><span data-stu-id="0ef47-144">screen shot of dialog box with drop-down lists</span></span> ](images/ctrl-spin-controls-image4.png)

    <span data-ttu-id="0ef47-145">Dans cet exemple, une zone de sélection numérique peut être utilisée, mais une liste déroulante est utilisée à des fins de cohérence.</span><span class="sxs-lookup"><span data-stu-id="0ef47-145">In this example, a spin box could be used, but a drop-down list is used for consistency.</span></span>

-   <span data-ttu-id="0ef47-146">**Les utilisateurs tactiles ou PEN sont-ils une cible principale ?**</span><span class="sxs-lookup"><span data-stu-id="0ef47-146">**Are touch or pen users a primary target?**</span></span> <span data-ttu-id="0ef47-147">Si c’est le cas, envisagez plutôt d’utiliser une liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="0ef47-147">If so, consider using a drop-down list instead.</span></span> <span data-ttu-id="0ef47-148">Les boutons fléchés dans un contrôle spin sont trop petits pour être utilisés efficacement avec Touch ou un stylet.</span><span class="sxs-lookup"><span data-stu-id="0ef47-148">The arrow buttons in a spin control are too small to be used efficiently with touch or a pen.</span></span>

<span data-ttu-id="0ef47-149">Si un curseur ou une zone de sélection numérique est possible, utilisez une zone de sélection numérique si :</span><span class="sxs-lookup"><span data-stu-id="0ef47-149">If a slider or a spin box is possible, use a spin box if:</span></span>

-   <span data-ttu-id="0ef47-150">l’espace de l’écran est réduit ;</span><span class="sxs-lookup"><span data-stu-id="0ef47-150">Screen space is tight.</span></span>
-   <span data-ttu-id="0ef47-151">Il est probable qu’un utilisateur préfère utiliser le clavier.</span><span class="sxs-lookup"><span data-stu-id="0ef47-151">A user is likely to prefer using the keyboard.</span></span>

<span data-ttu-id="0ef47-152">Utilisez un curseur si :</span><span class="sxs-lookup"><span data-stu-id="0ef47-152">Use a slider if:</span></span>

-   <span data-ttu-id="0ef47-153">les utilisateurs bénéficieront d’un résultat instantané.</span><span class="sxs-lookup"><span data-stu-id="0ef47-153">Users will benefit from instant feedback.</span></span>

## <a name="guidelines"></a><span data-ttu-id="0ef47-154">Consignes</span><span class="sxs-lookup"><span data-stu-id="0ef47-154">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="0ef47-155">Général</span><span class="sxs-lookup"><span data-stu-id="0ef47-155">General</span></span>

-   <span data-ttu-id="0ef47-156">**Utilisez des contrôles spin chaque fois qu’ils sont pratiques et utiles.**</span><span class="sxs-lookup"><span data-stu-id="0ef47-156">**Use spin controls whenever they are practical and helpful.**</span></span> <span data-ttu-id="0ef47-157">[S’agit-il du bon contrôle ?](#is-this-the-right-control)</span><span class="sxs-lookup"><span data-stu-id="0ef47-157">See [Is this the right control?](#is-this-the-right-control)</span></span>

    -   <span data-ttu-id="0ef47-158">**Exception :** Pour être cohérent avec d’autres zones de texte sur la même interface utilisateur, utilisez des contrôles spin même s’ils ne sont pas toujours pratiques.</span><span class="sxs-lookup"><span data-stu-id="0ef47-158">**Exception:** To be consistent with other text boxes on the same user interface (UI), use spin controls even if they aren't always practical.</span></span>

    <span data-ttu-id="0ef47-159">**Correct :**</span><span class="sxs-lookup"><span data-stu-id="0ef47-159">**Correct:**</span></span>

    ![<span data-ttu-id="0ef47-160">capture d’écran des contrôles de rotation du mois, du jour, de l’année</span><span class="sxs-lookup"><span data-stu-id="0ef47-160">screen shot of month, day, year spin controls</span></span> ](images/ctrl-spin-controls-image5.png)

    <span data-ttu-id="0ef47-161">Dans cet exemple, un contrôle spin est utilisé avec le contrôle Year pour des raisons de cohérence, même s’il n’est pas toujours pratique.</span><span class="sxs-lookup"><span data-stu-id="0ef47-161">In this example, a spin control is used with the year control for consistency, even though it isn't always practical.</span></span>

    <span data-ttu-id="0ef47-162">**Incorrect :**</span><span class="sxs-lookup"><span data-stu-id="0ef47-162">**Incorrect:**</span></span>

    ![<span data-ttu-id="0ef47-163">capture d’écran du contrôle spin de l’adresse IP</span><span class="sxs-lookup"><span data-stu-id="0ef47-163">screen shot of ip address spin control</span></span> ](images/ctrl-spin-controls-image6.png)

    <span data-ttu-id="0ef47-164">Dans cet exemple, le contrôle spin est inutilisable.</span><span class="sxs-lookup"><span data-stu-id="0ef47-164">In this example, the spin control is unusable.</span></span>

-   <span data-ttu-id="0ef47-165">**Faites toujours d’un contrôle toupie l' « ami » de la zone de texte.**</span><span class="sxs-lookup"><span data-stu-id="0ef47-165">**Always make a spin control the "buddy" of the text box.**</span></span> <span data-ttu-id="0ef47-166">Cela place le contrôle spin à l’intérieur de la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="0ef47-166">Doing so places the spin control inside the text box.</span></span>

    <span data-ttu-id="0ef47-167">**Correct :**</span><span class="sxs-lookup"><span data-stu-id="0ef47-167">**Correct:**</span></span>

    ![<span data-ttu-id="0ef47-168">capture d’écran du contrôle spin placé à l’intérieur de la zone de texte</span><span class="sxs-lookup"><span data-stu-id="0ef47-168">screen shot of spin control placed inside text box</span></span> ](images/ctrl-spin-controls-image7.png)

    <span data-ttu-id="0ef47-169">**Incorrect :**</span><span class="sxs-lookup"><span data-stu-id="0ef47-169">**Incorrect:**</span></span>

    ![<span data-ttu-id="0ef47-170">capture d’écran du contrôle spin placé en dehors de la zone de texte</span><span class="sxs-lookup"><span data-stu-id="0ef47-170">screen shot of spin control placed outside text box</span></span> ](images/ctrl-spin-controls-image8.png)

    <span data-ttu-id="0ef47-171">Dans l’exemple correct, le contrôle spin est placé à l’intérieur de sa zone de texte associée.</span><span class="sxs-lookup"><span data-stu-id="0ef47-171">In the correct example, the spin control is placed inside its associated text box.</span></span>

-   <span data-ttu-id="0ef47-172">**Désactiver un contrôle spin lorsque sa zone de texte associée est désactivée.**</span><span class="sxs-lookup"><span data-stu-id="0ef47-172">**Disable a spin control when its associated text box is disabled.**</span></span> <span data-ttu-id="0ef47-173">Le contrôle spin est une méthode d’entrée supplémentaire, qui n’est jamais la seule méthode d’entrée.</span><span class="sxs-lookup"><span data-stu-id="0ef47-173">The spin control is a supplemental input method—never the only input method.</span></span>

### <a name="values"></a><span data-ttu-id="0ef47-174">Valeurs</span><span class="sxs-lookup"><span data-stu-id="0ef47-174">Values</span></span>

-   <span data-ttu-id="0ef47-175">**Définissez le bouton du haut pour augmenter la valeur d’une unité et le bouton inférieur pour réduire d’une unité.**</span><span class="sxs-lookup"><span data-stu-id="0ef47-175">**Define the top button to increase the value by one unit and the bottom button to decrease by one unit.**</span></span> <span data-ttu-id="0ef47-176">En règle générale, l’unité est un, mais il doit s’agir de la plus petite modification courante de la valeur.</span><span class="sxs-lookup"><span data-stu-id="0ef47-176">Typically, the unit is one, but it should be the smallest common change in value.</span></span> <span data-ttu-id="0ef47-177">Dans l’idéal, le contrôle spin doit couvrir toutes les valeurs valides et doit être plus pratique que la saisie dans le texte.</span><span class="sxs-lookup"><span data-stu-id="0ef47-177">Ideally, the spin control should cover all valid values, and it should be more convenient than typing in the text.</span></span>

    ![<span data-ttu-id="0ef47-178">capture d’écran du contrôle spin « Margins »</span><span class="sxs-lookup"><span data-stu-id="0ef47-178">screen shot of 'margins' spin control</span></span> ](images/ctrl-spin-controls-image9.png)

    <span data-ttu-id="0ef47-179">Dans cet exemple, le fait de cliquer sur un contrôle spin modifie les valeurs par 1, ce qui correspond à la plus petite modification courante de la valeur.</span><span class="sxs-lookup"><span data-stu-id="0ef47-179">In this example, clicking a spin control changes the values by .1, which is the smallest common change in value.</span></span> <span data-ttu-id="0ef47-180">L’utilisation d’une unité plus petite couvre la plage de valeurs valides, mais rend les contrôles spin inutilisables.</span><span class="sxs-lookup"><span data-stu-id="0ef47-180">Using a smaller unit would cover the range of valid values but make the spin controls unusable.</span></span>

-   <span data-ttu-id="0ef47-181">**Utilisez le contrôle spin pour limiter l’entrée aux valeurs valides.**</span><span class="sxs-lookup"><span data-stu-id="0ef47-181">**Use the spin control to limit input to valid values.**</span></span> <span data-ttu-id="0ef47-182">L’utilisation d’un contrôle spin ne doit jamais aboutir à une valeur incorrecte.</span><span class="sxs-lookup"><span data-stu-id="0ef47-182">Using a spin control should never result in an incorrect value.</span></span>
-   <span data-ttu-id="0ef47-183">**À la fin d’une plage de valeurs valides, redémarrez la plage.**</span><span class="sxs-lookup"><span data-stu-id="0ef47-183">**At the end of a range of valid values, restart the range.**</span></span> <span data-ttu-id="0ef47-184">La métaphore du contrôle spin est que l’utilisateur tourne une roue de valeurs, ce qui est le comportement de type roue.</span><span class="sxs-lookup"><span data-stu-id="0ef47-184">The spin control metaphor is that the user is spinning a wheel of values, hence this wheel-like behavior.</span></span>
    -   <span data-ttu-id="0ef47-185">**Exception :** Ne redémarrez pas la plage si la valeur résultante est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="0ef47-185">**Exception:** Don't restart the range if the resulting value is certain to be incorrect.</span></span>

        ![<span data-ttu-id="0ef47-186">capture d’écran du contrôle spin « nombre de copies »</span><span class="sxs-lookup"><span data-stu-id="0ef47-186">screen shot of 'number of copies' spin control</span></span> ](images/ctrl-spin-controls-image10.png)

        <span data-ttu-id="0ef47-187">Dans cet exemple, le fait de cliquer sur le bouton fléché vers le bas ne redémarre pas la plage (en allant à la valeur maximale), car cette valeur est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="0ef47-187">In this example, clicking the down arrow button doesn't restart the range (by going to the maximum value) because that value is certain to be incorrect.</span></span>

-   <span data-ttu-id="0ef47-188">**Utilisez du texte au lieu de valeurs numériques spéciales.**</span><span class="sxs-lookup"><span data-stu-id="0ef47-188">**Use text instead of special numeric values.**</span></span> <span data-ttu-id="0ef47-189">Autorisez les utilisateurs à faire tourner ces valeurs spéciales au lieu de les connaître et de les taper.</span><span class="sxs-lookup"><span data-stu-id="0ef47-189">Allow users to spin to these special values instead of having to know them and type them in.</span></span>

    ![<span data-ttu-id="0ef47-190">capture d’écran du contrôle spin « mettre en veille après (jamais) »</span><span class="sxs-lookup"><span data-stu-id="0ef47-190">screen shot of 'sleep after (never)' spin control</span></span> ](images/ctrl-spin-controls-image11.png)

    <span data-ttu-id="0ef47-191">Dans cet exemple, n’est jamais une valeur spéciale, mais les utilisateurs peuvent y faire tourner.</span><span class="sxs-lookup"><span data-stu-id="0ef47-191">In this example, Never is a special value but users can spin to it.</span></span>

-   <span data-ttu-id="0ef47-192">**Si la valeur a des délimiteurs, la zone de texte associée doit avoir plusieurs points de focus d’entrée.**</span><span class="sxs-lookup"><span data-stu-id="0ef47-192">**If the value has delimiters, the associated text box should have multiple input focus points.**</span></span> <span data-ttu-id="0ef47-193">Cela permet de manipuler les segments numériques individuellement.</span><span class="sxs-lookup"><span data-stu-id="0ef47-193">Doing so allows the numeric segments to be manipulated individually.</span></span>

    ![<span data-ttu-id="0ef47-194">capture d’écran du contrôle de rotation de l’heure, minutes sélectionnées</span><span class="sxs-lookup"><span data-stu-id="0ef47-194">screen shot of time spin control, minutes selected</span></span> ](images/ctrl-spin-controls-image12.png)

    <span data-ttu-id="0ef47-195">Dans cet exemple, le contrôle spin affecte les valeurs pour les heures, les minutes, les secondes et le matin.</span><span class="sxs-lookup"><span data-stu-id="0ef47-195">In this example, the spin control affects the values for hours, minutes, seconds, and A.M./P.M.—whichever has the focus.</span></span>

-   <span data-ttu-id="0ef47-196">**Si la valeur a des unités, utilisez le contrôle spin pour modifier également ces unités.**</span><span class="sxs-lookup"><span data-stu-id="0ef47-196">**If the value has units, use the spin control to change those units as well.**</span></span>

    ![<span data-ttu-id="0ef47-197">capture d’écran du contrôle de rotation du temps, « a.m. »</span><span class="sxs-lookup"><span data-stu-id="0ef47-197">screen shot of time spin control, 'a.m.'</span></span> <span data-ttu-id="0ef47-198">activé</span><span class="sxs-lookup"><span data-stu-id="0ef47-198">selected</span></span> ](images/ctrl-spin-controls-image13.png)

    <span data-ttu-id="0ef47-199">Dans cet exemple, le contrôle spin peut être utilisé pour modifier des unités.</span><span class="sxs-lookup"><span data-stu-id="0ef47-199">In this example, the spin control can be used to change units.</span></span>

## <a name="labels"></a><span data-ttu-id="0ef47-200">Étiquettes</span><span class="sxs-lookup"><span data-stu-id="0ef47-200">Labels</span></span>

-   <span data-ttu-id="0ef47-201">Appliquez les indications relatives à l’étiquetage de la [zone de texte](ctrl-text-boxes.md) pour étiqueter la zone de texte associée.</span><span class="sxs-lookup"><span data-stu-id="0ef47-201">Apply the [text box labeling](ctrl-text-boxes.md) guidelines to label the associated text box.</span></span> <span data-ttu-id="0ef47-202">Les contrôles spin ne sont jamais étiquetés directement.</span><span class="sxs-lookup"><span data-stu-id="0ef47-202">Spin controls are never labeled directly.</span></span>

## <a name="documentation"></a><span data-ttu-id="0ef47-203">Documentation</span><span class="sxs-lookup"><span data-stu-id="0ef47-203">Documentation</span></span>

<span data-ttu-id="0ef47-204">Quand vous faites référence à des contrôles spin :</span><span class="sxs-lookup"><span data-stu-id="0ef47-204">When referring to spin controls:</span></span>

-   <span data-ttu-id="0ef47-205">Ne faites pas référence aux contrôles spin dans la documentation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0ef47-205">Don't refer to spin controls in user documentation.</span></span> <span data-ttu-id="0ef47-206">Au lieu de cela, reportez-vous à l’étiquette de la zone de texte associée.</span><span class="sxs-lookup"><span data-stu-id="0ef47-206">Instead, refer to the label of the associated text box.</span></span>
-   <span data-ttu-id="0ef47-207">Reportez-vous à des contrôles spin et à des zones de sélection numérique uniquement dans la programmation et dans d’autres documents techniques.</span><span class="sxs-lookup"><span data-stu-id="0ef47-207">Refer to spin controls and spin boxes only in programming and other technical documentation.</span></span>

<span data-ttu-id="0ef47-208">Exemple : dans la zone **Date** , tapez ou sélectionnez la partie de la date que vous souhaitez modifier.</span><span class="sxs-lookup"><span data-stu-id="0ef47-208">Example: In the **Date** box, type or select the part of the date you want to change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ef47-209">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0ef47-209">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ef47-210">Glossaire</span><span class="sxs-lookup"><span data-stu-id="0ef47-210">Glossary</span></span>](glossary.md)
</dt> </dl>

 

 