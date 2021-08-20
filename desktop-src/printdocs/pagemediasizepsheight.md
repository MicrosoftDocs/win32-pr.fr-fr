---
description: Obtenir des informations sur le paramètre PageMediaSizePSHeight. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 857caf51-ccf6-415c-aab3-1fed50fa7b34
title: PageMediaSizePSHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53af9494fe895c16fd884e06991b3072f320261e6a47d5fd7f2f06e029bff2d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117868204"
---
# <a name="pagemediasizepsheight"></a>PageMediaSizePSHeight

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

spécifie la hauteur de la page, parallèle à la direction de l’orientation du flux (référence [PostScript spécification du Format du fichier de Description](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)de l’imprimante).

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
<psf:ParameterDef name="psk:PageMediaSizePSHeight">
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
| Plusieurs<br/>     | integer<br/> | 1<br/>               |
| Unité<br/>     | string<br/>  | microns<br/>         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[PostScript Spécification de format de fichier de description d’imprimante](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




