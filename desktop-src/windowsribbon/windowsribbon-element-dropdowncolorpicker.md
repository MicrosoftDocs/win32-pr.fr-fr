---
title: Élément DropDownColorPicker
description: Représente une Drop-Down couleur Pickercontrol qui, lorsque l’utilisateur clique dessus, affiche une palette d’échantillons de couleurs.
ms.assetid: fc4df978-9c52-43d5-8a5e-e015aa7058cd
keywords:
- Ruban des fenêtres d’élément DropDownColorPicker
topic_type:
- apiref
api_name:
- DropDownColorPicker
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce2fd1d9ff12b56d87955304fad24af23209ff91
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442900"
---
# <a name="dropdowncolorpicker-element"></a><span data-ttu-id="d03b1-104">Élément DropDownColorPicker</span><span class="sxs-lookup"><span data-stu-id="d03b1-104">DropDownColorPicker element</span></span>

<span data-ttu-id="d03b1-105">Représente un contrôle de [Sélecteur de couleurs déroulant](windowsribbon-controls-dropdowncolorpicker.md)qui, lorsque l’utilisateur clique dessus, affiche une palette d’échantillons de couleurs.</span><span class="sxs-lookup"><span data-stu-id="d03b1-105">Represents a [Drop-Down Color Picker](windowsribbon-controls-dropdowncolorpicker.md)control that when clicked displays a palette of color swatches.</span></span>

## <a name="usage"></a><span data-ttu-id="d03b1-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="d03b1-106">Usage</span></span>

``` syntax
<DropDownColorPicker
  CommandName = "xs:positiveInteger or xs:string"
  Columns = "xs:positiveInteger"
  ThemeColorGridRows = "xs:positiveInteger"
  StandardColorGridRows = "xs:positiveInteger"
  RecentColorGridRows = "xs:positiveInteger"
  IsAutomaticColorButtonVisible = "Boolean"
  IsNoColorButtonVisible = "Boolean"
  ColorTemplate = "xs:string"
  ChipSize = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="d03b1-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="d03b1-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d03b1-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="d03b1-108">Attribute</span></span></th>
<th><span data-ttu-id="d03b1-109">Type</span><span class="sxs-lookup"><span data-stu-id="d03b1-109">Type</span></span></th>
<th><span data-ttu-id="d03b1-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d03b1-110">Required</span></span></th>
<th><span data-ttu-id="d03b1-111">Description</span><span class="sxs-lookup"><span data-stu-id="d03b1-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d03b1-112"><strong>Copeaux</strong></span><span class="sxs-lookup"><span data-stu-id="d03b1-112"><strong>ChipSize</strong></span></span><br/></td>
<td><span data-ttu-id="d03b1-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="d03b1-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="d03b1-114">Non</span><span class="sxs-lookup"><span data-stu-id="d03b1-114">No</span></span><br/></td>
<td><span data-ttu-id="d03b1-115">Taille de chaque puce ou nuance de couleur.</span><span class="sxs-lookup"><span data-stu-id="d03b1-115">The size of each color chip or swatch.</span></span> <br/> <span data-ttu-id="d03b1-116">Limité à l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="d03b1-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="d03b1-117">
<dt><span></span><span></span><strong></strong> Small</span><span class="sxs-lookup"><span data-stu-id="d03b1-117">
<dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="d03b1-118">Chaque puce de couleur est un carré de pixel 11x11.</span><span class="sxs-lookup"><span data-stu-id="d03b1-118">Each color chip is an 11x11 pixel square.</span></span> <br/> </dd> <span data-ttu-id="d03b1-119"><dt><span></span><span></span><strong></strong> Médias</span><span class="sxs-lookup"><span data-stu-id="d03b1-119"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd> <span data-ttu-id="d03b1-120">Chaque puce de couleur est un carré de 16 x 16 pixels.</span><span class="sxs-lookup"><span data-stu-id="d03b1-120">Each color chip is a 16x16 pixel square.</span></span> <br/> </dd> <span data-ttu-id="d03b1-121"><dt><span></span><span></span><strong></strong> Conséquent</span><span class="sxs-lookup"><span data-stu-id="d03b1-121"><dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd> <span data-ttu-id="d03b1-122">Chaque puce de couleur est un carré de pixel 24x24.</span><span class="sxs-lookup"><span data-stu-id="d03b1-122">Each color chip is a 24x24 pixel square.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d03b1-123"><strong>ColorTemplate</strong></span><span class="sxs-lookup"><span data-stu-id="d03b1-123"><strong>ColorTemplate</strong></span></span><br/></td>
<td><span data-ttu-id="d03b1-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="d03b1-124">xs:string</span></span><br/></td>
<td><span data-ttu-id="d03b1-125">Non</span><span class="sxs-lookup"><span data-stu-id="d03b1-125">No</span></span><br/></td>
<td><span data-ttu-id="d03b1-126">Modèles de disposition qui spécifient le type de <a href="windowsribbon-controls-dropdowncolorpicker.md">Sélecteur de couleur déroulant</a>.</span><span class="sxs-lookup"><span data-stu-id="d03b1-126">Layout templates that specify the type of <a href="windowsribbon-controls-dropdowncolorpicker.md">Drop-Down Color Picker</a>.</span></span> <br/> <span data-ttu-id="d03b1-127">Limité à l’une des valeurs suivantes (si aucun attribut facultatif relatif à un <em>ColorTemplate</em> n’est déclaré, la vue par défaut est indiquée) :</span><span class="sxs-lookup"><span data-stu-id="d03b1-127">Restricted to one of the following values (if no optional attributes related to a <em>ColorTemplate</em> are declared, the default view is shown):</span></span><br/> <br/><span data-ttu-id="d03b1-128">
<dt><span></span><span></span><strong></strong> (ThemeColors)</span><span class="sxs-lookup"><span data-stu-id="d03b1-128">
<dt><span></span><span></span><strong></strong> (ThemeColors)</span></span><br/> </dt> <dd> <span data-ttu-id="d03b1-129">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="d03b1-129">Default.</span></span> <br/> <img src="images/markup/colortemplate.themedcolors.1.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;ThemeColors&#39;." /><br/> <span data-ttu-id="d03b1-130">La définition de l’attribut <em>ColorTemplate</em> pour <code>ThemeColors</code> active les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="d03b1-130">Setting the <em>ColorTemplate</em> attribute to <code>ThemeColors</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="d03b1-131">Ancre SplitButton.</span><span class="sxs-lookup"><span data-stu-id="d03b1-131">SplitButton anchor.</span></span></li>
<li><span data-ttu-id="d03b1-132">Le bouton couleur <strong>automatique</strong> est affiché par défaut.</span><span class="sxs-lookup"><span data-stu-id="d03b1-132"><strong>Automatic</strong> color button is displayed by default.</span></span></li>
<li><span data-ttu-id="d03b1-133">Palette de <strong>couleurs du thème</strong> Windows.</span><span class="sxs-lookup"><span data-stu-id="d03b1-133">Windows <strong>Theme colors</strong> swatch grid.</span></span></li>
<li><span data-ttu-id="d03b1-134">Grille d’échantillons de <strong>couleurs standard</strong> .</span><span class="sxs-lookup"><span data-stu-id="d03b1-134"><strong>Standard colors</strong> swatch grid.</span></span></li>
<li><span data-ttu-id="d03b1-135">La grille des échantillons de <strong>couleurs récentes</strong> est facultative.</span><span class="sxs-lookup"><span data-stu-id="d03b1-135"><strong>Recent Colors</strong> swatch grid is optional.</span></span></li>
<li><span data-ttu-id="d03b1-136">Lanceur de boîte de dialogue <strong>couleurs supplémentaires</strong> .</span><span class="sxs-lookup"><span data-stu-id="d03b1-136"><strong>More colors</strong> dialog box launcher.</span></span></li>
<li><span data-ttu-id="d03b1-137"><strong>Aucun</strong> bouton de couleur de couleur n’est affiché par défaut.</span><span class="sxs-lookup"><span data-stu-id="d03b1-137"><strong>No color</strong> color button is displayed by default.</span></span></li>
</ul>
</dd> <span data-ttu-id="d03b1-138"><dt><span></span><span></span><strong></strong> (StandardColors)</span><span class="sxs-lookup"><span data-stu-id="d03b1-138"><dt><span></span><span></span><strong></strong> (StandardColors)</span></span><br/> </dt> <dd> <img src="images/markup/colortemplate.standardcolors.3.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;StandardColors&#39;." /><br/> <span data-ttu-id="d03b1-139">La définition de l’attribut <em>ColorTemplate</em> pour <code>StandardColors</code> active les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="d03b1-139">Setting the <em>ColorTemplate</em> attribute to <code>StandardColors</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="d03b1-140">Ancre SplitButton.</span><span class="sxs-lookup"><span data-stu-id="d03b1-140">SplitButton anchor.</span></span></li>
<li><span data-ttu-id="d03b1-141">Le bouton couleur <strong>automatique</strong> est affiché par défaut.</span><span class="sxs-lookup"><span data-stu-id="d03b1-141"><strong>Automatic</strong> color button is displayed by default.</span></span></li>
<li><span data-ttu-id="d03b1-142">Grille d’échantillons de <strong>couleurs standard</strong> .</span><span class="sxs-lookup"><span data-stu-id="d03b1-142"><strong>Standard colors</strong> swatch grid.</span></span></li>
<li><span data-ttu-id="d03b1-143">Lanceur de boîte de dialogue <strong>couleurs supplémentaires</strong> .</span><span class="sxs-lookup"><span data-stu-id="d03b1-143"><strong>More colors</strong> dialog box launcher.</span></span></li>
<li><span data-ttu-id="d03b1-144"><strong>Aucun</strong> bouton de couleur de couleur n’est affiché par défaut.</span><span class="sxs-lookup"><span data-stu-id="d03b1-144"><strong>No color</strong> color button is displayed by default.</span></span></li>
</ul>
</dd> <span data-ttu-id="d03b1-145"><dt><span></span><span></span><strong></strong> (HighlightColors)</span><span class="sxs-lookup"><span data-stu-id="d03b1-145"><dt><span></span><span></span><strong></strong> (HighlightColors)</span></span><br/> </dt> <dd> <img src="images/markup/colortemplate.highlightcolors.2.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;HighlightColors&#39;." /><br/> <span data-ttu-id="d03b1-146">La définition de l’attribut <em>ColorTemplate</em> pour <code>HighlightColors</code> active les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="d03b1-146">Setting the <em>ColorTemplate</em> attribute to <code>HighlightColors</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="d03b1-147">Ancre SplitButton.</span><span class="sxs-lookup"><span data-stu-id="d03b1-147">SplitButton anchor.</span></span></li>
<li><span data-ttu-id="d03b1-148">Grille d’échantillons de <strong>couleurs standard</strong> sans en-tête.</span><span class="sxs-lookup"><span data-stu-id="d03b1-148"><strong>Standard colors</strong> swatch grid with no header.</span></span></li>
<li><span data-ttu-id="d03b1-149"><strong>Aucun</strong> bouton de couleur de couleur n’est affiché par défaut.</span><span class="sxs-lookup"><span data-stu-id="d03b1-149"><strong>No color</strong> color button is displayed by default.</span></span></li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d03b1-150"><strong>Colonnes</strong></span><span class="sxs-lookup"><span data-stu-id="d03b1-150"><strong>Columns</strong></span></span><br/></td>
<td><span data-ttu-id="d03b1-151">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="d03b1-151">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="d03b1-152">Non</span><span class="sxs-lookup"><span data-stu-id="d03b1-152">No</span></span><br/></td>
<td><span data-ttu-id="d03b1-153">Nombre de colonnes de la puce de couleur (ou de l’échantillon).</span><span class="sxs-lookup"><span data-stu-id="d03b1-153">The number of color chip (or swatch) columns.</span></span><br/> <br/><span data-ttu-id="d03b1-154">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="d03b1-154">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="d03b1-155">Toute valeur entière positive comprise entre 1 et 256 inclus.</span><span class="sxs-lookup"><span data-stu-id="d03b1-155">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d03b1-156"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="d03b1-156"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="d03b1-157">XS : positiveInteger ou XS : String</span><span class="sxs-lookup"><span data-stu-id="d03b1-157">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="d03b1-158">Non</span><span class="sxs-lookup"><span data-stu-id="d03b1-158">No</span></span><br/></td>
<td><span data-ttu-id="d03b1-159">Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d03b1-159">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="d03b1-160">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)</span><span class="sxs-lookup"><span data-stu-id="d03b1-160">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="d03b1-161">Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus.</span><span class="sxs-lookup"><span data-stu-id="d03b1-161">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="d03b1-162">La valeur doit être unique dans le document XML du ruban.</span><span class="sxs-lookup"><span data-stu-id="d03b1-162">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="d03b1-163">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="d03b1-163">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d03b1-164"><strong>IsAutomaticColorButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="d03b1-164"><strong>IsAutomaticColorButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="d03b1-165">Boolean</span><span class="sxs-lookup"><span data-stu-id="d03b1-165">Boolean</span></span><br/></td>
<td><span data-ttu-id="d03b1-166">Non</span><span class="sxs-lookup"><span data-stu-id="d03b1-166">No</span></span><br/></td>
<td><span data-ttu-id="d03b1-167">Affiche (ou masque) le bouton de couleur <strong>automatique</strong> .</span><span class="sxs-lookup"><span data-stu-id="d03b1-167">Displays (or hides) the <strong>Automatic</strong> color button.</span></span> <br/> <span data-ttu-id="d03b1-168">Valide uniquement lorsque <code>StandardColors</code> ou <code>ThemeColors</code> est spécifié pour l’attribut <em>ColorTemplate</em> .</span><span class="sxs-lookup"><span data-stu-id="d03b1-168">Valid only when <code>StandardColors</code> or <code>ThemeColors</code> is specified for the <em>ColorTemplate</em> attribute.</span></span> <br/> <span data-ttu-id="d03b1-169">Limité à l’une des valeurs suivantes (0 et 1 ne sont pas valides) :</span><span class="sxs-lookup"><span data-stu-id="d03b1-169">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="d03b1-170">
<dt><span></span><span></span><strong></strong> :</span><span class="sxs-lookup"><span data-stu-id="d03b1-170">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="d03b1-171"><dt><span></span><span></span><strong></strong> fausses</span><span class="sxs-lookup"><span data-stu-id="d03b1-171"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d03b1-172"><strong>IsNoColorButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="d03b1-172"><strong>IsNoColorButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="d03b1-173">Boolean</span><span class="sxs-lookup"><span data-stu-id="d03b1-173">Boolean</span></span><br/></td>
<td><span data-ttu-id="d03b1-174">Non</span><span class="sxs-lookup"><span data-stu-id="d03b1-174">No</span></span><br/></td>
<td><span data-ttu-id="d03b1-175">Affiche (ou masque) le bouton <strong>aucune couleur</strong> .</span><span class="sxs-lookup"><span data-stu-id="d03b1-175">Displays (or hides) the <strong>No color</strong> button.</span></span> <br/> <span data-ttu-id="d03b1-176">Valide pour toutes les valeurs <em>ColorTemplate</em> .</span><span class="sxs-lookup"><span data-stu-id="d03b1-176">Valid for all <em>ColorTemplate</em> values.</span></span><br/> <span data-ttu-id="d03b1-177">Limité à l’une des valeurs suivantes (0 et 1 ne sont pas valides) :</span><span class="sxs-lookup"><span data-stu-id="d03b1-177">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="d03b1-178">
<dt><span></span><span></span><strong></strong> :</span><span class="sxs-lookup"><span data-stu-id="d03b1-178">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="d03b1-179"><dt><span></span><span></span><strong></strong> fausses</span><span class="sxs-lookup"><span data-stu-id="d03b1-179"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d03b1-180"><strong>RecentColorGridRows</strong></span><span class="sxs-lookup"><span data-stu-id="d03b1-180"><strong>RecentColorGridRows</strong></span></span><br/></td>
<td><span data-ttu-id="d03b1-181">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="d03b1-181">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="d03b1-182">Non</span><span class="sxs-lookup"><span data-stu-id="d03b1-182">No</span></span><br/></td>
<td><span data-ttu-id="d03b1-183">Nombre de lignes de la puce de couleur (ou de l’échantillon) dans la zone <strong>couleurs récentes</strong> .</span><span class="sxs-lookup"><span data-stu-id="d03b1-183">The number of color chip (or swatch) rows in the <strong>Recent colors</strong> area.</span></span> <br/> <span data-ttu-id="d03b1-184">Valide uniquement lorsque <code>ThemeColors</code> est spécifié pour l’attribut <em>ColorTemplate</em> .</span><span class="sxs-lookup"><span data-stu-id="d03b1-184">Valid only when <code>ThemeColors</code> is specified for the <em>ColorTemplate</em> attribute.</span></span><br/> <br/><span data-ttu-id="d03b1-185">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="d03b1-185">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="d03b1-186">Toute valeur entière positive comprise entre 1 et 256 inclus.</span><span class="sxs-lookup"><span data-stu-id="d03b1-186">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d03b1-187"><strong>StandardColorGridRows</strong></span><span class="sxs-lookup"><span data-stu-id="d03b1-187"><strong>StandardColorGridRows</strong></span></span><br/></td>
<td><span data-ttu-id="d03b1-188">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="d03b1-188">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="d03b1-189">Non</span><span class="sxs-lookup"><span data-stu-id="d03b1-189">No</span></span><br/></td>
<td><span data-ttu-id="d03b1-190">Nombre de lignes de puce de couleur (ou d’échantillon) dans la zone de <strong>couleurs standard</strong> .</span><span class="sxs-lookup"><span data-stu-id="d03b1-190">The number of color chip (or swatch) rows in the <strong>Standard colors</strong> area.</span></span><br/> <br/><span data-ttu-id="d03b1-191">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="d03b1-191">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="d03b1-192">Toute valeur entière positive comprise entre 1 et 256 inclus.</span><span class="sxs-lookup"><span data-stu-id="d03b1-192">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d03b1-193"><strong>ThemeColorGridRows</strong></span><span class="sxs-lookup"><span data-stu-id="d03b1-193"><strong>ThemeColorGridRows</strong></span></span><br/></td>
<td><span data-ttu-id="d03b1-194">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="d03b1-194">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="d03b1-195">Non</span><span class="sxs-lookup"><span data-stu-id="d03b1-195">No</span></span><br/></td>
<td><span data-ttu-id="d03b1-196">Nombre de lignes de puce de couleur (ou d’échantillon) dans la zone de <strong>couleurs de thème</strong> .</span><span class="sxs-lookup"><span data-stu-id="d03b1-196">The number of color chip (or swatch) rows in the <strong>Theme colors</strong> area.</span></span><br/> <span data-ttu-id="d03b1-197">Valide uniquement lorsque <code>ThemeColors</code> est spécifié pour l’attribut <em>ColorTemplate</em> .</span><span class="sxs-lookup"><span data-stu-id="d03b1-197">Valid only when <code>ThemeColors</code> is specified for the <em>ColorTemplate</em> attribute.</span></span><br/> <br/><span data-ttu-id="d03b1-198">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="d03b1-198">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="d03b1-199">Toute valeur entière positive comprise entre 1 et 256 inclus.</span><span class="sxs-lookup"><span data-stu-id="d03b1-199">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="d03b1-200">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d03b1-200">Child elements</span></span>

<span data-ttu-id="d03b1-201">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="d03b1-201">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="d03b1-202">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d03b1-202">Parent elements</span></span>



| <span data-ttu-id="d03b1-203">Élément</span><span class="sxs-lookup"><span data-stu-id="d03b1-203">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="d03b1-204">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="d03b1-204">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| [<span data-ttu-id="d03b1-205">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="d03b1-205">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>         |
| [<span data-ttu-id="d03b1-206">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="d03b1-206">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="d03b1-207">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="d03b1-207">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="d03b1-208">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="d03b1-208">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| [<span data-ttu-id="d03b1-209">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="d03b1-209">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>               |
| [<span data-ttu-id="d03b1-210">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="d03b1-210">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="d03b1-211">Remarques</span><span class="sxs-lookup"><span data-stu-id="d03b1-211">Remarks</span></span>

<span data-ttu-id="d03b1-212">facultatif.</span><span class="sxs-lookup"><span data-stu-id="d03b1-212">Optional.</span></span>

<span data-ttu-id="d03b1-213">Peut se produire une ou plusieurs fois pour chaque élément [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md)ou [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="d03b1-213">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="d03b1-214">Exemples</span><span class="sxs-lookup"><span data-stu-id="d03b1-214">Examples</span></span>

<span data-ttu-id="d03b1-215">L’exemple suivant illustre le balisage de base pour les trois types de [sélecteurs de couleurs déroulants](windowsribbon-controls-dropdowncolorpicker.md).</span><span class="sxs-lookup"><span data-stu-id="d03b1-215">The following example demonstrates the basic markup for all three types of [Drop-Down Color Picker](windowsribbon-controls-dropdowncolorpicker.md).</span></span>

<span data-ttu-id="d03b1-216">Cette section de code montre les déclarations de commande pour trois éléments **DropDownColorPicker** .</span><span class="sxs-lookup"><span data-stu-id="d03b1-216">This section of code shows the Command declarations for three **DropDownColorPicker** elements.</span></span>


```XML
<!-- DropDownColorPickers -->
<Command Name="cmdDropDownColorPickerGroup"
         Symbol="cmdDropDownColorPickerGroup"
         Comment="DropDownColorPicker Group"
         Id="55000"/>
<Command Name="cmdDropDownColorPickerThemeColors"
         Symbol="cmdDropDownColorPickerThemeColors"
         Comment="DropDownColorPicker ThemeColors"
         Id="55010"
         LabelTitle="ThemeColors"
         LabelDescription="ThemeColors\ndescription."/>
<Command Name="cmdDropDownColorPickerStandardColors"
         Symbol="cmdDropDownColorPickerStandardColors"
         Comment="DropDownColorPicker StandardColors"
         Id="55011"
         LabelTitle="StandardColors"/>
<Command Name="cmdDropDownColorPickerHighlightColors"
         Symbol="cmdDropDownColorPickerHighlightColors"
         Comment="DropDownColorPicker HighlightColors"
         Id="55012"
         LabelTitle="HighlightColors"/>
```



<span data-ttu-id="d03b1-217">Cette section de code illustre les trois types de déclarations de contrôle **DropDownColorPicker** .</span><span class="sxs-lookup"><span data-stu-id="d03b1-217">This section of code shows the three types of **DropDownColorPicker** control declarations.</span></span>


```XML
<Group CommandName="cmdDropDownColorPickerGroup"
       SizeDefinition="ThreeButtons">
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerThemeColors"
    ColorTemplate="ThemeColors"/>
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerStandardColors"
    ColorTemplate="StandardColors"/>
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerHighlightColors"
    ColorTemplate="HighlightColors"
    StandardColorGridRows="1"/>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="d03b1-218">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="d03b1-218">Element information</span></span>

* <span data-ttu-id="d03b1-219">**Système minimal pris en charge**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="d03b1-219">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="d03b1-220">**Peut être vide**: Oui</span><span class="sxs-lookup"><span data-stu-id="d03b1-220">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="d03b1-221">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d03b1-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d03b1-222">Contrôle de sélecteur de couleurs déroulant</span><span class="sxs-lookup"><span data-stu-id="d03b1-222">Drop-Down Color Picker control</span></span>](windowsribbon-controls-dropdowncolorpicker.md)
</dt> <dt>

[<span data-ttu-id="d03b1-223">Exemple DropDownColorPicker</span><span class="sxs-lookup"><span data-stu-id="d03b1-223">DropDownColorPicker Sample</span></span>](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

 

 





