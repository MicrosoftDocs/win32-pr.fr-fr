---
title: Personnalisation des couleurs du ruban
description: l’infrastructure du ruban Windows expose un jeu de propriétés de couleur qui permettent à une application de personnaliser l’apparence de différents éléments de l’interface utilisateur du ruban au moment de l’exécution.
ms.assetid: e070aaca-d350-4336-8e5d-d5d9c8167287
keywords:
- Windows Ruban, personnalisation des couleurs
- Ruban, personnalisation des couleurs
- personnalisation des couleurs du ruban Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ef83c40d49656c82aabfbf41c4ec5375f7f3f54f063ccf30d917e740f87408
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710889"
---
# <a name="customizing-ribbon-colors"></a>Personnalisation des couleurs du ruban

l’infrastructure du ruban Windows expose un jeu de propriétés de couleur qui permettent à une application de personnaliser l’apparence de différents éléments de l’interface utilisateur du ruban au moment de l’exécution.

-   [Introduction](#introduction)
-   [Spécifier les couleurs du ruban](#specify-ribbon-colors)
-   [Convertir RVB en TSL](#convert-rgb-to-hsb)
-   [Rubriques connexes](#related-topics)

## <a name="introduction"></a>Introduction

Les [clés de propriété de Framework](windowsribbon-reference-properties-framework.md) répertoriées dans le tableau suivant sont utilisées pour définir la couleur des différents éléments d’interface utilisateur dans une application de ruban. Ces propriétés permettent à l’infrastructure du ruban de prendre en charge les spécifications de personnalisation, d’identité et de personnalisation entre les applications.

| Couleur du ruban                     | Clé de propriété du Framework                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Couleur d’arrière-plan                 | [IU \_ \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)                                                                                                                                                                                                                                                                                                                                                                 |
| couleur de surbrillance (Windows 7 uniquement) | [Interface utilisateur \_ le \_ ](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md)groupe de GlobalHighlightColor * * * * introduit dans Windows 8 * * : * * [ui \_ \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) ne peut pas être défini indépendamment de [l’interface utilisateur \_ \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).<br/> <br/>                                                              |
| Couleur du texte                       | [Interface utilisateur \_ le \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md)de la pièce * * * * a été introduit dans Windows 8 **:** les modifications apportées à la valeur par défaut de l' [ui « \_ \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) » dans Windows 8 peuvent nécessiter un ajustement de l' [interface utilisateur de l’iu \_ \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) dans les applications du ruban conçues pour Windows 7.<br/> <br/> |



 

## <a name="specify-ribbon-colors"></a>Spécifier les couleurs du ruban

L’infrastructure du ruban utilise un modèle de couleurs teinte, saturation, luminosité (TSL), qui diffère des espaces de couleurs teinte, saturation, luminosité (TSL) ou teinte, saturation, valeur (HSV) les plus courants. En particulier, B représente un niveau de luminosité ou de luminosité global plutôt que la clarté d’une couleur particulière.

Pour spécifier la couleur des éléments d’interface utilisateur dans l’infrastructure du ruban, une application assigne des valeurs TSL à chacune des propriétés de couleur globale. Ces valeurs sont ensuite appliquées universellement à tous les éléments de ruban comme requis par l’application ruban (l’infrastructure ne prend pas en charge l’affectation de valeurs TSL à des éléments et des contrôles individuels).

introduite dans Windows 8 * * : * *[l’ui \_ \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) a la même valeur que [l' \_ ui \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).

Le tableau suivant décrit les paramètres TSL de l’infrastructure du ruban.



Composant

Description

Valeurs ajustées\*

Teinte (H)

Le pigment, ou la couleur réelle, est généralement identifié en tant que valeur d’une plage circlular comprise entre 0 et 359 degrés.

0 (rouge) à 255 (rouge)

Saturation (S)

Pureté, ou saturation, de la couleur mesurée en pourcentage de 0 à 100%.

0 (gris) à 255 (saturé entièrement)

Luminosité (B)

Luminosité ou obscurité globale de la couleur mesurée en pourcentage de 0 à 100%.

0 (sombre) à 255 (clair)

\* La plage d’origine de chaque valeur de paramètre est traduite dans une plage comprise entre 0 et 255 pour le Framework.



 

Les valeurs TSL n’identifient pas les couleurs spécifiques. Au lieu de cela, la combinaison des valeurs de propriété TSL influence la manière dont les dégradés de couleur dans l’interface utilisateur sont ajustés l’un par rapport à l’autre.

Quand vous assignez des valeurs TSL personnalisées à [l’interface utilisateur \_ \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) et à [l’interface utilisateur \_ \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md), il est recommandé que ces valeurs soient suffisamment grandes pour garantir la lisibilité. Plus précisément, la couleur de texte doit être plus sombre que la nuance la plus légère de l’interface ruban. Le cas échéant, l’infrastructure ajuste automatiquement la \_ valeur TSL de l’interface utilisateur GlobalTextColor de l’interface utilisateur \_ pour fournir un contraste suffisant par rapport à n’importe quel dégradé ou nuance d’arrière-plan dérivé de l’interface utilisateur \_ \_ GlobalBackgroundColor.

> [!Note]  
> dans Windows 7, [l’interface de groupe de \_ \_ GlobalHighlightColor de l’interface utilisateur](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) peut être définie indépendamment de [l’interface utilisateur \_ \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).

 

L’exemple suivant montre comment spécifier une couleur personnalisée pour les propriétés de l' [interface utilisateur \_ \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md), de l' [interface utilisateur \_ \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)et de l' [interface utilisateur de \_ \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) .


```C++
CComPtr<IPropertyStore> spPropertyStore;

// _spFramework is a pointer to the IUIFramework interface that is assigned 
// when the Ribbon is initialized.
if (SUCCEEDED(_spFramework->QueryInterface(&spPropertyStore)))
{
  PROPVARIANT propvarBackground;
  PROPVARIANT propvarHighlight;
  PROPVARIANT propvarText;
 
  // UI_HSBCOLOR is a type defined in UIRibbon.h that is composed of 
  // three component values: hue, saturation and brightness, respectively.
  UI_HSBCOLOR BackgroundColor = UI_HSB(0x14, 0x38, 0x54);
  UI_HSBCOLOR HighlightColor = UI_HSB(0x00, 0x36, 0x87);
  UI_HSBCOLOR TextColor = UI_HSB(0x2B, 0xD6, 0x00);

  InitPropVariantFromUInt32(BackgroundColor, &propvarBackground);
  InitPropVariantFromUInt32(HighlightColor, &propvarHighlight);
  InitPropVariantFromUInt32(TextColor, &propvarText);
 
  spPropertyStore->SetValue(UI_PKEY_GlobalBackgroundColor, propvarBackground);
  spPropertyStore->SetValue(UI_PKEY_GlobalTextColor, propvarText);
 
  spPropertyStore->Commit();
}
```



## <a name="convert-rgb-to-hsb"></a>Convertir RVB en TSL

Cette section décrit la formule requise pour la correspondance dynamique d’une valeur TSL de l’infrastructure du ruban, le [ \_ \_ GlobalBackgroundColor de l’interface utilisateur](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) , dans cet exemple, à une couleur RVB spécifique au moment de l’exécution.

L’arrière-plan de la ligne d’onglet est utilisé comme point de référence, car il est rendu sous la forme d’une surface de couleur plate par rapport au dégradé de luminosité de l’arrière-plan du ruban.

Une conversion préliminaire est nécessaire pour obtenir une valeur TSL intermédiaire. Cette valeur TSL peut ensuite être convertie en valeur TSL.

> [!Note]  
> La conversion de RVB en TSL est facilement effectuée avec la plupart des logiciels de modification de photos.

 

La conversion de TSL (avec chaque composant de la plage comprise entre 0,0 et 1,0) en un paramètre TSL du ruban est effectuée à l’aide des formules suivantes :

-   H<sub>Background</sub> = Round (255.0 H)
-   S<sub>arrière-plan</sub> = Round (255.0 S)
-   B<sub>Background</sub> = Round (257.7 + 149,9 ln (L)) si 0,1793 <= L <= 0,9821

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Recommandations relatives aux couleurs](https://msdn.microsoft.com/library/aa511283.aspx)
</dt> <dt>

[Propriétés du Framework](windowsribbon-reference-properties-framework.md)
</dt> </dl>

 

 





