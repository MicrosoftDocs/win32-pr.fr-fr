---
description: Obtenir des informations sur le paramètre PageWatermarkOriginHeight. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: ef429727-d881-408b-95ce-2acce667654a
title: PageWatermarkOriginHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25af5aa849cbf6d849afef2b11d2a39012818c8eabeccaeae8d77aa9e1925c84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034087"
---
# <a name="pagewatermarkoriginheight"></a>PageWatermarkOriginHeight

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Spécifie l’origine d’un filigrane par rapport à l’origine du PageImageableSize.

-   [Informations sur les éléments](#element-information)
-   [Structure de contenu](#structure-content)

## <a name="element-information"></a>Informations sur les éléments



| Name | Valeur |
|----------------------------|--------------------------------------------|
| Type d'élément <br/>   | ParameterDef<br/>                    |
| Préfixe d’étendue <br/> | Page<br/>                            |
| Notes <br/>          | Lié à l’élément PageWatermark<br/> |



 

## <a name="structure-content"></a>Structure de contenu

La structure XML de cet élément est la suivante :

``` syntax
<psf:ParameterDef name="psk:PageWatermarkOriginHeight">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a>Propriétés de structure

Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.



| Propriété                | xsi:type           | Valeur                                                                   |
|-------------------------|--------------------|-------------------------------------------------------------------------|
| DataType<br/>     | string<br/>  | xs:integer<br/>                                                   |
| DefaultValue<br/> | entier<br/> | non défini<br/>                                                    |
| MaxValue<br/>     | entier<br/> | Valeur inférieure ou égale à PageImageableSize-ExtentHeight<br/> |
| MinValue<br/>     | entier<br/> | 0<br/>                                                            |
| Plusieurs<br/>     | integer<br/> | 1<br/>                                                            |
| Obligatoire<br/>    | string<br/>  | PSK : conditionnel<br/>                                              |
| Unité<br/>     | string<br/>  | microns<br/>                                                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




