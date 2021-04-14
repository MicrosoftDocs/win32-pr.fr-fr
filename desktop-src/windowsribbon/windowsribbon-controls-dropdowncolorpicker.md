---
title: Sélecteur de couleurs Drop-Down
description: L’infrastructure de ruban Windows fournit un contrôle de sélecteur de couleurs Drop-Down spécialisé qui expose un large éventail de paramètres de couleur via un bouton partagé et un sélecteur de couleur déroulant personnalisable.
ms.assetid: 65e1fc23-7ac0-4bb3-9359-28ce88acf356
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 552cd05e619ba71653d0d72e8457f5d4c8c39624
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104383064"
---
# <a name="drop-down-color-picker"></a><span data-ttu-id="20bbe-103">Sélecteur de couleurs Drop-Down</span><span class="sxs-lookup"><span data-stu-id="20bbe-103">Drop-Down Color Picker</span></span>

<span data-ttu-id="20bbe-104">L’infrastructure de ruban Windows fournit un contrôle de sélecteur de couleurs Drop-Down spécialisé qui expose un large éventail de paramètres de couleur via un bouton partagé et un sélecteur de couleur déroulant personnalisable.</span><span class="sxs-lookup"><span data-stu-id="20bbe-104">The Windows Ribbon framework provides a specialized Drop-Down Color Picker control that exposes a variety of color settings through a split button and customizable drop-down color selector.</span></span>

-   [<span data-ttu-id="20bbe-105">Introduction</span><span class="sxs-lookup"><span data-stu-id="20bbe-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="20bbe-106">balisage</span><span class="sxs-lookup"><span data-stu-id="20bbe-106">Markup</span></span>](#markup)
-   [<span data-ttu-id="20bbe-107">Code</span><span class="sxs-lookup"><span data-stu-id="20bbe-107">Code</span></span>](#code)
    -   [<span data-ttu-id="20bbe-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="20bbe-108">Properties</span></span>](#properties)
    -   [<span data-ttu-id="20bbe-109">Gestionnaires de commandes</span><span class="sxs-lookup"><span data-stu-id="20bbe-109">Command handlers</span></span>](#command-handlers)
-   [<span data-ttu-id="20bbe-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="20bbe-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="20bbe-111">Introduction</span><span class="sxs-lookup"><span data-stu-id="20bbe-111">Introduction</span></span>

<span data-ttu-id="20bbe-112">En émulant l’apparence et la fonctionnalité du sélecteur de couleurs Microsoft Office, l’infrastructure du ruban peut à la fois tirer parti de et contribuer à la cohérence et à la familiarité dans un large éventail d’applications.</span><span class="sxs-lookup"><span data-stu-id="20bbe-112">By emulating the appearance and functionality of the Microsoft Office color picker, the Ribbon framework is able to both benefit from, and contribute to, consistency and familiarity across a wide range of applications.</span></span>

## <a name="markup"></a><span data-ttu-id="20bbe-113">balisage</span><span class="sxs-lookup"><span data-stu-id="20bbe-113">Markup</span></span>

<span data-ttu-id="20bbe-114">Comme tous les contrôles de ruban, le sélecteur de couleurs Drop-Down est facilement implémenté et personnalisé par le biais du balisage.</span><span class="sxs-lookup"><span data-stu-id="20bbe-114">Like all Ribbon controls, the Drop-Down Color Picker is easily implemented and customized through markup.</span></span> <span data-ttu-id="20bbe-115">L’infrastructure fournit un certain nombre d’attributs d’élément pour le sélecteur de couleurs Drop-Down pour exposer différents niveaux de fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="20bbe-115">The framework provides a number of element attributes for the Drop-Down Color Picker to expose various levels of functionality.</span></span> <span data-ttu-id="20bbe-116">Le tableau suivant répertorie les attributs du sélecteur de couleurs Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="20bbe-116">The following table lists the Drop-Down Color Picker attributes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20bbe-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="20bbe-117">Attribute</span></span></th>
<th><span data-ttu-id="20bbe-118">Description</span><span class="sxs-lookup"><span data-stu-id="20bbe-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="20bbe-119">ColorTemplate</span><span class="sxs-lookup"><span data-stu-id="20bbe-119">ColorTemplate</span></span></td>
<td><span data-ttu-id="20bbe-120">Modèles de disposition qui spécifient le type de Drop-Down sélecteur de couleurs.</span><span class="sxs-lookup"><span data-stu-id="20bbe-120">Layout templates that specify the type of Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="20bbe-121">Il existe trois modèles, chacun spécifiant une disposition de contrôle et des valeurs par défaut pour les attributs et les clés de propriété associés.</span><span class="sxs-lookup"><span data-stu-id="20bbe-121">There are three templates, each of which specifies a control layout and default values for associated attributes and property keys.</span></span> <br/>
<ul>
<li><code>ThemeColors</code></li>
<li><code>StandardColors</code></li>
<li><code>HighlightColors</code></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20bbe-122">Copeaux</span><span class="sxs-lookup"><span data-stu-id="20bbe-122">ChipSize</span></span></td>
<td><span data-ttu-id="20bbe-123">Taille de chaque puce de couleur (ou nuance).</span><span class="sxs-lookup"><span data-stu-id="20bbe-123">The size of each color chip (or swatch).</span></span><br/>
<ul>
<li><code>Small</code></li>
<li><code>Medium</code></li>
<li><code>Large</code></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20bbe-124">Colonnes</span><span class="sxs-lookup"><span data-stu-id="20bbe-124">Columns</span></span></td>
<td><span data-ttu-id="20bbe-125">Nombre de colonnes de la puce de couleur (ou de l’échantillon).</span><span class="sxs-lookup"><span data-stu-id="20bbe-125">The number of color chip (or swatch) columns.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20bbe-126">CommandName</span><span class="sxs-lookup"><span data-stu-id="20bbe-126">CommandName</span></span></td>
<td><span data-ttu-id="20bbe-127">Nom de la déclaration de commande associée.</span><span class="sxs-lookup"><span data-stu-id="20bbe-127">The name of the associated Command declaration.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20bbe-128">IsAutomaticColorButtonVisible</span><span class="sxs-lookup"><span data-stu-id="20bbe-128">IsAutomaticColorButtonVisible</span></span></td>
<td><span data-ttu-id="20bbe-129">Affiche (ou masque) le bouton <strong>automatique</strong> .</span><span class="sxs-lookup"><span data-stu-id="20bbe-129">Displays (or hides) the <strong>Automatic</strong> button.</span></span><br/> <span data-ttu-id="20bbe-130">Valide uniquement lorsque <em>ColorTemplate</em> a la valeur <code>ThemeColors</code> ou <code>StandardColors</code> .</span><span class="sxs-lookup"><span data-stu-id="20bbe-130">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20bbe-131">IsNoColorButtonVisible</span><span class="sxs-lookup"><span data-stu-id="20bbe-131">IsNoColorButtonVisible</span></span></td>
<td><span data-ttu-id="20bbe-132">Affiche (ou masque) le bouton <strong>aucune couleur</strong> .</span><span class="sxs-lookup"><span data-stu-id="20bbe-132">Displays (or hides) the <strong>No color</strong> button.</span></span><br/> <span data-ttu-id="20bbe-133">Valide pour toutes les valeurs <em>ColorTemplate</em> .</span><span class="sxs-lookup"><span data-stu-id="20bbe-133">Valid for all <em>ColorTemplate</em> values.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20bbe-134">RecentColorGridRows</span><span class="sxs-lookup"><span data-stu-id="20bbe-134">RecentColorGridRows</span></span></td>
<td><span data-ttu-id="20bbe-135">Nombre de lignes de la puce de couleur (ou de l’échantillon) dans la zone <strong>couleurs récentes</strong> .</span><span class="sxs-lookup"><span data-stu-id="20bbe-135">The number of color chip (or swatch) rows in the <strong>Recent colors</strong> area.</span></span><br/> <span data-ttu-id="20bbe-136">Valide uniquement lorsque <em>ColorTemplate</em> a la valeur <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="20bbe-136">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20bbe-137">StandardColorGridRows</span><span class="sxs-lookup"><span data-stu-id="20bbe-137">StandardColorGridRows</span></span></td>
<td><span data-ttu-id="20bbe-138">Nombre de lignes de puce de couleur (ou d’échantillon) dans la zone de <strong>couleurs standard</strong> .</span><span class="sxs-lookup"><span data-stu-id="20bbe-138">The number of color chip (or swatch) rows in the <strong>Standard colors</strong> area.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20bbe-139">ThemeColorGridRows</span><span class="sxs-lookup"><span data-stu-id="20bbe-139">ThemeColorGridRows</span></span></td>
<td><span data-ttu-id="20bbe-140">Nombre de lignes de puce de couleur (ou d’échantillon) dans la zone de <strong>couleurs de thème</strong> .</span><span class="sxs-lookup"><span data-stu-id="20bbe-140">The number of color chip (or swatch) rows in the <strong>Theme colors</strong> area.</span></span><br/> <span data-ttu-id="20bbe-141">Valide uniquement lorsque <em>ColorTemplate</em> a la valeur <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="20bbe-141">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="20bbe-142">Les captures d’écran suivantes illustrent les dispositions par défaut du sélecteur de couleurs Drop-Down pour les trois modèles de couleurs.</span><span class="sxs-lookup"><span data-stu-id="20bbe-142">The following screen shots illustrate the default Drop-Down Color Picker layouts for the three color templates.</span></span>



|                                                                                                                                                                                               |                                                                                                                                                                                                       |                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20bbe-143">`ThemeColors`: \[ \] ![ capture d’écran de saut de ligne de l’élément dropdowncolorpicker avec l’attribut colortemplate défini sur’ThemeColors'. ](images/markup/colortemplate.themedcolors.1.png) \[ caractère\]</span><span class="sxs-lookup"><span data-stu-id="20bbe-143">`ThemeColors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'themecolors'.](images/markup/colortemplate.themedcolors.1.png)\[newline\]</span></span> | <span data-ttu-id="20bbe-144">`standardcolors`: \[ \] ![ capture d’écran de saut de ligne de l’élément dropdowncolorpicker avec l’attribut colortemplate défini sur’standardcolors'. ](images/markup/colortemplate.standardcolors.3.png) \[ caractère\]</span><span class="sxs-lookup"><span data-stu-id="20bbe-144">`standardcolors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'standardcolors'.](images/markup/colortemplate.standardcolors.3.png)\[newline\]</span></span> | <span data-ttu-id="20bbe-145">`highlightcolors`: \[ \] ![ capture d’écran de saut de ligne de l’élément dropdowncolorpicker avec l’attribut colortemplate défini sur’highlightcolors'.](images/markup/colortemplate.highlightcolors.2.png)</span><span class="sxs-lookup"><span data-stu-id="20bbe-145">`highlightcolors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'highlightcolors'.](images/markup/colortemplate.highlightcolors.2.png)</span></span><br/> |



 

<span data-ttu-id="20bbe-146">Le balisage de base requis pour chaque type de sélecteur de couleurs Drop-Down est illustré dans les exemples suivants :</span><span class="sxs-lookup"><span data-stu-id="20bbe-146">The basic markup required for each Drop-Down Color Picker type is demonstrated in the following examples:</span></span>

> [!Note]  
> <span data-ttu-id="20bbe-147">Le sélecteur de couleurs Drop-Down est un contrôle [bouton](windowsribbon-controls-button.md) valide dans un modèle [**SizeDefinition**](windowsribbon-element-sizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="20bbe-147">The Drop-Down Color Picker is a valid [Button](windowsribbon-controls-button.md) control in a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template.</span></span>

 


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


```XML

<Group CommandName=&quot;cmdDropDownColorPickerGroup&quot;
       SizeDefinition=&quot;ThreeButtons&quot;>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerThemeColors&quot;
    ColorTemplate=&quot;ThemeColors&quot;/>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerStandardColors&quot;
    ColorTemplate=&quot;StandardColors&quot;/>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerHighlightColors&quot;
    ColorTemplate=&quot;HighlightColors&quot;
    StandardColorGridRows=&quot;1&quot;/>
</Group>
```





## <a name="code"></a><span data-ttu-id="20bbe-148">Code</span><span class="sxs-lookup"><span data-stu-id="20bbe-148">Code</span></span>

<span data-ttu-id="20bbe-149">En tant que contrôle spécialisé qui prend en charge la personnalisation, toute implémentation du sélecteur de couleurs Drop-Down qui tire parti de ces fonctionnalités nécessite un code d’application spécialisé pour gérer les propriétés et gérer les commandes émises par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="20bbe-149">As a specialized control that supports customization, any implemention of the Drop-Down Color Picker that takes advantage of these capabilities requires specialized application code to manage properties and handle any Commands issued by the control.</span></span>

### <a name="properties"></a><span data-ttu-id="20bbe-150">Propriétés</span><span class="sxs-lookup"><span data-stu-id="20bbe-150">Properties</span></span>

<span data-ttu-id="20bbe-151">L’infrastructure du ruban définit une collection de [clés de propriété](windowsribbon-reference-properties.md) pour le contrôle de sélecteur de couleurs Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="20bbe-151">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Drop-Down Color Picker control.</span></span>

<span data-ttu-id="20bbe-152">En règle générale, une Drop-Down propriété du sélecteur de couleurs est mise à jour dans l’interface ruban en invalidant la commande associée au contrôle via un appel à la méthode [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="20bbe-152">Typically, a Drop-Down Color Picker property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="20bbe-153">L’événement d’invalidation est géré, et les mises à jour de la propriété sont définies par la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="20bbe-153">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="20bbe-154">La méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) n’est pas exécutée et l’application a interrogé une valeur de propriété mise à jour, jusqu’à ce que la propriété soit requise par le Framework.</span><span class="sxs-lookup"><span data-stu-id="20bbe-154">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="20bbe-155">Par exemple, lorsqu’un onglet est activé et qu’un contrôle est affiché dans l’interface ruban, ou lorsqu’une info-bulle est affichée.</span><span class="sxs-lookup"><span data-stu-id="20bbe-155">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="20bbe-156">Dans certains cas, une propriété peut être récupérée par le biais de la méthode [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et définie avec la méthode [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="20bbe-156">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="20bbe-157">Le tableau suivant répertorie les clés de propriété associées au contrôle de sélecteur de couleurs Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="20bbe-157">The following table lists the property keys that are associated with the Drop-Down Color Picker control.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20bbe-158">Clé de propriété</span><span class="sxs-lookup"><span data-stu-id="20bbe-158">Property Key</span></span></th>
<th><span data-ttu-id="20bbe-159">Description</span><span class="sxs-lookup"><span data-stu-id="20bbe-159">Description</span></span></th>
<th><span data-ttu-id="20bbe-160">Notes</span><span class="sxs-lookup"><span data-stu-id="20bbe-160">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="20bbe-161"><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></span><span class="sxs-lookup"><span data-stu-id="20bbe-161"><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></span></span></td>
<td><span data-ttu-id="20bbe-162">Définit l’étiquette du bouton de couleur <strong>automatique</strong> .</span><span class="sxs-lookup"><span data-stu-id="20bbe-162">Defines the label for the <strong>Automatic</strong> color button.</span></span><br/> <span data-ttu-id="20bbe-163">Valide uniquement lorsque <em>ColorTemplate</em> a la valeur <code>ThemeColors</code> ou <code>StandardColors</code> .</span><span class="sxs-lookup"><span data-stu-id="20bbe-163">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
<td><span data-ttu-id="20bbe-164">Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="20bbe-164">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20bbe-165"><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></span><span class="sxs-lookup"><span data-stu-id="20bbe-165"><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></span></span></td>
<td><span data-ttu-id="20bbe-166">Définit la valeur de couleur sélectionnée en tant que <a href="/windows/win32/gdi/colorref">COLORREF</a>.</span><span class="sxs-lookup"><span data-stu-id="20bbe-166">Defines the selected color value as a <a href="/windows/win32/gdi/colorref">COLORREF</a>.</span></span><br/> <span data-ttu-id="20bbe-167">Valide uniquement lorsque <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> a la valeur <code>UI_SWATCHCOLORTYPE_RGB</code> .</span><span class="sxs-lookup"><span data-stu-id="20bbe-167">Only valid when <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> has a value of <code>UI_SWATCHCOLORTYPE_RGB</code>.</span></span><br/></td>
<td><span data-ttu-id="20bbe-168">Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="20bbe-168">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20bbe-169"><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></span><span class="sxs-lookup"><span data-stu-id="20bbe-169"><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></span></span></td>
<td><span data-ttu-id="20bbe-170">Définit le type de couleur sélectionné.</span><span class="sxs-lookup"><span data-stu-id="20bbe-170">Defines the selected color type.</span></span><br/></td>
<td><span data-ttu-id="20bbe-171">Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="20bbe-171">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20bbe-172"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="20bbe-172"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="20bbe-173">Définit la capacité d’un contrôle à répondre à l’interaction de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="20bbe-173">Defines the ability for a control to respond to user interaction.</span></span><br/></td>
<td><span data-ttu-id="20bbe-174">Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="20bbe-174">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20bbe-175"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="20bbe-175"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>

<td><span data-ttu-id="20bbe-176">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="20bbe-176">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20bbe-177"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="20bbe-177"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="20bbe-178">Définit la chaîne de caractères pour une étiquette de contrôle.</span><span class="sxs-lookup"><span data-stu-id="20bbe-178">Defines the character string for a control label.</span></span><br/></td>
<td><span data-ttu-id="20bbe-179">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="20bbe-179">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20bbe-180"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="20bbe-180"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="20bbe-181">Définit la grande image à contraste élevé à afficher pour un contrôle.</span><span class="sxs-lookup"><span data-stu-id="20bbe-181">Defines the large high-contrast image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="20bbe-182">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="20bbe-182">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="20bbe-183">Pour plus d’informations sur les formats d’image, consultez <a href="windowsribbon-imageformats.md">spécification des ressources d’image de ruban</a>.</span><span class="sxs-lookup"><span data-stu-id="20bbe-183">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20bbe-184"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="20bbe-184"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="20bbe-185">Définit la grande image à afficher pour un contrôle.</span><span class="sxs-lookup"><span data-stu-id="20bbe-185">Defines the large image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="20bbe-186">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="20bbe-186">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="20bbe-187">Pour plus d’informations sur les formats d’image, consultez <a href="windowsribbon-imageformats.md">spécification des ressources d’image de ruban</a>.</span><span class="sxs-lookup"><span data-stu-id="20bbe-187">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20bbe-188"><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></span><span class="sxs-lookup"><span data-stu-id="20bbe-188"><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></span></span></td>
<td><span data-ttu-id="20bbe-189">Définit l’étiquette du bouton <strong>plus de couleurs</strong> ....</span><span class="sxs-lookup"><span data-stu-id="20bbe-189">Defines the label for the <strong>More colors...</strong> button.</span></span><br/> <span data-ttu-id="20bbe-190">Valide uniquement lorsque <em>ColorTemplate</em> a la valeur <code>ThemeColors</code> ou <code>StandardColors</code> .</span><span class="sxs-lookup"><span data-stu-id="20bbe-190">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
<td><span data-ttu-id="20bbe-191">Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="20bbe-191">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20bbe-192"><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></span><span class="sxs-lookup"><span data-stu-id="20bbe-192"><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></span></span></td>
<td><span data-ttu-id="20bbe-193">Définit l’étiquette du bouton <strong>aucune couleur</strong> .</span><span class="sxs-lookup"><span data-stu-id="20bbe-193">Defines the label for the <strong>No color</strong> button.</span></span><br/> <span data-ttu-id="20bbe-194">Valide pour toutes les valeurs <em>ColorTemplate</em> .</span><span class="sxs-lookup"><span data-stu-id="20bbe-194">Valid for all <em>ColorTemplate</em> values.</span></span><br/></td>
<td><span data-ttu-id="20bbe-195">Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="20bbe-195">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20bbe-196"><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="20bbe-196"><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="20bbe-197">Définit l’étiquette de la catégorie des <strong>couleurs récentes</strong> .</span><span class="sxs-lookup"><span data-stu-id="20bbe-197">Defines the label for the <strong>Recent colors</strong> category.</span></span><br/> <span data-ttu-id="20bbe-198">Valide uniquement lorsque <em>ColorTemplate</em> a la valeur <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="20bbe-198">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="20bbe-199">Il s’agit du seul modèle qui contient des catégories étiquetées.</span><span class="sxs-lookup"><span data-stu-id="20bbe-199">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="20bbe-200">Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="20bbe-200">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20bbe-201"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="20bbe-201"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="20bbe-202">Définit la petite image à contraste élevé à afficher pour un contrôle.</span><span class="sxs-lookup"><span data-stu-id="20bbe-202">Defines the small high-contrast image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="20bbe-203">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="20bbe-203">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="20bbe-204">Pour plus d’informations sur les formats d’image, consultez <a href="windowsribbon-imageformats.md">spécification des ressources d’image de ruban</a>.</span><span class="sxs-lookup"><span data-stu-id="20bbe-204">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20bbe-205"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="20bbe-205"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="20bbe-206">Définit la petite image à afficher pour un contrôle.</span><span class="sxs-lookup"><span data-stu-id="20bbe-206">Defines the small image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="20bbe-207">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="20bbe-207">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="20bbe-208">Pour plus d’informations sur les formats d’image, consultez <a href="windowsribbon-imageformats.md">spécification des ressources d’image de ruban</a>.</span><span class="sxs-lookup"><span data-stu-id="20bbe-208">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20bbe-209"><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></span><span class="sxs-lookup"><span data-stu-id="20bbe-209"><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></span></span></td>
<td><span data-ttu-id="20bbe-210">Définit un tableau de valeurs <a href="/windows/win32/gdi/colorref">COLORREF</a> pour les nuanciers d’un sélecteur de couleurs Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="20bbe-210">Defines an array of <a href="/windows/win32/gdi/colorref">COLORREF</a> values for the swatches of a Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="20bbe-211">Chaque Drop-Down sélecteur de couleurs <em>ColorTemplate</em> contient une <code>StandardColors</code> grille.</span><span class="sxs-lookup"><span data-stu-id="20bbe-211">Each Drop-Down Color Picker <em>ColorTemplate</em> contains a <code>StandardColors</code> grid.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="20bbe-212">Les valeurs <a href="/windows/win32/gdi/colorref">COLORREF</a> des <em>colonnes</em> <em>StandardColorGridRows</em> x initiales du tableau sont affichées.</span><span class="sxs-lookup"><span data-stu-id="20bbe-212">The <a href="/windows/win32/gdi/colorref">COLORREF</a> values from the initial <em>StandardColorGridRows</em> x <em>Columns</em> of the array are displayed.</span></span> <span data-ttu-id="20bbe-213">Si le tableau définit moins de couleurs que le nombre d' <code>StandardColors</code> échantillons déclarés dans le balisage, les espaces vides s’affichent pour les puces manquantes.</span><span class="sxs-lookup"><span data-stu-id="20bbe-213">If the array defines fewer colors than the number of <code>StandardColors</code> swatches declared in markup, empty spaces are displayed for the missing chips.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="20bbe-214">Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="20bbe-214">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20bbe-215"><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="20bbe-215"><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="20bbe-216">Définit l’étiquette de la catégorie de <strong>couleurs standard</strong> .</span><span class="sxs-lookup"><span data-stu-id="20bbe-216">Defines the label for the <strong>Standard colors</strong> category.</span></span><br/> <span data-ttu-id="20bbe-217">Valide uniquement lorsque <em>ColorTemplate</em> a la valeur <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="20bbe-217">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="20bbe-218">Il s’agit du seul modèle qui contient des catégories étiquetées.</span><span class="sxs-lookup"><span data-stu-id="20bbe-218">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="20bbe-219">Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="20bbe-219">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20bbe-220"><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></span><span class="sxs-lookup"><span data-stu-id="20bbe-220"><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></span></span></td>
<td><span data-ttu-id="20bbe-221">Définit un tableau de chaînes d’info-bulles d’échantillons de couleurs pour la <code>StandardColors</code> grille.</span><span class="sxs-lookup"><span data-stu-id="20bbe-221">Defines a string array of color swatch tooltips for the <code>StandardColors</code> grid.</span></span><br/> <span data-ttu-id="20bbe-222">Chaque Drop-Down sélecteur de couleurs <em>ColorTemplate</em> contient une <code>StandardColors</code> grille.</span><span class="sxs-lookup"><span data-stu-id="20bbe-222">Each Drop-Down Color Picker <em>ColorTemplate</em> contains a <code>StandardColors</code> grid.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="20bbe-223">Seuls les conseils d’outils requis pour étiqueter les échantillons de couleurs affichés dans la <code>StandardColors</code> grille sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="20bbe-223">Only those tool tips required to label the color swatches displayed in the <code>StandardColors</code> grid are used.</span></span> <span data-ttu-id="20bbe-224">Si moins d’étiquettes sont fournies que le nombre d’échantillons dans la <code>StandardColors</code> grille, une valeur par défaut est fournie pour les échantillons remainining.</span><span class="sxs-lookup"><span data-stu-id="20bbe-224">If fewer labels are supplied than the number of swatches in the <code>StandardColors</code> grid, a default is provided for the remainining swatches.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="20bbe-225">Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="20bbe-225">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20bbe-226"><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></span><span class="sxs-lookup"><span data-stu-id="20bbe-226"><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></span></span></td>
<td><span data-ttu-id="20bbe-227">Définit un tableau de valeurs <a href="/windows/win32/gdi/colorref">COLORREF</a> pour les nuanciers d’un sélecteur de couleurs Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="20bbe-227">Defines an array of <a href="/windows/win32/gdi/colorref">COLORREF</a> values for the swatches of a Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="20bbe-228">Valide uniquement lorsque <em>ColorTemplate</em> a la valeur <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="20bbe-228">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="20bbe-229">Les valeurs <a href="/windows/win32/gdi/colorref">COLORREF</a> des <em>colonnes</em> <em>ThemeColorGridRows</em> x initiales du tableau sont affichées.</span><span class="sxs-lookup"><span data-stu-id="20bbe-229">The <a href="/windows/win32/gdi/colorref">COLORREF</a> values from the initial <em>ThemeColorGridRows</em> x <em>Columns</em> of the array are displayed.</span></span> <span data-ttu-id="20bbe-230">Si le tableau définit moins de couleurs que le nombre d' <code>ThemeColors</code> échantillons déclarés dans le balisage, les espaces vides s’affichent pour les puces manquantes.</span><span class="sxs-lookup"><span data-stu-id="20bbe-230">If the array defines fewer colors than the number of <code>ThemeColors</code> swatches declared in markup, empty spaces are displayed for the missing chips.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="20bbe-231">Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="20bbe-231">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20bbe-232"><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></span><span class="sxs-lookup"><span data-stu-id="20bbe-232"><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></span></span></td>
<td><span data-ttu-id="20bbe-233">Définit le tableau de chaînes des info-bulles des échantillons de couleurs pour la <code>ThemeColors</code> grille.</span><span class="sxs-lookup"><span data-stu-id="20bbe-233">Defines the string array of color swatch tooltips for the <code>ThemeColors</code> grid.</span></span><br/> <span data-ttu-id="20bbe-234">Valide uniquement lorsque <em>ColorTemplate</em> a la valeur <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="20bbe-234">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="20bbe-235">Seuls les conseils d’outils requis pour étiqueter les échantillons de couleurs affichés dans la <code>ThemeColors</code> grille sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="20bbe-235">Only those tool tips required to label the color swatches displayed in the <code>ThemeColors</code> grid are used.</span></span> <span data-ttu-id="20bbe-236">Si moins d’étiquettes sont fournies que le nombre d’échantillons dans la <code>ThemeColors</code> grille, une valeur par défaut est fournie pour les échantillons remainining.</span><span class="sxs-lookup"><span data-stu-id="20bbe-236">If fewer labels are supplied than the number of swatches in the <code>ThemeColors</code> grid, a default is provided for the remainining swatches.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="20bbe-237">Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="20bbe-237">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20bbe-238"><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="20bbe-238"><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="20bbe-239">Définit l’étiquette de la catégorie de <strong>couleurs de thème</strong> .</span><span class="sxs-lookup"><span data-stu-id="20bbe-239">Defines the label for the <strong>Theme colors</strong> category.</span></span><br/> <span data-ttu-id="20bbe-240">Valide uniquement lorsque <em>ColorTemplate</em> a la valeur <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="20bbe-240">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="20bbe-241">Il s’agit du seul modèle qui contient des catégories étiquetées.</span><span class="sxs-lookup"><span data-stu-id="20bbe-241">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="20bbe-242">Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="20bbe-242">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20bbe-243"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="20bbe-243"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="20bbe-244">Définit la chaîne de caractères pour une description d’info-bulle associée à un <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>.</span><span class="sxs-lookup"><span data-stu-id="20bbe-244">Defines the character string for a tooltip description associated with a <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>.</span></span><br/></td>
<td><span data-ttu-id="20bbe-245">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="20bbe-245">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20bbe-246"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="20bbe-246"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="20bbe-247">Définit la chaîne de caractères pour une info-bulle de commande.</span><span class="sxs-lookup"><span data-stu-id="20bbe-247">Defines the character string for a Command tooltip.</span></span><br/></td>
<td><span data-ttu-id="20bbe-248">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="20bbe-248">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="command-handlers"></a><span data-ttu-id="20bbe-249">Gestionnaires de commandes</span><span class="sxs-lookup"><span data-stu-id="20bbe-249">Command handlers</span></span>

<span data-ttu-id="20bbe-250">La méthode [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) est utilisée pour personnaliser un Drop-Down sélecteur de couleurs via les clés de propriété listées ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="20bbe-250">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) method is used to customize a Drop-Down Color Picker through the property keys listed above.</span></span> <span data-ttu-id="20bbe-251">L’exemple suivant montre comment définir les échantillons de couleur d’un Drop-Down sélecteur de couleurs, en fonction d’une préférence de style personnalisée ou d’une grille de nuances personnalisée déclarée dans le balisage.</span><span class="sxs-lookup"><span data-stu-id="20bbe-251">The following example demonstrates how to set the color swatches of a Drop-Down Color Picker, based on a custom style preference or a custom swatch grid that is declared in markup.</span></span>


```C++
STDMETHODIMP DropDownColorPickerHandler::UpdateProperty(
              UINT nCmdID,
              __in REFPROPERTYKEY key,
              __in_opt const PROPVARIANT* ppropvarCurrentValue,
              __out PROPVARIANT* ppropvarNewValue)
{
  HRESULT hr = E_NOTIMPL;
  if (key == UI_PKEY_ThemeColors)
  {
    COLORREF rThemeColors[TOT_THEME_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rThemeColors); i++)
    {
      // any COLORREF
      rThemeColors[i] = RGB(0, 255, 0); 
    }
    hr = InitPropVariantFromUInt32Vector(
           &rThemeColors, ARRAYSIZE(rThemeColors), ppropvarNewValue);
  }

  else if (key == UI_PKEY_StandardColors)
  {
    ULONG rStandardColors[TOT_STANDARD_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rStandardColors); i++)
    {
      // any COLORREF
      rStandardColors[i] = RGB(255, 0, 0); 
    }
    hr = InitPropVariantFromUInt32Vector(
           &rStandardColors, ARRAYSIZE(rStandardColors),ppropvarNewValue);
  }

  else if (key == UI_PKEY_ThemeColorsTooltips)
  {
    BSTR rThemeTooltips[TOT_THEME_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rThemeTooltips); i++)
    {
      // any constant character string
      rThemeTooltips[i] = L"Green"; 
    }
    hr = InitPropVariantFromStringVector((PCWSTR *)&rThemeTooltips, 50, ppropvarNewValue);
  }
  else if (key == UI_PKEY_StandardColorsTooltips)
  {
    static BSTR rStandardTooltips[TOT_STANDARD_COLORS];
    for (LONG i = 0; i < ARRAYSize(rStandardTooltips); i++)
    {
      // any constant character string
      rStandardTooltips[i] = L"Red"; 
    }
    hr = InitPropVariantFromStringVector(
           (PCWSTR *)&rStandardTooltips, 20, ppropvarNewValue);
  }
  return hr;
}
```



<span data-ttu-id="20bbe-252">L’exemple suivant illustre une implémentation de la méthode [**IUICommandHandler :: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) qui expose les couleurs de l’échantillon du sélecteur de couleurs Drop-Down à l’application du ruban.</span><span class="sxs-lookup"><span data-stu-id="20bbe-252">The following example demonstrates an implementation of the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) method that exposes the Drop-Down Color Picker swatch colors to the Ribbon application.</span></span>


```C++
STDMETHODIMP DropDownColorPickerHandler::Execute(
                 UINT nCmdID,
                 UI_EXECUTIONVERB verb,
                 __in_opt const PROPERTYKEY* key,
                 __in_opt const PROPVARIANT* ppropvarValue,
                 __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
  HRESULT hr = E_NOTIMPL;
  if (*key == UI_PKEY_ColorType)
  {
    UI_SWATCHCOLORTYPE uType = 
      (UI_SWATCHCOLORTYPE)PropVariantToUInt32WithDefault(
        *ppropvarValue, 
        UI_SWATCHCOLORTYPE_NOCOLOR);

    COLORREF color;
    switch(uType)
    {
      case UI_SWATCHCOLORTYPE_RGB:
        PROPVARIANT var;
        pCommandExecutionProperties->GetValue(UI_PKEY_Color, &var);
        color = PropVariantToUInt32WithDefault(var, 0);
        break;
      case UI_SWATCHCOLORTYPE_AUTOMATIC:
        color = COLOR_WINDOWTEXT;
        break;
      case UI_SWATCHCOLORTYPE_NOCOLOR:
        color = MSONoFill;
        break;
    }

    // do with your color what you will...
    gInternalColor = color;
    hr = S_OK;
  }
  return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="20bbe-253">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="20bbe-253">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20bbe-254">Bibliothèque de contrôles de l’infrastructure du ruban Windows</span><span class="sxs-lookup"><span data-stu-id="20bbe-254">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="20bbe-255">**Élément de balisage DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="20bbe-255">**DropDownColorPicker markup element**</span></span>](windowsribbon-element-dropdowncolorpicker.md)
</dt> <dt>

[<span data-ttu-id="20bbe-256">Propriétés du sélecteur de couleurs</span><span class="sxs-lookup"><span data-stu-id="20bbe-256">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> <dt>

[<span data-ttu-id="20bbe-257">Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle</span><span class="sxs-lookup"><span data-stu-id="20bbe-257">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> <dt>

[<span data-ttu-id="20bbe-258">Exemple DropDownColorPicker</span><span class="sxs-lookup"><span data-stu-id="20bbe-258">DropDownColorPicker Sample</span></span>](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

