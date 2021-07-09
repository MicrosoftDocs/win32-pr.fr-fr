---
description: Obtenir des informations sur le paramètre PageMediaSizePSWidthOffset. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: b93ad6e6-ab27-4fab-b488-6f402b6ee857
title: PageMediaSizePSWidthOffset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 265acad803dbc334be115440e195967465b3ef50
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549099"
---
# <a name="pagemediasizepswidthoffset"></a>PageMediaSizePSWidthOffset

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

spécifie le décalage perpendiculaire à la direction de l’orientation du flux (référence [PostScript spécification du Format du fichier de Description](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)de l’imprimante).

-   [Informations sur les éléments](#element-information)
-   [Structure de contenu](#structure-content)

## <a name="element-information"></a>Informations sur les éléments



| Nom | Valeur |
|----------------------------|-------------------------------------------------------------|
| Type d'élément <br/>   | ParameterDef<br/>                                     |
| Préfixe d’étendue <br/> | Page<br/>                                             |
| Remarques <br/>          | Lié à l’élément PageMediaSize, option CustomPS<br/> |



 

## <a name="structure-content"></a>Structure de contenu

La structure XML de cet élément est :

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSWidthOffset">
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
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
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



| Propriété                | xsi:type           | Valeur                      |
|-------------------------|--------------------|----------------------------|
| DataType<br/>     | string<br/>  | xs:integer<br/>      |
| DefaultValue<br/> | entier<br/> | non défini<br/>       |
| MaxValue<br/>     | entier<br/> | non défini<br/>       |
| MinValue<br/>     | entier<br/> | non défini<br/>       |
| Obligatoire<br/>    | string<br/>  | PSK : conditionnel<br/> |
| Multiple<br/>     | integer<br/> | 1<br/>               |
| Unité<br/>     | string<br/>  | microns<br/>         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[PostScript Spécification de format de fichier de description d’imprimante](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




