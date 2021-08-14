---
title: Sélecteur de couleurs Drop-Down
description: l’infrastructure du ruban Windows fournit un contrôle de sélecteur de couleurs Drop-Down spécialisé qui expose un large éventail de paramètres de couleur via un bouton partagé et un sélecteur de couleur déroulant personnalisable.
ms.assetid: 65e1fc23-7ac0-4bb3-9359-28ce88acf356
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e8104ba92d0be9d56607083508d7f30728a7f3a141839d74314561d392fb942
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118707659"
---
# <a name="drop-down-color-picker"></a>Sélecteur de couleurs Drop-Down

l’infrastructure du ruban Windows fournit un contrôle de sélecteur de couleurs Drop-Down spécialisé qui expose un large éventail de paramètres de couleur via un bouton partagé et un sélecteur de couleur déroulant personnalisable.

-   [Introduction](#introduction)
-   [balisage](#markup)
-   [Code](#code)
    -   [Propriétés](#properties)
    -   [Gestionnaires de commandes](#command-handlers)
-   [Rubriques connexes](#related-topics)

## <a name="introduction"></a>Introduction

en émulant l’apparence et la fonctionnalité du sélecteur de couleurs Microsoft Office, l’infrastructure du ruban peut à la fois tirer parti de et contribuer à la cohérence et à la familiarité dans un large éventail d’applications.

## <a name="markup"></a>balisage

Comme tous les contrôles de ruban, le sélecteur de couleurs Drop-Down est facilement implémenté et personnalisé par le biais du balisage. L’infrastructure fournit un certain nombre d’attributs d’élément pour le sélecteur de couleurs Drop-Down pour exposer différents niveaux de fonctionnalité. Le tableau suivant répertorie les attributs du sélecteur de couleurs Drop-Down.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ColorTemplate</td>
<td>Modèles de disposition qui spécifient le type de Drop-Down sélecteur de couleurs.<br/> Il existe trois modèles, chacun spécifiant une disposition de contrôle et des valeurs par défaut pour les attributs et les clés de propriété associés. <br/>
<ul>
<li><code>ThemeColors</code></li>
<li><code>StandardColors</code></li>
<li><code>HighlightColors</code></li>
</ul></td>
</tr>
<tr class="even">
<td>Copeaux</td>
<td>Taille de chaque puce de couleur (ou nuance).<br/>
<ul>
<li><code>Small</code></li>
<li><code>Medium</code></li>
<li><code>Large</code></li>
</ul></td>
</tr>
<tr class="odd">
<td>Colonnes</td>
<td>Nombre de colonnes de la puce de couleur (ou de l’échantillon).<br/></td>
</tr>
<tr class="even">
<td>CommandName</td>
<td>Nom de la déclaration de commande associée. <br/></td>
</tr>
<tr class="odd">
<td>IsAutomaticColorButtonVisible</td>
<td>Affiche (ou masque) le bouton <strong>automatique</strong> .<br/> Valide uniquement lorsque <em>ColorTemplate</em> a la valeur <code>ThemeColors</code> ou <code>StandardColors</code> .<br/></td>
</tr>
<tr class="even">
<td>IsNoColorButtonVisible</td>
<td>Affiche (ou masque) le bouton <strong>aucune couleur</strong> .<br/> Valide pour toutes les valeurs <em>ColorTemplate</em> .<br/></td>
</tr>
<tr class="odd">
<td>RecentColorGridRows</td>
<td>Nombre de lignes de la puce de couleur (ou de l’échantillon) dans la zone <strong>couleurs récentes</strong> .<br/> Valide uniquement lorsque <em>ColorTemplate</em> a la valeur <code>ThemeColors</code> .<br/></td>
</tr>
<tr class="even">
<td>StandardColorGridRows</td>
<td>Nombre de lignes de puce de couleur (ou d’échantillon) dans la zone de <strong>couleurs standard</strong> .<br/></td>
</tr>
<tr class="odd">
<td>ThemeColorGridRows</td>
<td>Nombre de lignes de puce de couleur (ou d’échantillon) dans la zone de <strong>couleurs de thème</strong> .<br/> Valide uniquement lorsque <em>ColorTemplate</em> a la valeur <code>ThemeColors</code> .<br/></td>
</tr>
</tbody>
</table>



 

Les captures d’écran suivantes illustrent les dispositions par défaut du sélecteur de couleurs Drop-Down pour les trois modèles de couleurs.



|     &nbsp;     |  &nbsp;   | &nbsp;  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ThemeColors`: \[ \] ![ capture d’écran de saut de ligne de l’élément dropdowncolorpicker avec l’attribut colortemplate défini sur’ThemeColors'. ](images/markup/colortemplate.themedcolors.1.png) \[ caractère\] | `standardcolors`: \[ \] ![ capture d’écran de saut de ligne de l’élément dropdowncolorpicker avec l’attribut colortemplate défini sur’standardcolors'. ](images/markup/colortemplate.standardcolors.3.png) \[ caractère\] | `highlightcolors`: \[ \] ![ capture d’écran de saut de ligne de l’élément dropdowncolorpicker avec l’attribut colortemplate défini sur’highlightcolors'.](images/markup/colortemplate.highlightcolors.2.png)<br/> |



 

Le balisage de base requis pour chaque type de sélecteur de couleurs Drop-Down est illustré dans les exemples suivants :

> [!Note]  
> Le sélecteur de couleurs Drop-Down est un contrôle [bouton](windowsribbon-controls-button.md) valide dans un modèle [**SizeDefinition**](windowsribbon-element-sizedefinition.md) .

 


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





## <a name="code"></a>Code

En tant que contrôle spécialisé qui prend en charge la personnalisation, toute implémentation du sélecteur de couleurs Drop-Down qui tire parti de ces fonctionnalités nécessite un code d’application spécialisé pour gérer les propriétés et gérer les commandes émises par le contrôle.

### <a name="properties"></a>Propriétés

L’infrastructure du ruban définit une collection de [clés de propriété](windowsribbon-reference-properties.md) pour le contrôle de sélecteur de couleurs Drop-Down.

En règle générale, une Drop-Down propriété du sélecteur de couleurs est mise à jour dans l’interface ruban en invalidant la commande associée au contrôle via un appel à la méthode [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . L’événement d’invalidation est géré, et les mises à jour de la propriété sont définies par la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

La méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) n’est pas exécutée et l’application a interrogé une valeur de propriété mise à jour, jusqu’à ce que la propriété soit requise par le Framework. Par exemple, lorsqu’un onglet est activé et qu’un contrôle est affiché dans l’interface ruban, ou lorsqu’une info-bulle est affichée.

> [!Note]  
> Dans certains cas, une propriété peut être récupérée par le biais de la méthode [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et définie avec la méthode [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

Le tableau suivant répertorie les clés de propriété associées au contrôle de sélecteur de couleurs Drop-Down.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Clé de propriété</th>
<th>Description</th>
<th>Remarques</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></td>
<td>Définit l’étiquette du bouton de couleur <strong>automatique</strong> .<br/> Valide uniquement lorsque <em>ColorTemplate</em> a la valeur <code>ThemeColors</code> ou <code>StandardColors</code> .<br/></td>
<td>Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></td>
<td>Définit la valeur de couleur sélectionnée en tant que <a href="/windows/win32/gdi/colorref">COLORREF</a>.<br/> Valide uniquement lorsque <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> a la valeur <code>UI_SWATCHCOLORTYPE_RGB</code> .<br/></td>
<td>Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></td>
<td>Définit le type de couleur sélectionné.<br/></td>
<td>Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></td>
<td>Définit la capacité d’un contrôle à répondre à l’interaction de l’utilisateur.<br/></td>
<td>Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></td>

<td>Peut uniquement être mis à jour par le biais d’une invalidation.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></td>
<td>Définit la chaîne de caractères pour une étiquette de contrôle.<br/></td>
<td>Peut uniquement être mis à jour par le biais d’une invalidation.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></td>
<td>Définit la grande image à contraste élevé à afficher pour un contrôle.<br/></td>
<td>Peut uniquement être mis à jour par le biais d’une invalidation.<br/> Pour plus d’informations sur les formats d’image, consultez <a href="windowsribbon-imageformats.md">spécification des ressources d’image de ruban</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></td>
<td>Définit la grande image à afficher pour un contrôle.<br/></td>
<td>Peut uniquement être mis à jour par le biais d’une invalidation.<br/> Pour plus d’informations sur les formats d’image, consultez <a href="windowsribbon-imageformats.md">spécification des ressources d’image de ruban</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></td>
<td>Définit l’étiquette du bouton <strong>plus de couleurs</strong> ....<br/> Valide uniquement lorsque <em>ColorTemplate</em> a la valeur <code>ThemeColors</code> ou <code>StandardColors</code> .<br/></td>
<td>Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></td>
<td>Définit l’étiquette du bouton <strong>aucune couleur</strong> .<br/> Valide pour toutes les valeurs <em>ColorTemplate</em> .<br/></td>
<td>Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></td>
<td>Définit l’étiquette de la catégorie des <strong>couleurs récentes</strong> .<br/> Valide uniquement lorsque <em>ColorTemplate</em> a la valeur <code>ThemeColors</code> . Il s’agit du seul modèle qui contient des catégories étiquetées.<br/></td>
<td>Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></td>
<td>Définit la petite image à contraste élevé à afficher pour un contrôle.<br/></td>
<td>Peut uniquement être mis à jour par le biais d’une invalidation.<br/> Pour plus d’informations sur les formats d’image, consultez <a href="windowsribbon-imageformats.md">spécification des ressources d’image de ruban</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></td>
<td>Définit la petite image à afficher pour un contrôle.<br/></td>
<td>Peut uniquement être mis à jour par le biais d’une invalidation.<br/> Pour plus d’informations sur les formats d’image, consultez <a href="windowsribbon-imageformats.md">spécification des ressources d’image de ruban</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></td>
<td>Définit un tableau de valeurs <a href="/windows/win32/gdi/colorref">COLORREF</a> pour les nuanciers d’un sélecteur de couleurs Drop-Down.<br/> Chaque Drop-Down sélecteur de couleurs <em>ColorTemplate</em> contient une <code>StandardColors</code> grille. <br/>
<blockquote>
[!Note]<br />
Les valeurs <a href="/windows/win32/gdi/colorref">COLORREF</a> des <em>colonnes</em> <em>StandardColorGridRows</em> x initiales du tableau sont affichées. Si le tableau définit moins de couleurs que le nombre d' <code>StandardColors</code> échantillons déclarés dans le balisage, les espaces vides s’affichent pour les puces manquantes.
</blockquote>
<br/></td>
<td>Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></td>
<td>Définit l’étiquette de la catégorie de <strong>couleurs standard</strong> .<br/> Valide uniquement lorsque <em>ColorTemplate</em> a la valeur <code>ThemeColors</code> . Il s’agit du seul modèle qui contient des catégories étiquetées.<br/></td>
<td>Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></td>
<td>Définit un tableau de chaînes d’info-bulles d’échantillons de couleurs pour la <code>StandardColors</code> grille.<br/> Chaque Drop-Down sélecteur de couleurs <em>ColorTemplate</em> contient une <code>StandardColors</code> grille. <br/>
<blockquote>
[!Note]<br />
Seuls les conseils d’outils requis pour étiqueter les échantillons de couleurs affichés dans la <code>StandardColors</code> grille sont utilisés. Si moins d’étiquettes sont fournies que le nombre d’échantillons dans la <code>StandardColors</code> grille, une valeur par défaut est fournie pour les échantillons remainining.
</blockquote>
<br/></td>
<td>Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></td>
<td>Définit un tableau de valeurs <a href="/windows/win32/gdi/colorref">COLORREF</a> pour les nuanciers d’un sélecteur de couleurs Drop-Down.<br/> Valide uniquement lorsque <em>ColorTemplate</em> a la valeur <code>ThemeColors</code> . <br/>
<blockquote>
[!Note]<br />
Les valeurs <a href="/windows/win32/gdi/colorref">COLORREF</a> des <em>colonnes</em> <em>ThemeColorGridRows</em> x initiales du tableau sont affichées. Si le tableau définit moins de couleurs que le nombre d' <code>ThemeColors</code> échantillons déclarés dans le balisage, les espaces vides s’affichent pour les puces manquantes.
</blockquote>
<br/></td>
<td>Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></td>
<td>Définit le tableau de chaînes des info-bulles des échantillons de couleurs pour la <code>ThemeColors</code> grille.<br/> Valide uniquement lorsque <em>ColorTemplate</em> a la valeur <code>ThemeColors</code> . <br/>
<blockquote>
[!Note]<br />
Seuls les conseils d’outils requis pour étiqueter les échantillons de couleurs affichés dans la <code>ThemeColors</code> grille sont utilisés. Si moins d’étiquettes sont fournies que le nombre d’échantillons dans la <code>ThemeColors</code> grille, une valeur par défaut est fournie pour les échantillons remainining.
</blockquote>
<br/></td>
<td>Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></td>
<td>Définit l’étiquette de la catégorie de <strong>couleurs de thème</strong> .<br/> Valide uniquement lorsque <em>ColorTemplate</em> a la valeur <code>ThemeColors</code> . Il s’agit du seul modèle qui contient des catégories étiquetées.<br/></td>
<td>Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></td>
<td>Définit la chaîne de caractères pour une description d’info-bulle associée à un <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>.<br/></td>
<td>Peut uniquement être mis à jour par le biais d’une invalidation.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></td>
<td>Définit la chaîne de caractères pour une info-bulle de commande.<br/></td>
<td>Peut uniquement être mis à jour par le biais d’une invalidation.</td>
</tr>
</tbody>
</table>



 

### <a name="command-handlers"></a>Gestionnaires de commandes

La méthode [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) est utilisée pour personnaliser un Drop-Down sélecteur de couleurs via les clés de propriété listées ci-dessus. L’exemple suivant montre comment définir les échantillons de couleur d’un Drop-Down sélecteur de couleurs, en fonction d’une préférence de style personnalisée ou d’une grille de nuances personnalisée déclarée dans le balisage.


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



L’exemple suivant illustre une implémentation de la méthode [**IUICommandHandler :: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) qui expose les couleurs de l’échantillon du sélecteur de couleurs Drop-Down à l’application du ruban.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Bibliothèque de contrôles de Framework du ruban](windowsribbon-controls-entry.md)
</dt> <dt>

[**Élément de balisage DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)
</dt> <dt>

[Propriétés du sélecteur de couleurs](windowsribbon-reference-properties-colorpicker.md)
</dt> <dt>

[Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle](windowsribbon-templates.md)
</dt> <dt>

[Exemple DropDownColorPicker](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

