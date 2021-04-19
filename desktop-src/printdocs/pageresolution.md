---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 88f9a9a3-520e-4044-9ab2-961de03878fa
title: PageResolution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e0fdd16cf3dc0beb6a418b23d8ee6a93e4a6a61
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "106531771"
---
# <a name="pageresolution"></a>PageResolution

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Définit la résolution de la page de sortie d'impression comme valeur qualitative ou comme points par pouce, ou les à la fois.

-   [Informations sur les éléments](#element-information)
-   [Contenu structurel](#structural-content)
-   [Contenu Extensible Markup Language (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informations sur les éléments



| Nom                       |                    |
|----------------------------|--------------------|
| Type d'élément <br/>   | Fonctionnalité<br/> |
| Préfixe d’étendue <br/> | Page<br/>    |
| Notes <br/>          | Aucun<br/>    |



 

## <a name="structural-content"></a>Contenu structurel

La structure XML de cet élément est :

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:integer">_ResolutionXValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:integer">_ResolutionYValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:QualitativeResolution">
      <psf:Value xsi:type="xs:string">_QualitativeResolutionValue_</psf:Value>
    </psf:ScoredProperty> 
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a>Variables de structure

Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.



| Nom                                      | Type de données          | Unité                  | Valeurs prises en charge                                                                                                                                                                      | Résumé                                                                                                                                                          |
|-------------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_OptionName\_<br/>                 | string<br/>  | caractères<br/> | Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.<br/> | Nom de l'option.<br/>                                                                                                                               |
| \_IdentityOptionValue\_<br/>        | string<br/>  | n/a<br/>        | True, False.<br/>                                                                                                                                                               | Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.<br/>                                                                                     |
| \_ResolutionXValue\_<br/>           | entier<br/> | PPP<br/>        | Supérieur à 0.<br/>                                                                                                                                                            | Spécifie le composant x de la résolution par rapport au PageImageableSize en DPI (par rapport à la direction du PageMediaSize et du flux du média).<br/> |
| \_ResolutionYValue\_<br/>           | entier<br/> | PPP<br/>        | Supérieur à 0.<br/>                                                                                                                                                            | Spécifie le composant y de la résolution par rapport au PageImageableSize en DPI (par rapport à la direction du PageMediaSize et du flux du média).<br/> |
| \_QualitativeResolutionValue\_<br/> | string<br/>  | n/a<br/>        | Par défaut, brouillon, élevé, normal, autre.<br/>                                                                                                                                       | Spécifie une étiquette de qualité pour la résolution.<br/>                                                                                                         |



 

## <a name="extensible-markup-language-xml-content"></a>Contenu Extensible Markup Language (XML)

Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms. Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <!-- The horizontal resolution in dots per inch -->
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <!-- The vertical resolution in dots per inch -->
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <!-- Value representing the resolution -->
    <psf:ScoredProperty name="psk:QualitativeResolution">
      <psf:Value xsi:type="xs:string">Other</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




