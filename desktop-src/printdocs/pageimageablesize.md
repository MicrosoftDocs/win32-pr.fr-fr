---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 6b81814f-2d9e-4862-8633-6ba016c11dac
title: PageImageableSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1eef9012a7fda3eed6afd16add1d483c35c1111
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996106"
---
# <a name="pageimageablesize"></a>PageImageableSize

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Décrit le canevas Imaged pour la disposition et le rendu. Ce rapport est basé sur PageMediaSize et PageOrientation.

Les diagrammes suivants illustrent l’utilisation des variables PageImageableSize basée sur PageOrientation.

![diagramme qui affiche les mesures des pages](images/local-1641910626-image.png)

-   [Informations sur les éléments](#element-information)
-   [Contenu structurel](#structural-content)
-   [Contenu Extensible Markup Language (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informations sur les éléments



|                            |                     |
|----------------------------|---------------------|
| Nom | Value |
| Type d'élément<br/>    | Propriété<br/> |
| Préfixe d’étendue <br/> | Page<br/>     |
| Notes <br/>          | Aucun<br/>     |



 

## <a name="structural-content"></a>Contenu structurel

La structure XML de cet élément est :

``` syntax
<psf:Property name="psk:PageImageableSize">
  <psf:Property name="psk:ImageableSizeWidth">
    <psf:Value xsi:type="xs:integer">_ImageableSizeWidthValue_</psf:Value>
  </psf:Property>
  <psf:Property name="psk:ImageableSizeHeight">
    <psf:Value xsi:type="xs:integer">_ImageableSizeHeightValue_</psf:Value>
  </psf:Property>
  <!--Specifies the imageable area within the logical page.  -->
  <psf:Property name="psk:ImageableArea">
    <psf:Property name="psk:OriginWidth">
      <psf:Value xsi:type="xs:integer">_OriginWidthValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:OriginHeight">
      <psf:Value xsi:type="xs:integer">_OriginHeightValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentWidth">
      <psf:Value xsi:type="xs:integer">_ExtentWidthValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentHeight">
      <psf:Value xsi:type="xs:integer">_ExtentHeightValue_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="structure-variables"></a>Variables de structure

Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.



| Nom                                    | Type de données          | Unité               | Valeurs prises en charge                       | Résumé                                                                                                                    |
|-----------------------------------------|--------------------|--------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| \_ImageableSizeWidthValue\_<br/>  | entier<br/> | microns<br/> | Supérieur à 0.<br/>             | Spécifie la dimension horizontale de la taille du média d’application par rapport au PageOrientation.<br/>               |
| \_ImageableSizeHeightValue\_<br/> | entier<br/> | microns<br/> | Supérieur à 0.<br/>             | Spécifie la dimension verticale de la taille du média d’application par rapport au PageOrientation.<br/>                 |
| \_OriginWidthValue\_<br/>         | entier<br/> | microns<br/> | Supérieur ou égal à 0.<br/> | Spécifie l’origine horizontale de la zone imageable par rapport à la taille du média d’application.<br/>                   |
| \_OriginHeightValue\_<br/>        | entier<br/> | microns<br/> | Supérieur ou égal à 0.<br/> | Spécifie l’origine verticale de la zone imageable par rapport à la taille du média d’application.<br/>                     |
| \_ExtentWidthValue\_<br/>         | entier<br/> | microns<br/> | Supérieur à 0.<br/>             | Spécifie la distance horizontale entre l’origine et la limite limite de la taille du média d’application.<br/>      |
| \_ExtentHeightValue\_<br/>        | entier<br/> | microns<br/> | Supérieur à 0.<br/>             | Spécifie la distance verticale entre l’origine et la limite limite de la taille du média de l’application de canevas.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Contenu Extensible Markup Language (XML)

Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms. Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :

``` syntax
<psf:Property name="psk:PageImageableSize">
  <psf:Property name="psk:ImageableSizeWidth">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psk:ImageableSizeHeight">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
    <psf:Property name="psk:ImageableArea">
      <psf:Property name="psk:OriginWidth">
        <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
      </psf:Property>
    <psf:Property name="psk:OriginHeight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentWidth">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentHeight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
  
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




