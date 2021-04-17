---
title: Zones de texte
description: Avec une zone de texte, les utilisateurs peuvent afficher, entrer ou modifier un texte ou une valeur numérique.
ms.assetid: fb8ed262-1451-496d-a3f4-a29af39763bb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 2b5257e9772465f26815abb0f6ecbe0ff357ba4b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104530435"
---
# <a name="text-boxes"></a><span data-ttu-id="34767-103">Zones de texte</span><span class="sxs-lookup"><span data-stu-id="34767-103">Text Boxes</span></span>

> [!NOTE]
> <span data-ttu-id="34767-104">Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows.</span><span class="sxs-lookup"><span data-stu-id="34767-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="34767-105">La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.</span><span class="sxs-lookup"><span data-stu-id="34767-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="34767-106">Avec une zone de texte, les utilisateurs peuvent afficher, entrer ou modifier un texte ou une valeur numérique.</span><span class="sxs-lookup"><span data-stu-id="34767-106">With a text box, users can display, enter, or edit a text or numeric value.</span></span>

![<span data-ttu-id="34767-107">capture d’écran d’une zone de texte et d’une étiquette typiques</span><span class="sxs-lookup"><span data-stu-id="34767-107">screen shot of a typical text box and label</span></span> ](images/ctrl-text-boxes-image1.png)

<span data-ttu-id="34767-108">Zone de texte standard.</span><span class="sxs-lookup"><span data-stu-id="34767-108">A typical text box.</span></span>

> [!Note]  
> <span data-ttu-id="34767-109">Les instructions relatives à la [disposition](vis-layout.md), aux [polices](vis-fonts.md)et aux [bulles](ctrl-balloons.md) sont présentées dans des articles distincts.</span><span class="sxs-lookup"><span data-stu-id="34767-109">Guidelines related to [layout](vis-layout.md), [fonts](vis-fonts.md), and [balloons](ctrl-balloons.md) are presented in separate articles.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="34767-110">Est-ce le contrôle approprié ?</span><span class="sxs-lookup"><span data-stu-id="34767-110">Is this the right control?</span></span>

<span data-ttu-id="34767-111">Pour vous décider, posez-vous les questions suivantes :</span><span class="sxs-lookup"><span data-stu-id="34767-111">To decide, consider these questions:</span></span>

-   <span data-ttu-id="34767-112">**Est-il pratique d’énumérer toutes les valeurs valides efficacement ?**</span><span class="sxs-lookup"><span data-stu-id="34767-112">**Is it practical to enumerate all the valid values efficiently?**</span></span> <span data-ttu-id="34767-113">Dans ce cas, envisagez une [liste de sélection unique](ctrl-list-boxes.md), un [affichage de liste](ctrl-list-views.md) [, une](/windows/desktop/uxguide/ctrl-drop)liste déroulante modifiable, une liste déroulante modifiable ou un [curseur](ctrl-sliders.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="34767-113">If so, consider a [single-selection list](ctrl-list-boxes.md), [list view](ctrl-list-views.md), [drop-down list](/windows/desktop/uxguide/ctrl-drop), editable drop-down list, or [slider](ctrl-sliders.md) instead.</span></span>
-   <span data-ttu-id="34767-114">**Les données valides sont-elles entièrement non restreintes ? Ou les données valides sont-elles uniquement restreintes par le format (longueur restreinte ou types de caractères) ?**</span><span class="sxs-lookup"><span data-stu-id="34767-114">**Is the valid data completely unconstrained? Or is the valid data constrained only by format (constrained length or character types)?**</span></span> <span data-ttu-id="34767-115">Dans ce cas, utilisez une zone de texte.</span><span class="sxs-lookup"><span data-stu-id="34767-115">If so, use a text box.</span></span>
-   <span data-ttu-id="34767-116">**La valeur représente-t-elle un type de données auquel correspond un contrôle courant spécialisé ?**</span><span class="sxs-lookup"><span data-stu-id="34767-116">**Does the value represent a data type that has a specialized common control?**</span></span> <span data-ttu-id="34767-117">Les exemples incluent la date, l’heure ou l’adresse IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="34767-117">Examples include date, time, or IPv4 or IPv6 address.</span></span> <span data-ttu-id="34767-118">Si c’est le cas, utilisez le contrôle approprié, tel qu’un contrôle de date plutôt qu’une zone de texte.</span><span class="sxs-lookup"><span data-stu-id="34767-118">If so, use the appropriate control, such as a date control rather than a text box.</span></span>
-   <span data-ttu-id="34767-119">Si les données sont numériques :</span><span class="sxs-lookup"><span data-stu-id="34767-119">If the data is numeric:</span></span>
    -   <span data-ttu-id="34767-120">**Les utilisateurs perçoivent-ils le paramètre comme une quantité relative ?**</span><span class="sxs-lookup"><span data-stu-id="34767-120">**Do users perceive the setting as a relative quantity?**</span></span> <span data-ttu-id="34767-121">Si tel est le cas, utilisez un curseur.</span><span class="sxs-lookup"><span data-stu-id="34767-121">If so, use a slider.</span></span>
    -   <span data-ttu-id="34767-122">**L’utilisateur va-t-il bénéficier d’un feedback instantané sur l’effet des modifications apportées aux paramètres ?**</span><span class="sxs-lookup"><span data-stu-id="34767-122">**Would the user benefit from instant feedback on the effect of setting changes?**</span></span> <span data-ttu-id="34767-123">Dans ce cas, utilisez un curseur, éventuellement avec une zone de texte.</span><span class="sxs-lookup"><span data-stu-id="34767-123">If so, use a slider, possibly along with a text box.</span></span> <span data-ttu-id="34767-124">Par exemple, les utilisateurs peuvent facilement choisir une couleur à l’aide d’un curseur, car ils peuvent immédiatement voir l’effet des modifications des valeurs de teinte, de saturation ou de luminosité.</span><span class="sxs-lookup"><span data-stu-id="34767-124">For example, users can easily choose a color using a slider because they can immediately see the effect of changes to hue, saturation, or luminosity values.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="34767-125">Principes de conception</span><span class="sxs-lookup"><span data-stu-id="34767-125">Design concepts</span></span>

<span data-ttu-id="34767-126">Bien que les zones de texte présentent l’avantage d’être très souples, elles présentent l’inconvénient d’avoir des contraintes minimales.</span><span class="sxs-lookup"><span data-stu-id="34767-126">While text boxes have the benefit of being very flexible, they have the drawback of having minimal constraints.</span></span> <span data-ttu-id="34767-127">Les seules contraintes sur une zone de texte modifiable sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="34767-127">The only constraints on an editable text box are:</span></span>

-   <span data-ttu-id="34767-128">Vous pouvez éventuellement définir le nombre maximal de caractères.</span><span class="sxs-lookup"><span data-stu-id="34767-128">You can optionally set the maximum number of characters.</span></span>
-   <span data-ttu-id="34767-129">Vous pouvez éventuellement limiter l’entrée aux caractères numériques (0 9) uniquement.</span><span class="sxs-lookup"><span data-stu-id="34767-129">You can optionally restrict input to numeric characters (0   9) only.</span></span>
-   <span data-ttu-id="34767-130">Si vous utilisez un [contrôle spin](ctrl-spin-controls.md), vous pouvez limiter les choix de contrôle spin aux valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="34767-130">If you use a [spin control](ctrl-spin-controls.md), you can limit spin control choices to valid values.</span></span>

<span data-ttu-id="34767-131">Outre leur longueur et la présence facultative d’un contrôle spin, les zones de texte n’ont pas d’indications visuelles qui suggèrent les valeurs valides ou leur format.</span><span class="sxs-lookup"><span data-stu-id="34767-131">Aside from their length and the optional presence of a spin control, text boxes don't have any visual clues that suggest the valid values or their format.</span></span> <span data-ttu-id="34767-132">Cela signifie que vous pouvez utiliser des étiquettes pour communiquer ces informations aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="34767-132">This means relying on labels to convey this information to users.</span></span> <span data-ttu-id="34767-133">Si les utilisateurs entrent du texte qui n’est pas valide, vous devez gérer l’erreur avec un message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="34767-133">If users enter text that's not valid, you must handle the error with an error message.</span></span>

<span data-ttu-id="34767-134">En règle générale, **vous devez utiliser le contrôle le plus restreint que vous pouvez**.</span><span class="sxs-lookup"><span data-stu-id="34767-134">As a general rule, **you should use the most constrained control that you can**.</span></span> <span data-ttu-id="34767-135">Utilisez des contrôles sans contrainte comme des zones de texte en dernier recours.</span><span class="sxs-lookup"><span data-stu-id="34767-135">Use unconstrained controls like text boxes as a last resort.</span></span> <span data-ttu-id="34767-136">Cela dit, lorsque vous envisagez des contraintes, gardez à l’esprit les besoins des utilisateurs généraux.</span><span class="sxs-lookup"><span data-stu-id="34767-136">That said, when you are considering constraints, bear in mind the needs of global users.</span></span> <span data-ttu-id="34767-137">Par exemple, un contrôle qui est contraint à États-Unis codes POSTaux n’est pas globalisé, mais une zone de texte sans contrainte qui accepte n’importe quel format de code postal est.</span><span class="sxs-lookup"><span data-stu-id="34767-137">For example, a control that is constrained to United States ZIP Codes isn't globalized, but an unconstrained text box that accepts any postal code format is.</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="34767-138">Modèles d’usage</span><span class="sxs-lookup"><span data-stu-id="34767-138">Usage patterns</span></span>

<span data-ttu-id="34767-139">Une zone de texte est un contrôle flexible avec plusieurs utilisations possibles.</span><span class="sxs-lookup"><span data-stu-id="34767-139">A text box is a flexible control with several possible uses.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="34767-140"><strong>Entrée de données</strong></span><span class="sxs-lookup"><span data-stu-id="34767-140"><strong>Data input</strong></span></span><br/> <span data-ttu-id="34767-141">Zone de texte à une seule ligne, sans contrainte, utilisée pour entrer ou modifier des chaînes courtes.</span><span class="sxs-lookup"><span data-stu-id="34767-141">A single-line, unconstrained text box used to enter or edit short strings.</span></span><br/></td>
<td><img src="images/ctrl-text-boxes-image2.png" alt="Screen shot of a text box with Display name label " /><br/> <span data-ttu-id="34767-142">Zone de texte à une seule ligne et sans contrainte.</span><span class="sxs-lookup"><span data-stu-id="34767-142">A single-line, unconstrained text box.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34767-143"><strong>Saisie de données mises en forme</strong></span><span class="sxs-lookup"><span data-stu-id="34767-143"><strong>Formatted data input</strong></span></span><br/> <span data-ttu-id="34767-144">Ensemble de zones de texte d’une seule ligne de taille fixe, qui permettent d’entrer des données avec un format spécifique.</span><span class="sxs-lookup"><span data-stu-id="34767-144">A set of short, fixed-sized, single-line text boxes used to enter data with a specific format.</span></span> <br/></td>
<td><img src="images/ctrl-text-boxes-image3.png" alt="Screen shot of a Product key text box " /><br/> <span data-ttu-id="34767-145">Zone de texte utilisée pour l’entrée de données mises en forme.</span><span class="sxs-lookup"><span data-stu-id="34767-145">A text box used for formatted data input.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="34767-146">La fonctionnalité de <a href="glossary.md">fermeture automatique</a> avance automatiquement le focus d’entrée d’une zone de texte à la suivante.</span><span class="sxs-lookup"><span data-stu-id="34767-146">The <a href="glossary.md">auto-exit</a> feature automatically advances the input focus from one text box to the next.</span></span> <span data-ttu-id="34767-147">L’un des inconvénients de cette approche est que les données ne peuvent pas être copiées ou collées en tant qu’unité unique.</span><span class="sxs-lookup"><span data-stu-id="34767-147">One disadvantage to this approach is that the data can't be copied or pasted as a single unit.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34767-148"><strong>Saisie de données assistée</strong></span><span class="sxs-lookup"><span data-stu-id="34767-148"><strong>Assisted data input</strong></span></span><br/> <span data-ttu-id="34767-149">Zone de texte sur une seule ligne, sans contrainte, utilisée pour entrer ou modifier des chaînes, combinée avec un bouton de commande qui aide les utilisateurs à sélectionner des valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="34767-149">A single-line, unconstrained text box used to enter or edit strings, combined with a command button that helps users select valid values.</span></span><br/></td>
<td><img src="images/ctrl-text-boxes-image4.png" alt="Screen shot of text box with Browse button" /><br/> <span data-ttu-id="34767-150">Dans cet exemple, la commande parcourir aide les utilisateurs à sélectionner des valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="34767-150">In this example, the Browse command helps users select valid values.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34767-151"><strong>Entrée textuelle</strong></span><span class="sxs-lookup"><span data-stu-id="34767-151"><strong>Textual input</strong></span></span><br/> <span data-ttu-id="34767-152">Zone de texte multiligne, sans contrainte, utilisée pour entrer ou modifier des chaînes longues.</span><span class="sxs-lookup"><span data-stu-id="34767-152">A multi-line, unconstrained text box used to enter or edit long strings.</span></span> <br/></td>
<td><img src="images/ctrl-text-boxes-image5.png" alt="Screen shot of an Address text box " /><br/> <span data-ttu-id="34767-153">Zone de texte multiligne, sans contrainte.</span><span class="sxs-lookup"><span data-stu-id="34767-153">A multi-line, unconstrained text box.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34767-154"><strong>Entrée numérique</strong></span><span class="sxs-lookup"><span data-stu-id="34767-154"><strong>Numeric input</strong></span></span><br/> <span data-ttu-id="34767-155">Zone de texte à une seule ligne, numérique uniquement utilisée pour entrer ou modifier des nombres, avec un <a href="ctrl-spin-controls.md">contrôle spin</a> facultatif pour faciliter l’entrée à l’aide de la souris.</span><span class="sxs-lookup"><span data-stu-id="34767-155">A single-line, numeric-only text box used to enter or edit numbers, with an optional <a href="ctrl-spin-controls.md">spin control</a> to facilitate mouse-based input.</span></span> <br/></td>
<td><img src="images/ctrl-text-boxes-image6.png" alt="Screen shot of a text box for entering a wait time " /><br/> <span data-ttu-id="34767-156">Zone de texte utilisée pour l’entrée numérique.</span><span class="sxs-lookup"><span data-stu-id="34767-156">A text box used for numeric input.</span></span><br/> <span data-ttu-id="34767-157">La combinaison d’une zone de texte et de son contrôle spin associé est appelée <a href="ctrl-spin-controls.md">zone de sélection numérique</a>.</span><span class="sxs-lookup"><span data-stu-id="34767-157">The combination of a text box and its associated spin control is called a <a href="ctrl-spin-controls.md">spin box</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34767-158"><strong>Saisie du mot de passe et du code confidentiel</strong></span><span class="sxs-lookup"><span data-stu-id="34767-158"><strong>Password and PIN input</strong></span></span><br/> <span data-ttu-id="34767-159">Zone de texte sur une seule ligne, sans contrainte, utilisée pour entrer des mots de passe et des codes confidentiels en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="34767-159">A single-line, unconstrained text box used to enter passwords and PINs securely.</span></span><br/></td>
<td><img src="images/ctrl-text-boxes-image7.png" alt="Screen shot of a Password text box " /><br/> <span data-ttu-id="34767-160">Zone de texte utilisée pour entrer des mots de passe.</span><span class="sxs-lookup"><span data-stu-id="34767-160">A text box used to enter passwords.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34767-161"><strong>Sortie des données</strong></span><span class="sxs-lookup"><span data-stu-id="34767-161"><strong>Data output</strong></span></span><br/> <span data-ttu-id="34767-162">Zone de texte sur une seule ligne, en lecture seule, toujours affichée sans bordure, utilisée pour afficher des chaînes courtes.</span><span class="sxs-lookup"><span data-stu-id="34767-162">A single-line, read-only text box, always displayed without a border, used to display short strings.</span></span> <br/></td>
<td><span data-ttu-id="34767-163">Contrairement au texte statique, les données affichées à l’aide d’une zone de texte peuvent être défilées (utiles si les données sont plus larges que le contrôle), sélectionnées et copiées.</span><span class="sxs-lookup"><span data-stu-id="34767-163">Unlike static text, data displayed using a text box can be scrolled (useful if the data is wider than the control), selected, and copied.</span></span><br/> <img src="images/ctrl-text-boxes-image8.png" alt="Screen shot of a text box showing path to a folder " /><br/> <span data-ttu-id="34767-164">Zone de texte d’une seule ligne, en lecture seule, utilisée pour afficher les données.</span><span class="sxs-lookup"><span data-stu-id="34767-164">A single-line, read-only text box used to display data.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34767-165"><strong>Sortie textuelle</strong></span><span class="sxs-lookup"><span data-stu-id="34767-165"><strong>Textual output</strong></span></span><br/> <span data-ttu-id="34767-166">Zone de texte multiligne en lecture seule utilisée pour afficher des chaînes longues.</span><span class="sxs-lookup"><span data-stu-id="34767-166">A multi-line, read-only text box used to display long strings.</span></span> <br/></td>
<td><img src="images/ctrl-text-boxes-image9.png" alt="Screen shot of a Privacy information text box " /><br/> <span data-ttu-id="34767-167">Zone de texte en lecture seule utilisée pour afficher les données.</span><span class="sxs-lookup"><span data-stu-id="34767-167">A read-only text box used to display data.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a><span data-ttu-id="34767-168">Consignes</span><span class="sxs-lookup"><span data-stu-id="34767-168">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="34767-169">Général</span><span class="sxs-lookup"><span data-stu-id="34767-169">General</span></span>

-   <span data-ttu-id="34767-170">**Lors de la désactivation d’une zone de texte, désactivez également les étiquettes, les étiquettes d’instruction, les contrôles spin et les boutons de commande associés.**</span><span class="sxs-lookup"><span data-stu-id="34767-170">**When disabling a text box, also disable any associated labels, instruction labels, spin controls, and command buttons.**</span></span>
-   <span data-ttu-id="34767-171">**Utilisez la saisie semi-automatique pour aider les utilisateurs à entrer des données susceptibles d’être utilisées à plusieurs reprises**.</span><span class="sxs-lookup"><span data-stu-id="34767-171">**Use auto-complete to help users enter data that is likely to be used repeatedly**.</span></span> <span data-ttu-id="34767-172">Les noms d’utilisateur, les adresses et les noms de fichiers sont des exemples.</span><span class="sxs-lookup"><span data-stu-id="34767-172">Examples include user names, addresses, and file names.</span></span> <span data-ttu-id="34767-173">Toutefois, n’utilisez pas la saisie semi-automatique pour les zones de texte qui peuvent contenir des informations sensibles, telles que des mots de passe, des codes confidentiels, des numéros de carte de crédit ou des informations médicales.</span><span class="sxs-lookup"><span data-stu-id="34767-173">However, don't use auto-complete for text boxes that may contain sensitive information, such as passwords, PINs, credit card numbers, or medical information.</span></span>
-   <span data-ttu-id="34767-174">**Ne faites pas défiler inutilement les utilisateurs.**</span><span class="sxs-lookup"><span data-stu-id="34767-174">**Don't make users scroll unnecessarily.**</span></span> <span data-ttu-id="34767-175">Si vous vous attendez à ce que les données soient plus volumineuses que la zone de texte et que vous puissiez facilement rendre la zone de texte plus grande sans nuire à la disposition, redimensionnez-la pour éviter d’avoir à faire défiler la liste.</span><span class="sxs-lookup"><span data-stu-id="34767-175">If you expect data to be larger than the text box and you can readily make the text box larger without harming the layout, size the box to eliminate the need for scrolling.</span></span>

    <span data-ttu-id="34767-176">**Incorrect :**</span><span class="sxs-lookup"><span data-stu-id="34767-176">**Incorrect:**</span></span>

    ![<span data-ttu-id="34767-177">capture d’écran d’une zone de texte de nom d’ordinateur</span><span class="sxs-lookup"><span data-stu-id="34767-177">screen shot of a computer name text box</span></span> ](images/ctrl-text-boxes-image10.png)

    <span data-ttu-id="34767-178">Dans cet exemple, la zone de texte doit être bien plus longue pour gérer ses données.</span><span class="sxs-lookup"><span data-stu-id="34767-178">In this example, the text box should be made much longer to handle its data.</span></span>

-   <span data-ttu-id="34767-179">Barres de défilement :</span><span class="sxs-lookup"><span data-stu-id="34767-179">Scroll bars:</span></span>
    -   <span data-ttu-id="34767-180">**Ne placez pas de barres de défilement horizontales sur des zones de texte à plusieurs lignes.**</span><span class="sxs-lookup"><span data-stu-id="34767-180">**Don't put horizontal scroll bars on multi-line text boxes.**</span></span> <span data-ttu-id="34767-181">Utilisez à la place le défilement vertical et le retour à la ligne.</span><span class="sxs-lookup"><span data-stu-id="34767-181">Use vertical scrolling and line wrapping instead.</span></span>
    -   <span data-ttu-id="34767-182">**Ne placez pas de barres de défilement sur des zones de texte sur une seule ligne.**</span><span class="sxs-lookup"><span data-stu-id="34767-182">**Don't put any scroll bars on single-line text boxes.**</span></span>
-   <span data-ttu-id="34767-183">**Pour une entrée numérique, vous pouvez utiliser un contrôle spin.**</span><span class="sxs-lookup"><span data-stu-id="34767-183">**For numeric input, you may use a spin control.**</span></span> <span data-ttu-id="34767-184">Pour entrée textuelle, utilisez une liste déroulante ou une liste déroulante modifiable à la place.</span><span class="sxs-lookup"><span data-stu-id="34767-184">For textual input, use a drop-down list or editable drop-down list instead.</span></span>
-   <span data-ttu-id="34767-185">**N’utilisez pas la fonctionnalité de sortie automatique, à l’exception des entrées de données mises en forme.**</span><span class="sxs-lookup"><span data-stu-id="34767-185">**Don't use the auto-exit feature except for formatted data input.**</span></span> <span data-ttu-id="34767-186">Le déplacement automatique du Focus peut surprendre en surprise les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="34767-186">The automatic shift of focus can surprise users.</span></span>

### <a name="editable-text-boxes"></a><span data-ttu-id="34767-187">Zones de texte modifiables</span><span class="sxs-lookup"><span data-stu-id="34767-187">Editable text boxes</span></span>

-   <span data-ttu-id="34767-188">**Lorsque vous le pouvez, limitez la longueur du texte d’entrée.**</span><span class="sxs-lookup"><span data-stu-id="34767-188">**Limit the length of the input text when you can.**</span></span> <span data-ttu-id="34767-189">Par exemple, si l’entrée valide est un nombre compris entre 0 et 999, utilisez une zone de texte numérique limitée à trois caractères.</span><span class="sxs-lookup"><span data-stu-id="34767-189">For example, if the valid input is a number between 0 and 999, use a numeric text box that is limited to three characters.</span></span> <span data-ttu-id="34767-190">Toutes les parties de zones de texte qui utilisent une entrée de données mises en forme doivent avoir une longueur fixe brève.</span><span class="sxs-lookup"><span data-stu-id="34767-190">All parts of text boxes that use formatted data input must have a short, fixed length.</span></span>
-   <span data-ttu-id="34767-191">**Soyez flexible avec les formats de données.**</span><span class="sxs-lookup"><span data-stu-id="34767-191">**Be flexible with data formats.**</span></span> <span data-ttu-id="34767-192">Si les utilisateurs sont susceptibles de saisir du texte à l’aide d’un grand nombre de formats, essayez de gérer tous les types les plus courants.</span><span class="sxs-lookup"><span data-stu-id="34767-192">If users are likely to enter text using a wide variety of formats, try to handle all the most common ones.</span></span> <span data-ttu-id="34767-193">Par exemple, de nombreux noms, chiffres et identificateurs peuvent être entrés avec des espaces et des signes de ponctuation facultatifs, et la mise en majuscules n’a souvent pas d’importance.</span><span class="sxs-lookup"><span data-stu-id="34767-193">For example, many names, numbers, and identifiers can be entered with optional spaces and punctuation, and the capitalization often doesn't matter.</span></span>
-   <span data-ttu-id="34767-194">Si vous ne pouvez pas gérer les formats probables, vous devez utiliser un format spécifique à l’aide d’une entrée de données mises en forme ou indiquer les formats valides dans l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="34767-194">If you can't handle the likely formats, require a specific format by using formatted data input or indicate the valid formats in the label.</span></span>

    <span data-ttu-id="34767-195">**Acceptable:**</span><span class="sxs-lookup"><span data-stu-id="34767-195">**Acceptable:**</span></span>

    ![<span data-ttu-id="34767-196">capture d’écran d’une zone de texte pour une entrée numérique</span><span class="sxs-lookup"><span data-stu-id="34767-196">screen shot of a text box for numeric input</span></span> ](images/ctrl-text-boxes-image11.png)

    <span data-ttu-id="34767-197">Dans cet exemple, une zone de texte requiert une entrée dans un format spécifique.</span><span class="sxs-lookup"><span data-stu-id="34767-197">In this example, a text box requires input in a specific format.</span></span>

    <span data-ttu-id="34767-198">**Conseillé**</span><span class="sxs-lookup"><span data-stu-id="34767-198">**Better:**</span></span>

    ![<span data-ttu-id="34767-199">capture d’écran de la zone de texte entrée des données mises en forme</span><span class="sxs-lookup"><span data-stu-id="34767-199">screen shot of formatted data input text box</span></span> ](images/ctrl-text-boxes-image12.png)

    <span data-ttu-id="34767-200">Dans cet exemple, le modèle d’entrée de données mis en forme est utilisé pour exiger un format spécifique.</span><span class="sxs-lookup"><span data-stu-id="34767-200">In this example, the formatted data input pattern is used to require a specific format.</span></span>

    <span data-ttu-id="34767-201">**Meilleures**</span><span class="sxs-lookup"><span data-stu-id="34767-201">**Best:**</span></span>

    ![<span data-ttu-id="34767-202">capture d’écran d’une zone de texte sans contrainte</span><span class="sxs-lookup"><span data-stu-id="34767-202">screen shot of an unconstrained text box</span></span> ](images/ctrl-text-boxes-image13.png)

    <span data-ttu-id="34767-203">Dans cet exemple, une zone de texte gère tous les formats probables.</span><span class="sxs-lookup"><span data-stu-id="34767-203">In this example, a text box handles all likely formats.</span></span>

-   <span data-ttu-id="34767-204">Tenez compte de la flexibilité de mise en forme lors du choix de la longueur d’entrée maximale.</span><span class="sxs-lookup"><span data-stu-id="34767-204">Consider format flexibility when choosing the maximum input length.</span></span> <span data-ttu-id="34767-205">Par exemple, un numéro de carte de crédit valide peut utiliser jusqu’à 19 caractères, ce qui permet de limiter la longueur à toute valeur plus petite, ce qui rend difficile l’entrée de nombres à l’aide des formats plus longs.</span><span class="sxs-lookup"><span data-stu-id="34767-205">For example, a valid credit card number can use up to 19 characters so limiting the length to anything shorter would make it difficult to enter numbers using the longer formats.</span></span>
-   <span data-ttu-id="34767-206">**N’utilisez pas le modèle d’entrée de données mis en forme si les utilisateurs sont plus susceptibles de coller des données longues et complexes.**</span><span class="sxs-lookup"><span data-stu-id="34767-206">**Don't use the formatted data input pattern if users are more likely to paste in long, complex data.**</span></span> <span data-ttu-id="34767-207">Au lieu de cela, réservez le modèle d’entrée de données mis en forme pour les situations où les utilisateurs sont plus susceptibles de saisir les données.</span><span class="sxs-lookup"><span data-stu-id="34767-207">Rather, reserve the formatted data input pattern for situations where users are more likely to type the data.</span></span>

    ![<span data-ttu-id="34767-208">capture d’écran d’une zone de texte avec étiquette : adresse IPv6</span><span class="sxs-lookup"><span data-stu-id="34767-208">screen shot of a text box with label: ipv6 address</span></span> ](images/ctrl-text-boxes-image14.png)

    <span data-ttu-id="34767-209">Dans cet exemple, le modèle d’entrée de données mis en forme n’est pas utilisé, afin que les utilisateurs puissent coller des adresses IPv6.</span><span class="sxs-lookup"><span data-stu-id="34767-209">In this example, the formatted data input pattern isn't used, so that users can to paste IPv6 addresses.</span></span>

-   <span data-ttu-id="34767-210">**Si les utilisateurs sont plus susceptibles de ressaisir la valeur entière, sélectionnez tout le texte sur le focus d’entrée.**</span><span class="sxs-lookup"><span data-stu-id="34767-210">**If users are more likely going to reenter the entire value, select all the text on input focus.**</span></span> <span data-ttu-id="34767-211">Si les utilisateurs sont plus susceptibles de modifier, placez le signe insertion à la fin du texte.</span><span class="sxs-lookup"><span data-stu-id="34767-211">If users are more likely to edit, place the caret at the end of the text.</span></span>

    ![<span data-ttu-id="34767-212">capture d’écran d’une zone de texte de mot de passe</span><span class="sxs-lookup"><span data-stu-id="34767-212">screen shot of a password text box</span></span> ](images/ctrl-text-boxes-image15.png)

    <span data-ttu-id="34767-213">Dans cet exemple, il est plus probable que les utilisateurs remplacent la modification, donc la valeur entière est sélectionnée dans le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="34767-213">In this example, users are more likely to replace than edit, so the entire value is selected on input focus.</span></span>

    ![<span data-ttu-id="34767-214">capture d’écran d’une zone de texte pour la saisie de mots clés</span><span class="sxs-lookup"><span data-stu-id="34767-214">screen shot of a text box for entering keywords</span></span> ](images/ctrl-text-boxes-image16.png)

    <span data-ttu-id="34767-215">Dans cet exemple, les utilisateurs sont plus susceptibles d’ajouter des mots clés que de remplacer le texte ; le signe insertion est donc placé à la fin du texte.</span><span class="sxs-lookup"><span data-stu-id="34767-215">In this example, users are more likely to add keywords than replace the text, so the caret is placed at the end of the text.</span></span>

-   <span data-ttu-id="34767-216">**Utilisez toujours une zone de texte multiligne si les caractères de nouvelle ligne sont des entrées valides.**</span><span class="sxs-lookup"><span data-stu-id="34767-216">**Always use a multi-line text box if new-line characters are valid input.**</span></span>
-   <span data-ttu-id="34767-217">**Lorsque la zone de texte correspond à un fichier ou à un chemin d’accès, indiquez toujours un bouton Parcourir.**</span><span class="sxs-lookup"><span data-stu-id="34767-217">**When the text box is for a file or path, always provide a Browse button.**</span></span>

### <a name="numeric-text-boxes"></a><span data-ttu-id="34767-218">Zones de texte numériques</span><span class="sxs-lookup"><span data-stu-id="34767-218">Numeric text boxes</span></span>

-   <span data-ttu-id="34767-219">**Choisissez l’unité la plus pratique et étiquetez les unités.**</span><span class="sxs-lookup"><span data-stu-id="34767-219">**Choose the most convenient unit and label the units.**</span></span> <span data-ttu-id="34767-220">Par exemple, envisagez d’utiliser milliliters au lieu de litres (ou vice versa), des pourcentages au lieu de valeurs directes (ou vice versa), etc.</span><span class="sxs-lookup"><span data-stu-id="34767-220">For example, consider using milliliters instead of liters (or vice versa), percentages instead of direct values (or vice versa), and so on.</span></span>

    <span data-ttu-id="34767-221">**Correct :**</span><span class="sxs-lookup"><span data-stu-id="34767-221">**Correct:**</span></span>

    ![<span data-ttu-id="34767-222">capture d’écran de la zone de texte avec litres comme unité</span><span class="sxs-lookup"><span data-stu-id="34767-222">screen shot of text box with liters as unit</span></span> ](images/ctrl-text-boxes-image17.png)

    <span data-ttu-id="34767-223">Dans cet exemple, l’unité est étiquetée, mais elle nécessite que les utilisateurs entrent des nombres décimaux.</span><span class="sxs-lookup"><span data-stu-id="34767-223">In this example, the unit is labeled, but it requires users to enter decimal numbers.</span></span>

    <span data-ttu-id="34767-224">**Conseillé**</span><span class="sxs-lookup"><span data-stu-id="34767-224">**Better:**</span></span>

    ![<span data-ttu-id="34767-225">capture d’écran de la zone de texte avec milliliters en tant qu’unité</span><span class="sxs-lookup"><span data-stu-id="34767-225">screen shot of text box with milliliters as unit</span></span> ](images/ctrl-text-boxes-image18.png)

    <span data-ttu-id="34767-226">Dans cet exemple, la zone de texte utilise une unité plus pratique.</span><span class="sxs-lookup"><span data-stu-id="34767-226">In this example, the text box uses a more convenient unit.</span></span>

-   <span data-ttu-id="34767-227">**Utilisez un contrôle spin à chaque fois qu’il est utile.**</span><span class="sxs-lookup"><span data-stu-id="34767-227">**Use a spin control whenever it is helpful.**</span></span> <span data-ttu-id="34767-228">Toutefois, parfois, les contrôles spin ne sont pas pratiques, par exemple lorsque les utilisateurs doivent entrer un grand nombre de grands nombres.</span><span class="sxs-lookup"><span data-stu-id="34767-228">However, sometimes spin controls aren't practical, such as when users need to enter many large numbers.</span></span> <span data-ttu-id="34767-229">Utilisez des contrôles spin dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="34767-229">Use spin controls when:</span></span>
    -   <span data-ttu-id="34767-230">L’entrée est probablement un petit nombre, généralement sous 100.</span><span class="sxs-lookup"><span data-stu-id="34767-230">The input is likely to be a small number, typically under 100.</span></span>
    -   <span data-ttu-id="34767-231">Les utilisateurs sont susceptibles d’apporter une petite modification à un nombre existant.</span><span class="sxs-lookup"><span data-stu-id="34767-231">Users are likely to make a small change to an existing number.</span></span>
    -   <span data-ttu-id="34767-232">Les utilisateurs sont plus susceptibles d’utiliser la souris que le clavier.</span><span class="sxs-lookup"><span data-stu-id="34767-232">Users are more likely to be using the mouse than the keyboard.</span></span>
-   <span data-ttu-id="34767-233">**Aligner le texte numérique à droite chaque fois :**</span><span class="sxs-lookup"><span data-stu-id="34767-233">**Right-align numeric text whenever:**</span></span>

    -   <span data-ttu-id="34767-234">Il existe plusieurs zones de texte numériques.</span><span class="sxs-lookup"><span data-stu-id="34767-234">There is more than one numeric text box.</span></span>
    -   <span data-ttu-id="34767-235">Les zones de texte sont alignées verticalement.</span><span class="sxs-lookup"><span data-stu-id="34767-235">The text boxes are vertically aligned.</span></span>
    -   <span data-ttu-id="34767-236">Les utilisateurs sont susceptibles d’ajouter ou de comparer les valeurs.</span><span class="sxs-lookup"><span data-stu-id="34767-236">Users are likely to add or compare the values.</span></span>

    <span data-ttu-id="34767-237">**Correct :**</span><span class="sxs-lookup"><span data-stu-id="34767-237">**Correct:**</span></span>

    ![<span data-ttu-id="34767-238">capture d’écran des zones de texte des frais (hôtel, etc.)</span><span class="sxs-lookup"><span data-stu-id="34767-238">screen shot of expenses text boxes (hotel, etc.)</span></span> ](images/ctrl-text-boxes-image19.png)

    <span data-ttu-id="34767-239">Dans cet exemple, le texte numérique est aligné à droite pour faciliter la comparaison des valeurs.</span><span class="sxs-lookup"><span data-stu-id="34767-239">In this example, the numeric text is right-aligned to make it easy to compare values.</span></span>

    <span data-ttu-id="34767-240">**Incorrect :**</span><span class="sxs-lookup"><span data-stu-id="34767-240">**Incorrect:**</span></span>

    ![<span data-ttu-id="34767-241">capture d’écran des zones de texte pour les valeurs RVB</span><span class="sxs-lookup"><span data-stu-id="34767-241">screen shot of text boxes for rgb values</span></span> ](images/ctrl-text-boxes-image20.png)

    <span data-ttu-id="34767-242">Dans cet exemple, le texte numérique est aligné à gauche de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="34767-242">In this example, the numeric text is incorrectly left-aligned.</span></span>

-   <span data-ttu-id="34767-243">**Aligner toujours à droite les valeurs monétaires.**</span><span class="sxs-lookup"><span data-stu-id="34767-243">**Always right-align monetary values.**</span></span>
-   <span data-ttu-id="34767-244">**N’affectez pas de significations particulières à des valeurs numériques spécifiques**, même si ces significations particulières sont utilisées en interne par votre application.</span><span class="sxs-lookup"><span data-stu-id="34767-244">**Don't assign special meanings to specific numeric values**, even if those special meanings are used internally by your application.</span></span> <span data-ttu-id="34767-245">Utilisez plutôt des cases à cocher ou des cases d’option pour une sélection explicite de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="34767-245">Instead, use check boxes or radio buttons for an explicit user selection.</span></span>

    <span data-ttu-id="34767-246">**Incorrect :**</span><span class="sxs-lookup"><span data-stu-id="34767-246">**Incorrect:**</span></span>

    ![<span data-ttu-id="34767-247">capture d’écran de l’étiquette : utilisez-1 pour désactiver la mise en cache</span><span class="sxs-lookup"><span data-stu-id="34767-247">screen shot of label: use -1 to disable caching</span></span> ](images/ctrl-text-boxes-image21.png)

    <span data-ttu-id="34767-248">Dans cet exemple, la valeur-1 a une signification particulière.</span><span class="sxs-lookup"><span data-stu-id="34767-248">In this example, the value -1 has a special meaning.</span></span>

    <span data-ttu-id="34767-249">**Correct :**</span><span class="sxs-lookup"><span data-stu-id="34767-249">**Correct:**</span></span>

    ![<span data-ttu-id="34767-250">capture d’écran de l’étiquette de case à cocher : Caching</span><span class="sxs-lookup"><span data-stu-id="34767-250">screen shot of check box label: caching</span></span> ](images/ctrl-text-boxes-image22.png)

    <span data-ttu-id="34767-251">Dans cet exemple, une case à cocher rend l’option explicite.</span><span class="sxs-lookup"><span data-stu-id="34767-251">In this example, a check box makes the option explicit.</span></span>

### <a name="password-and-pin-input"></a><span data-ttu-id="34767-252">Saisie du mot de passe et du code confidentiel</span><span class="sxs-lookup"><span data-stu-id="34767-252">Password and PIN input</span></span>

-   <span data-ttu-id="34767-253">**Utilisez toujours le contrôle commun de mot de passe au lieu de créer le vôtre.**</span><span class="sxs-lookup"><span data-stu-id="34767-253">**Always use the password common control instead of creating your own.**</span></span> <span data-ttu-id="34767-254">Les mots de passe et les codes confidentiels nécessitent un traitement spécial pour être gérés en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="34767-254">Passwords and PINs require special treatment to be handled securely.</span></span>

<span data-ttu-id="34767-255">Pour obtenir des instructions et des exemples supplémentaires, consultez [bulles](ctrl-balloons.md).</span><span class="sxs-lookup"><span data-stu-id="34767-255">For more guidelines and examples, see [Balloons](ctrl-balloons.md).</span></span>

### <a name="textual-output"></a><span data-ttu-id="34767-256">Sortie textuelle</span><span class="sxs-lookup"><span data-stu-id="34767-256">Textual output</span></span>

-   <span data-ttu-id="34767-257">**Envisagez d’utiliser la couleur du système d’arrière-plan blanc pour du texte en lecture seule à plusieurs lignes.**</span><span class="sxs-lookup"><span data-stu-id="34767-257">**Consider using the white background system color for large, multi-line read-only text.**</span></span> <span data-ttu-id="34767-258">Un arrière-plan blanc rend le texte plus facile à lire.</span><span class="sxs-lookup"><span data-stu-id="34767-258">A white background makes the text easier to read.</span></span> <span data-ttu-id="34767-259">Un grand nombre de texte sur un arrière-plan gris découragent la lecture.</span><span class="sxs-lookup"><span data-stu-id="34767-259">Lots of text on a gray background discourages reading.</span></span>

<span data-ttu-id="34767-260">Pour plus d’informations sur les couleurs d’arrière-plan, consultez [polices](vis-fonts.md).</span><span class="sxs-lookup"><span data-stu-id="34767-260">For more information on background colors, see [Fonts](vis-fonts.md).</span></span>

### <a name="data-output"></a><span data-ttu-id="34767-261">Sortie des données</span><span class="sxs-lookup"><span data-stu-id="34767-261">Data output</span></span>

-   <span data-ttu-id="34767-262">**N’utilisez pas de bordure pour les zones de texte à une seule ligne et en lecture seule.**</span><span class="sxs-lookup"><span data-stu-id="34767-262">**Don't use a border for single-line, read-only text boxes.**</span></span> <span data-ttu-id="34767-263">La bordure est un indice visuel indiquant que le texte est modifiable.</span><span class="sxs-lookup"><span data-stu-id="34767-263">The border is a visual clue that the text is editable.</span></span>
-   <span data-ttu-id="34767-264">**Ne désactivez pas les zones de texte en lecture seule sur une seule ligne.**</span><span class="sxs-lookup"><span data-stu-id="34767-264">**Don't disable single-line, read-only text boxes.**</span></span> <span data-ttu-id="34767-265">Cela empêche les utilisateurs de sélectionner et de copier le texte dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="34767-265">This prevents users from selecting and copying the text to the clipboard.</span></span> <span data-ttu-id="34767-266">Il empêche également les utilisateurs de faire défiler les données si elles dépassent la taille de leurs limites.</span><span class="sxs-lookup"><span data-stu-id="34767-266">It also prevents users from scrolling the data if it exceeds the size of its boundaries.</span></span>
-   <span data-ttu-id="34767-267">**Ne définissez pas de taquet de tabulation sur une seule ligne, zone de texte en lecture seule, à moins que l’utilisateur ait besoin de faire défiler ou de copier le texte.**</span><span class="sxs-lookup"><span data-stu-id="34767-267">**Don't set a tab stop on single-line, read-only text box unless the user is likely to need to scroll or copy the text.**</span></span>

## <a name="input-validation-and-error-handling"></a><span data-ttu-id="34767-268">Validation des entrées et gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="34767-268">Input validation and error handling</span></span>

<span data-ttu-id="34767-269">Étant donné que les zones de texte ne sont généralement pas converties pour accepter uniquement des entrées valides, vous devrez peut-être valider l’entrée et gérer les problèmes éventuels.</span><span class="sxs-lookup"><span data-stu-id="34767-269">Because text boxes are usually not constrained to accept only valid input, you may need to validate the input and handle any problems.</span></span> <span data-ttu-id="34767-270">Validez les différents types de problèmes d’entrée comme suit :</span><span class="sxs-lookup"><span data-stu-id="34767-270">Validate the various types of input problems as follows:</span></span>

-   <span data-ttu-id="34767-271">Si l’utilisateur entre un caractère qui n’est pas valide, ignorez le caractère et affichez une [bulle de problème d’entrée](ctrl-balloons.md) qui explique les caractères valides.</span><span class="sxs-lookup"><span data-stu-id="34767-271">If the user enters a character that isn't valid, ignore the character and display an [input problem balloon](ctrl-balloons.md) that explains the valid characters.</span></span>

    ![capture d’écran de la zone de texte clé de produit](images/ctrl-text-boxes-image23.png)

    <span data-ttu-id="34767-273">Dans cet exemple, une bulle signale un caractère d’entrée incorrect.</span><span class="sxs-lookup"><span data-stu-id="34767-273">In this example, a balloon reports an incorrect input character.</span></span>

-   <span data-ttu-id="34767-274">Si les données d’entrée ont une valeur ou un format qui n’est pas valide, affichez une bulle de problème d’entrée lorsque la zone de texte perd le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="34767-274">If the input data has a value or format that isn't valid, display an input problem balloon when the text box loses input focus.</span></span>
-   <span data-ttu-id="34767-275">Si les données d’entrée ne sont pas cohérentes avec les autres contrôles de la fenêtre, affichez un message d’erreur lorsque la totalité de l’entrée est complète, par exemple lorsque les utilisateurs cliquent sur OK pour obtenir une boîte de dialogue modale.</span><span class="sxs-lookup"><span data-stu-id="34767-275">If the input data is inconsistent with other controls on the window, give an error message when the entire input is complete, such as when users click OK for a modal dialog box.</span></span>

<span data-ttu-id="34767-276">**Ne supprimez pas les données d’entrée non valides, sauf si les utilisateurs ne peuvent pas facilement corriger les erreurs.**</span><span class="sxs-lookup"><span data-stu-id="34767-276">**Don't clear invalid input data unless users aren't able to correct errors easily.**</span></span> <span data-ttu-id="34767-277">Cela permet aux utilisateurs de corriger les erreurs sans recommencer.</span><span class="sxs-lookup"><span data-stu-id="34767-277">Doing so allows users to correct mistakes without starting over.</span></span> <span data-ttu-id="34767-278">Par exemple, vous devez effacer les codes confidentiels et les mots de passe incorrects, car les utilisateurs ne peuvent pas les corriger facilement.</span><span class="sxs-lookup"><span data-stu-id="34767-278">For example, you should clear incorrect passwords and PINs because users can't correct them easily.</span></span>

<span data-ttu-id="34767-279">Pour obtenir des instructions et des exemples supplémentaires, consultez [messages d’erreur](mess-error.md) et [bulles](ctrl-balloons.md).</span><span class="sxs-lookup"><span data-stu-id="34767-279">For more guidelines and examples, see [Error Messages](mess-error.md) and [Balloons](ctrl-balloons.md).</span></span>

## <a name="prompts"></a><span data-ttu-id="34767-280">Invites</span><span class="sxs-lookup"><span data-stu-id="34767-280">Prompts</span></span>

<span data-ttu-id="34767-281">Une invite est une étiquette ou une brève instruction placée dans une zone de texte comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="34767-281">A prompt is a label or short instruction placed inside a text box as its default value.</span></span> <span data-ttu-id="34767-282">Contrairement au texte statique, les invites disparaissent de l’écran une fois que les utilisateurs ont tapé un texte dans la zone de texte ou qu’il obtient le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="34767-282">Unlike static text, prompts disappear from the screen once users type something into the text box or it gets input focus.</span></span>

![<span data-ttu-id="34767-283">capture d’écran de la zone de texte d’invite avec étiquette : Rechercher</span><span class="sxs-lookup"><span data-stu-id="34767-283">screen shot of prompt text box with label: search</span></span> ](images/ctrl-text-boxes-image24.png)

<span data-ttu-id="34767-284">Invite classique.</span><span class="sxs-lookup"><span data-stu-id="34767-284">A typical prompt.</span></span>

<span data-ttu-id="34767-285">Utilisez une invite dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="34767-285">Use a prompt when:</span></span>

-   <span data-ttu-id="34767-286">L’espace à l’écran est d’une qualité telle que l’utilisation d’une étiquette ou d’une instruction n’est pas souhaitable, par exemple dans une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="34767-286">Screen space is at such a premium that using a label or instruction is undesirable, such as on a toolbar.</span></span>
-   <span data-ttu-id="34767-287">L’invite est principalement destinée à identifier l’objectif de la zone de texte de manière compacte.</span><span class="sxs-lookup"><span data-stu-id="34767-287">The prompt is primarily for identifying the purpose of the text box in a compact way.</span></span> <span data-ttu-id="34767-288">Il ne doit pas s’agir d’informations essentielles que l’utilisateur doit voir lors de l’utilisation de la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="34767-288">It must not be crucial information that the user needs to see while using the text box.</span></span>

<span data-ttu-id="34767-289">N’utilisez pas les invites uniquement pour demander aux utilisateurs de taper un texte ou de cliquer sur les boutons.</span><span class="sxs-lookup"><span data-stu-id="34767-289">Don't use prompts just to direct users to type something or to click buttons.</span></span> <span data-ttu-id="34767-290">Par exemple, n’écrivez pas de texte d’invite indiquant entrez un nom de fichier, puis cliquez sur Envoyer.</span><span class="sxs-lookup"><span data-stu-id="34767-290">For example, don't write prompt text that says Enter a filename and then click Send.</span></span>

<span data-ttu-id="34767-291">Quand vous utilisez des invites :</span><span class="sxs-lookup"><span data-stu-id="34767-291">When using prompts:</span></span>

-   <span data-ttu-id="34767-292">Dessinez le texte de l’invite en italique gris et le texte d’entrée réel en noir normal.</span><span class="sxs-lookup"><span data-stu-id="34767-292">Draw the prompt text in italic gray and the actual input text in normal black.</span></span> <span data-ttu-id="34767-293">Le texte de l’invite ne doit pas être confondu avec du texte réel.</span><span class="sxs-lookup"><span data-stu-id="34767-293">The prompt text must not be confused with real text.</span></span>
-   <span data-ttu-id="34767-294">Conservez le texte de l’invite concis.</span><span class="sxs-lookup"><span data-stu-id="34767-294">Keep the prompt text concise.</span></span> <span data-ttu-id="34767-295">Vous pouvez utiliser des fragments au lieu de phrases entières.</span><span class="sxs-lookup"><span data-stu-id="34767-295">You can use fragments instead of full sentences.</span></span>
-   <span data-ttu-id="34767-296">Utilisez les majuscules comme pour les phrases.</span><span class="sxs-lookup"><span data-stu-id="34767-296">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="34767-297">N’utilisez pas de ponctuation de fin ni de points de suspension.</span><span class="sxs-lookup"><span data-stu-id="34767-297">Don't use ending punctuation or ellipsis.</span></span>
-   <span data-ttu-id="34767-298">Le texte de l’invite ne doit pas être modifiable et doit disparaître une fois que les utilisateurs cliquent dans ou sur l’onglet dans la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="34767-298">The prompt text should not be editable and should disappear once users click in or tab into the text box.</span></span>
    -   <span data-ttu-id="34767-299">**Exception :** Si la zone de texte a le focus d’entrée par défaut, l’invite s’affiche et disparaît lorsque l’utilisateur commence à taper.</span><span class="sxs-lookup"><span data-stu-id="34767-299">**Exception:** If the text box has default input focus, the prompt is displayed, and it disappears once the user starts typing.</span></span>
-   <span data-ttu-id="34767-300">Le texte d’invite est restauré si la zone de texte est toujours vide lorsqu’il perd le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="34767-300">The prompt text is restored if the text box is still empty when it loses input focus.</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="34767-301">Dimensionnement et espacement recommandés</span><span class="sxs-lookup"><span data-stu-id="34767-301">Recommended sizing and spacing</span></span>

![<span data-ttu-id="34767-302">Figure des zones de texte d’une ligne et de deux lignes</span><span class="sxs-lookup"><span data-stu-id="34767-302">figure of one-line and two-line text boxes</span></span> ](images/ctrl-text-boxes-image25.png)

<span data-ttu-id="34767-303">Dimensionnement et espacement recommandés pour les zones de texte.</span><span class="sxs-lookup"><span data-stu-id="34767-303">Recommended sizing and spacing for text boxes.</span></span>

<span data-ttu-id="34767-304">La largeur d’une zone de texte est un indice visuel de la taille d’entrée attendue.</span><span class="sxs-lookup"><span data-stu-id="34767-304">The width of a text box is a visual clue of the expected input size.</span></span> <span data-ttu-id="34767-305">Lors du dimensionnement des zones de texte :</span><span class="sxs-lookup"><span data-stu-id="34767-305">When sizing text boxes:</span></span>

-   <span data-ttu-id="34767-306">**Choisissez une largeur appropriée pour les données valides les plus longues.**</span><span class="sxs-lookup"><span data-stu-id="34767-306">**Choose a width appropriate for the longest valid data.**</span></span> <span data-ttu-id="34767-307">Dans la plupart des cas, les utilisateurs ne doivent pas avoir à faire défiler la chaîne la plus longue possible qu’ils entrent ou affichent.</span><span class="sxs-lookup"><span data-stu-id="34767-307">In most situations, users shouldn't have to scroll the longest likely string they'll enter or view.</span></span>
-   <span data-ttu-id="34767-308">**Incluez 30 pour cent supplémentaires** (jusqu’à 200 pour cent pour du texte plus petit) pour tout texte (mais pas les nombres) qui sera localisé.</span><span class="sxs-lookup"><span data-stu-id="34767-308">**Include an additional 30 percent** (up to 200 percent for shorter text) for any text (but not numbers) that will be localized.</span></span>
-   <span data-ttu-id="34767-309">**Si l’entrée attendue n’a pas de taille particulière, choisissez une largeur qui est cohérente avec les autres zones de texte ou contrôles de la fenêtre.**</span><span class="sxs-lookup"><span data-stu-id="34767-309">**If the expected input has no particular size, choose a width that is consistent with the other text boxes or controls on the window.**</span></span>
-   <span data-ttu-id="34767-310">**Dimensionnez les zones de texte sur plusieurs lignes pour afficher un nombre entier de lignes de texte.**</span><span class="sxs-lookup"><span data-stu-id="34767-310">**Size multi-line text boxes to display an integral number of lines of text.**</span></span>

## <a name="labels"></a><span data-ttu-id="34767-311">Étiquettes</span><span class="sxs-lookup"><span data-stu-id="34767-311">Labels</span></span>

### <a name="text-box-labels"></a><span data-ttu-id="34767-312">Étiquettes de zone de texte</span><span class="sxs-lookup"><span data-stu-id="34767-312">Text box labels</span></span>

-   <span data-ttu-id="34767-313">Toutes les zones de texte ont besoin d’étiquettes.</span><span class="sxs-lookup"><span data-stu-id="34767-313">All text boxes need labels.</span></span> <span data-ttu-id="34767-314">Écrivez l’étiquette en tant que mot ou expression, pas en tant que phrase, en terminant par un signe deux-points et en utilisant du [texte statique](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="34767-314">Write the label as a word or phrase, not as a sentence, ending with a colon, and using [static text](glossary.md).</span></span>

    <span data-ttu-id="34767-315">**Exceptions :**</span><span class="sxs-lookup"><span data-stu-id="34767-315">**Exceptions:**</span></span>

    -   <span data-ttu-id="34767-316">Zones de texte avec des invites à l’endroit où l’espace est au niveau Premium.</span><span class="sxs-lookup"><span data-stu-id="34767-316">Text boxes with prompts located where space is at a premium.</span></span>
    -   <span data-ttu-id="34767-317">Pour l’étiquetage, un groupe de zones de texte utilisé pour l' **entrée de données mises en forme** doit être traité comme une seule zone de texte.</span><span class="sxs-lookup"><span data-stu-id="34767-317">For labeling, a group of text boxes used for **formatted data input** should be treated as a single text box.</span></span>
    -   <span data-ttu-id="34767-318">Si une zone de texte est subordonnée à une case d’option ou à une case à cocher et qu’elle est introduite par son étiquette se terminant par un signe deux-points, ne placez pas d’étiquette supplémentaire sur la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="34767-318">If a text box is subordinate to a radio button or check box, and is introduced by its label ending with a colon, don't put an additional label on the text box.</span></span>
    -   <span data-ttu-id="34767-319">**Omettez les étiquettes de contrôle qui restatent l’instruction principale.**</span><span class="sxs-lookup"><span data-stu-id="34767-319">**Omit control labels that restate the main instruction.**</span></span> <span data-ttu-id="34767-320">Dans ce cas, l’instruction principale prend le signe deux-points (sauf s’il s’agit d’une question) et la clé d’accès.</span><span class="sxs-lookup"><span data-stu-id="34767-320">In this case, the main instruction takes the colon (unless it's a question) and access key.</span></span>

        <span data-ttu-id="34767-321">**Acceptable:**</span><span class="sxs-lookup"><span data-stu-id="34767-321">**Acceptable:**</span></span>

        ![capture d’écran de la zone de texte avec l’étiquette répétitive](images/ctrl-text-boxes-image26.png)

        <span data-ttu-id="34767-323">Dans cet exemple, l’étiquette de la zone de texte n’est qu’une REstate de l’instruction principale.</span><span class="sxs-lookup"><span data-stu-id="34767-323">In this example, the text box label is just a restatement of the main instruction.</span></span>

        <span data-ttu-id="34767-324">**Conseillé**</span><span class="sxs-lookup"><span data-stu-id="34767-324">**Better:**</span></span>

        ![<span data-ttu-id="34767-325">capture d’écran de la zone de texte avec l’instruction principale uniquement</span><span class="sxs-lookup"><span data-stu-id="34767-325">screen shot of text box with main instruction only</span></span> ](images/ctrl-text-boxes-image27.png)

        <span data-ttu-id="34767-326">Dans cet exemple, l’étiquette redondante est supprimée, de sorte que l’instruction principale prend le signe deux-points et la clé d’accès.</span><span class="sxs-lookup"><span data-stu-id="34767-326">In this example, the redundant label is removed, so the main instruction takes the colon and access key.</span></span>

-   <span data-ttu-id="34767-327">Attribuez une clé d’accès unique.</span><span class="sxs-lookup"><span data-stu-id="34767-327">Assign a unique access key.</span></span> <span data-ttu-id="34767-328">Pour connaître les instructions d’attribution de clé d’accès, consultez [clavier](inter-keyboard.md).</span><span class="sxs-lookup"><span data-stu-id="34767-328">For access key assignment guidelines, see [Keyboard](inter-keyboard.md).</span></span>
-   <span data-ttu-id="34767-329">Utilisez les majuscules comme pour les phrases.</span><span class="sxs-lookup"><span data-stu-id="34767-329">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="34767-330">Placez l’étiquette à gauche ou au-dessus de la zone de texte, puis alignez l’étiquette sur le bord gauche de la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="34767-330">Position the label either to the left of or above the text box, and align the label with the left edge of the text box.</span></span> <span data-ttu-id="34767-331">Si l’étiquette est située à gauche, aligne verticalement le texte de l’étiquette avec le texte de la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="34767-331">If the label is on the left, vertically align the label text with the text box text.</span></span>

    <span data-ttu-id="34767-332">**Correct :**</span><span class="sxs-lookup"><span data-stu-id="34767-332">**Correct:**</span></span>

    ![<span data-ttu-id="34767-333">capture d’écran de l’étiquette alignée à gauche au-dessus de la zone de texte</span><span class="sxs-lookup"><span data-stu-id="34767-333">screen shot of left-aligned label above text box</span></span> ](images/ctrl-text-boxes-image28.png)

    ![<span data-ttu-id="34767-334">capture d’écran de l’étiquette alignée sur le texte à gauche de la zone de texte</span><span class="sxs-lookup"><span data-stu-id="34767-334">screen shot of text-aligned label left of text box</span></span> ](images/ctrl-text-boxes-image29.png)

    <span data-ttu-id="34767-335">Dans ces exemples, l’étiquette en haut est alignée sur le bord gauche de la zone de texte, et l’étiquette à gauche s’aligne sur le texte de la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="34767-335">In these examples, the label on top aligns with the left edge of the text box, and the label on the left aligns with the text in the text box.</span></span>

    <span data-ttu-id="34767-336">**Incorrect :**</span><span class="sxs-lookup"><span data-stu-id="34767-336">**Incorrect:**</span></span>

    ![<span data-ttu-id="34767-337">capture d’écran de l’étiquette alignée sur le texte au-dessus de la zone de texte</span><span class="sxs-lookup"><span data-stu-id="34767-337">screen shot of text-aligned label above text box</span></span> ](images/ctrl-text-boxes-image30.png)

    ![<span data-ttu-id="34767-338">capture d’écran de l’étiquette alignée en haut à gauche de la zone de texte</span><span class="sxs-lookup"><span data-stu-id="34767-338">screen shot of top-aligned label left of text box</span></span> ](images/ctrl-text-boxes-image31.png)

    <span data-ttu-id="34767-339">Dans ces exemples incorrects, l’étiquette en haut est alignée sur le texte de la zone de texte, et l’étiquette à gauche s’aligne sur le haut de la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="34767-339">In these incorrect examples, the label on top aligns with the text in the text box, and the label on the left aligns with the top of the text box.</span></span>

-   <span data-ttu-id="34767-340">Vous pouvez spécifier des unités (par exemple, des secondes ou des connexions) entre parenthèses après l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="34767-340">You may specify units (for example, seconds or connections) in parentheses after the label.</span></span>
-   <span data-ttu-id="34767-341">Si une zone de texte accepte un nombre de caractères arbitrairement réduit, vous pouvez indiquer l’entrée maximale dans l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="34767-341">If a text box accepts an arbitrarily small maximum number of characters, you can state the maximum input in the label.</span></span> <span data-ttu-id="34767-342">La largeur de la zone de texte doit également suggérer la taille maximale.</span><span class="sxs-lookup"><span data-stu-id="34767-342">The text box width should also suggest the maximum size.</span></span>

    ![<span data-ttu-id="34767-343">capture d’écran de la zone de texte mot de passe</span><span class="sxs-lookup"><span data-stu-id="34767-343">screen shot of password text box</span></span> ](images/ctrl-text-boxes-image32.png)

    <span data-ttu-id="34767-344">Dans cet exemple, l’étiquette indique le nombre maximal de caractères.</span><span class="sxs-lookup"><span data-stu-id="34767-344">In this example, the label gives the maximum number of characters.</span></span>

-   <span data-ttu-id="34767-345">Ne faites pas du contenu de la zone de texte (ou de son étiquette d’unités) une partie d’une phrase, car cela n’est pas localisable.</span><span class="sxs-lookup"><span data-stu-id="34767-345">Don't make the content of the text box (or its units label) part of a sentence, because this is not localizable.</span></span>
-   <span data-ttu-id="34767-346">Si la zone de texte peut être utilisée pour entrer plusieurs éléments, indiquez clairement comment séparer les éléments dans l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="34767-346">If the text box can be used to enter several items, make it clear how to separate the items in the label.</span></span>

    ![<span data-ttu-id="34767-347">capture d’écran de noms séparés par un point-virgule</span><span class="sxs-lookup"><span data-stu-id="34767-347">screen shot of label separate names with semicolon</span></span> ](images/ctrl-text-boxes-image33.png)

    <span data-ttu-id="34767-348">Dans cet exemple, le séparateur d’éléments est indiqué dans l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="34767-348">In this example, the item separator is given in the label.</span></span>

-   <span data-ttu-id="34767-349">Pour obtenir des instructions sur l’indication des entrées requises, consultez entrée requise dans les [boîtes de dialogue](win-dialog-box.md).</span><span class="sxs-lookup"><span data-stu-id="34767-349">For guidelines on indicating required input, see Required input in [Dialog Boxes](win-dialog-box.md).</span></span>

### <a name="instruction-labels"></a><span data-ttu-id="34767-350">Étiquettes d’instruction</span><span class="sxs-lookup"><span data-stu-id="34767-350">Instruction labels</span></span>

-   <span data-ttu-id="34767-351">Si vous devez ajouter du texte d’instructions sur une zone de texte, ajoutez-la au-dessus de l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="34767-351">If you need to add instructional text about a text box, add it above the label.</span></span> <span data-ttu-id="34767-352">Utilisez des phrases complètes avec la ponctuation finale.</span><span class="sxs-lookup"><span data-stu-id="34767-352">Use complete sentences with ending punctuation.</span></span>
-   <span data-ttu-id="34767-353">Utilisez les majuscules comme pour les phrases.</span><span class="sxs-lookup"><span data-stu-id="34767-353">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="34767-354">Les informations supplémentaires qui sont utiles, mais pas nécessaires, doivent être courtes.</span><span class="sxs-lookup"><span data-stu-id="34767-354">Additional information that is helpful but not necessary should be kept short.</span></span> <span data-ttu-id="34767-355">Placez ces informations entre parenthèses entre l’étiquette et le signe deux-points, ou sans parenthèses sous la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="34767-355">Place this information either in parentheses between the label and colon, or without parentheses below the text box.</span></span>

    ![<span data-ttu-id="34767-356">capture d’écran des informations ajoutées en dessous de la zone de texte</span><span class="sxs-lookup"><span data-stu-id="34767-356">screen shot of added information below text box</span></span> ](images/ctrl-text-boxes-image34.png)

    <span data-ttu-id="34767-357">Dans cet exemple, des informations supplémentaires sont placées sous la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="34767-357">In this example, additional information is placed below the text box.</span></span>

### <a name="prompt-labels"></a><span data-ttu-id="34767-358">Étiquettes d’invite</span><span class="sxs-lookup"><span data-stu-id="34767-358">Prompt labels</span></span>

-   <span data-ttu-id="34767-359">Conservez le texte de l’invite concis.</span><span class="sxs-lookup"><span data-stu-id="34767-359">Keep the prompt text concise.</span></span> <span data-ttu-id="34767-360">Vous pouvez utiliser des fragments au lieu de phrases entières.</span><span class="sxs-lookup"><span data-stu-id="34767-360">You can use fragments instead of full sentences.</span></span>
-   <span data-ttu-id="34767-361">Utilisez les majuscules comme pour les phrases.</span><span class="sxs-lookup"><span data-stu-id="34767-361">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="34767-362">N’utilisez pas de ponctuation de fin ni de points de suspension.</span><span class="sxs-lookup"><span data-stu-id="34767-362">Don't use ending punctuation or ellipsis.</span></span>
-   <span data-ttu-id="34767-363">Si l’invite indique aux utilisateurs d’entrer des informations qui seront traitées par un bouton en regard de la zone de texte, placez simplement le bouton en regard de la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="34767-363">If the prompt directs users to enter information that will be acted upon by a button next to the text box, simply place the button next to the text box.</span></span> <span data-ttu-id="34767-364">N’utilisez pas l’invite pour demander aux utilisateurs de cliquer sur le bouton (par exemple, n’écrivez pas de texte d’invite indiquant, faites glisser un fichier, puis cliquez sur Envoyer).</span><span class="sxs-lookup"><span data-stu-id="34767-364">Don't use the prompt to direct users to click the button (for example, don't write prompt text that says, Drag a file and then click Send).</span></span>

## <a name="documentation"></a><span data-ttu-id="34767-365">Documentation</span><span class="sxs-lookup"><span data-stu-id="34767-365">Documentation</span></span>

<span data-ttu-id="34767-366">Lorsque vous faites référence à des zones de texte :</span><span class="sxs-lookup"><span data-stu-id="34767-366">When referring to text boxes:</span></span>

-   <span data-ttu-id="34767-367">Utilisez type pour faire référence aux interactions de l’utilisateur qui nécessitent une saisie ou un collage ; Sinon, utilisez la touche entrée si les utilisateurs peuvent placer des informations dans la zone de texte à l’aide d’autres moyens, par exemple en sélectionnant la valeur dans une liste ou en utilisant un bouton Parcourir.</span><span class="sxs-lookup"><span data-stu-id="34767-367">Use type to refer to user interactions that require typing or pasting; otherwise use enter if users can put information into the text box using other means, such as selecting the value from a list or using a Browse button.</span></span>
-   <span data-ttu-id="34767-368">Utilisez SELECT pour faire référence à une entrée dans une zone de texte en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="34767-368">Use select to refer to an entry in a read-only text box.</span></span>
-   <span data-ttu-id="34767-369">Utilisez le texte d’étiquette exact, y compris sa mise en majuscules, et incluez le mot zone.</span><span class="sxs-lookup"><span data-stu-id="34767-369">Use the exact label text, including its capitalization, and include the word box.</span></span> <span data-ttu-id="34767-370">N’incluez pas le trait de soulignement ou le signe deux-points.</span><span class="sxs-lookup"><span data-stu-id="34767-370">Don't include the access key underscore or colon.</span></span> <span data-ttu-id="34767-371">Ne faites pas référence à une zone de texte sous la forme d’une zone de texte ou d’un champ.</span><span class="sxs-lookup"><span data-stu-id="34767-371">Don't refer to a text box as a text box or a field.</span></span>
-   <span data-ttu-id="34767-372">Dans la mesure du possible, mettez en forme l’étiquette à l’aide de texte en gras.</span><span class="sxs-lookup"><span data-stu-id="34767-372">When possible, format the label using bold text.</span></span> <span data-ttu-id="34767-373">Sinon, placez l’étiquette entre guillemets uniquement si nécessaire pour éviter toute confusion.</span><span class="sxs-lookup"><span data-stu-id="34767-373">Otherwise, put the label in quotation marks only if required to prevent confusion.</span></span>

    <span data-ttu-id="34767-374">Exemple : tapez votre mot de passe dans la zone **mot de passe** , puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="34767-374">Example: Type your password into the **Password** box, and then click **OK**.</span></span>

-   <span data-ttu-id="34767-375">Si la zone de texte requiert un format spécifique, documentez uniquement le format acceptable le plus couramment utilisé.</span><span class="sxs-lookup"><span data-stu-id="34767-375">If the text box requires a specific format, document only the most commonly used acceptable format.</span></span> <span data-ttu-id="34767-376">Permet aux utilisateurs de découvrir eux-mêmes d’autres formats.</span><span class="sxs-lookup"><span data-stu-id="34767-376">Let users discover any other formats on their own.</span></span> <span data-ttu-id="34767-377">Vous souhaitez être flexible avec les formats de données, mais cela ne devrait pas aboutir à une documentation complexe.</span><span class="sxs-lookup"><span data-stu-id="34767-377">You want to be flexible with data formats, but doing so should not result in complex documentation.</span></span>

    <span data-ttu-id="34767-378">**Correct :**</span><span class="sxs-lookup"><span data-stu-id="34767-378">**Correct:**</span></span>

    <span data-ttu-id="34767-379">Entrez le numéro de série du composant en utilisant le format 1234-56-7890.</span><span class="sxs-lookup"><span data-stu-id="34767-379">Enter the part's serial number using the 1234-56-7890 format.</span></span>

    <span data-ttu-id="34767-380">**Incorrect :**</span><span class="sxs-lookup"><span data-stu-id="34767-380">**Incorrect:**</span></span>

    <span data-ttu-id="34767-381">Entrez le numéro de série du composant en utilisant l’un des formats suivants :</span><span class="sxs-lookup"><span data-stu-id="34767-381">Enter the part's serial number using any of the following formats:</span></span>

    <span data-ttu-id="34767-382">1234567890</span><span class="sxs-lookup"><span data-stu-id="34767-382">1234567890</span></span>

    <span data-ttu-id="34767-383">1234-56-7890</span><span class="sxs-lookup"><span data-stu-id="34767-383">1234-56-7890</span></span>

    <span data-ttu-id="34767-384">1234 56 7890</span><span class="sxs-lookup"><span data-stu-id="34767-384">1234 56 7890</span></span>

