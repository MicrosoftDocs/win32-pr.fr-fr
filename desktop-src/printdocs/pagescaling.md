---
description: En savoir plus sur l’élément PageScaling. Cet élément décrit les caractéristiques de mise à l’échelle de la sortie.
ms.assetid: cf35bb37-bf67-4e86-bfef-9838606982a5
title: PageScaling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4cf1a122f71148570cf69fc17455c8ca5c917ee4f441d1bc16be1922705eb81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948129"
---
# <a name="pagescaling"></a>PageScaling

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Décrit les caractéristiques de mise à l’échelle de la sortie. Certaines options de cette fonctionnalité requièrent que le consommateur soit en mesure de déterminer les caractéristiques des « dimensions de contenu de l’application ». En l’absence de la possibilité de déterminer ces caractéristiques, le consommateur doit avoir comme valeur par défaut l’option Identity. Ces caractéristiques sont les suivantes :



| Caractéristiques de la mise à l’échelle                         | Description                                                                                                                                                                                                                                                      |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Taille du média d’application   | Dimensions des médias définies par la disposition de l’application. La taille du média d’application peut ou ne peut pas correspondre à un PageMediaSize pris en charge par le consommateur.<br/>                                                                          |
| Taille du contenu de l’application | Dimensions des médias définies par la disposition de l’application. La taille du média d’application peut ou ne peut pas correspondre à un PageMediaSize pris en charge par le consommateur.<br/>                                                                          |
| Taille du fond perdu de l’application   | Le décalage et l’étendue de la zone de fond perdu de l’application, une zone de dépassement de capacité utilisée par l’application pour l’inscription et la mise en page, par rapport à la taille du support d’application. La zone de fond perdu est supérieure ou égale à la taille du média de l’application.<br/> |



 

-   [Informations sur les éléments](#element-information)
-   [Contenu structurel](#structural-content)
-   [Contenu Extensible Markup Language (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informations sur les éléments



| Nom | Valeur |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Type d'élément <br/>   | Fonctionnalité<br/>                                                                                                                                                                                    |
| Préfixe d’étendue <br/> | Page<br/>                                                                                                                                                                                       |
| Remarques <br/>          | Haut, bas, gauche et droite sont relatifs à PageImageableSize. Les coordonnées sont relatives à PageImageableSize, où l’origine de est relative à l’origine du PageImageableSize.<br/> |



 

## <a name="structural-content"></a>Contenu structurel

La structure XML de cet élément est :

``` syntax
<psf:Feature name="psk:PageScaling">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies offset of the width relative to the PageImageableSize.  
         Measured in microns. -->
    <psf:ScoredProperty name="psk:OffsetWidth">
      <psf:ParameterRef name="psk:PageScalingOffsetWidth" />
    </psf:ScoredProperty>
    <!-- Specifies offset of the height relative to the PageImageableSize.  
         Measured in microns. -->
    <psf:ScoredProperty name="psk:OffsetHeight">
      <psf:ParameterRef name="psk:PageScalingOffsetHeight" />
    </psf:ScoredProperty>
    <!-- Specifies the scaling percentage for the width dimension relative to the PageImageableSize. -->
    <psf:ScoredProperty name="psk:ScaleWidth">
      <psf:ParameterRef name="psk:PageScalingScaleWidth" />
    </psf:ScoredProperty>
    <!-- Specifies the scaling percentage for the height dimension relative to the PageImageableSize. -->
    <psf:ScoredProperty name="psk:ScaleHeight">
      <psf:ParameterRef name="psk:PageScalingScaleHeight" />
    </psf:ScoredProperty>
    <!-- Specifies the scaling percentage for square scaling (both dimensions are scaled equally). -->
    <psf:ScoredProperty name="psk:Scale">
      <psf:ParameterRef name="psk:PageScalingScale" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the alignment of the scaled content. -->
  <psf:Feature name="psk:ScaleOffsetAlignment">
    <!-- Specifies the scaling should be aligned on the center of the bottom edge of the media. -->
    <psf:Option name="psk:BottomCenter"/>
    <!-- Specifies the scaling should be aligned on the bottom left corner of the media. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies the scaling should be aligned on the bottom right corner of the media. -->
    <psf:Option name="psk:BottomRight "/>
    <!-- Specifies the scaling should be aligned on the bottom right corner of the media. -->
    <psf:Option name="psk:Center"/>
    <!-- Specifies the scaling should be aligned on the center of the left edge of the media. -->
    <psf:Option name="psk:LeftCenter"/>
    <!-- Specifies the scaling should be aligned on the center of the right edge of the media. -->
    <psf:Option name="psk:RightCenter"/>
    <!-- Specifies the scaling should be aligned on the center of the top edge of the media. -->
    <psf:Option name="psk:TopCenter"/>
    <!-- Specifies the scaling should be aligned on the top left corner of the media. -->
    <psf:Option name="psk:TopLeft"/>
    <!-- Specifies the scaling should be aligned on the top right corner of the media. -->
    <psf:Option name="psk:TopRight"/>
  </psf:Feature>
</psf:Feature>
```

## <a name="structure-variables"></a>Variables de structure

Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.



| Nom                               | Type de données         | Unité                  | Valeurs prises en charge                                                                                                                                                                      | Résumé                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| \_OptionName\_<br/>          | string<br/> | caractères<br/> | Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.<br/> | Nom de l'option.<br/>                                           |
| \_IdentityOptionValue\_<br/> | string<br/> | n/a<br/>        | True, False.<br/>                                                                                                                                                               | Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Contenu Extensible Markup Language (XML)

Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms. Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :

``` syntax
<psf:Feature name="psk:PageScaling">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:OffsetWidth">
      <psf:ParameterRef name="psk:PageScalingOffsetWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:OffsetHeight">
      <psf:ParameterRef name="psk:PageScalingOffsetHeight" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ScaleWidth">
      <psf:ParameterRef name="psk:PageScalingScaleWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ScaleHeight">
      <psf:ParameterRef name="psk:PageScalingScaleHeight" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a custom square scaling should be applied to the Application Media Size. -->
  <psf:Option name="psk:CustomSquare">
    <psf:ScoredProperty name="psk:OffsetWidth">
      <psf:ParameterRef name="psk:PageScalingOffsetWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:OffsetHeight">
      <psf:ParameterRef name="psk:PageScalingOffsetHeight" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Scale">
      <psf:ParameterRef name="psk:PageScalingScale" />
    </psf:ScoredProperty>
  </psf:Option>

  <!-- Specifies the application bleed size should be scaled to the PageImageableSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationBleedSizeToPageImageableSize" />
  <!-- Specifies the application content size should be scaled to the PageImageableSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationContentSizeToPageImageableSize" />
  <!-- Specifies the application media size should be scaled to the PageImageableSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationMediaSizeToPageImageableSize" />
  <!-- Specifies the application media size should be scaled to the PageMediaSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationMediaSizeToPageMediaSize" />

  <!-- Specifies that no scaling should be applied. -->
  <psf:Option name="psk:None" />

  <!-- Specifies the alignment of the scaled content. -->
  <psf:Feature name="psk:ScaleOffsetAlignment">
    <!-- Specifies the scaling should be aligned on the center of the bottom edge of the media. -->
    <psf:Option name="psk:BottomCenter" />
    <!-- Specifies the scaling should be aligned on the bottom left corner of the media.-->
    <psf:Option name="psk:BottomLeft" />
    <!--Specifies the scaling should be aligned on the bottom right corner of the media.-->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies the scaling should be centered on the media.-->
    <psf:Option name="psk:Center" />
    <!-- Specifies the scaling should be aligned on the center of the left edge of the media.-->
    <psf:Option name="psk:LeftCenter" />
    <!--Specifies the scaling should be aligned on the center of the right edge of the media.-->
    <psf:Option name="psk:RightCenter" />
    <!-- Specifies the scaling should be aligned on the center of the top edge of the media.-->
    <psf:Option name="psk:TopCenter" />
    <!--  Specifies the scaling should be aligned on the top left corner of the media.-->
    <psf:Option name="psk:TopLeft" />
    <!-- Specifies the scaling should be aligned on the top right corner of the media.-->
    <psf:Option name="psk:TopRight" />
  </psf:Feature>
</psf:Feature>
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




