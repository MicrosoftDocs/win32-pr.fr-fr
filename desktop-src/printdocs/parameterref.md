---
description: Découvrez l’élément ParameterRef, qui définit une référence à un élément ParameterInit et comment il fonctionne avec ScoredProperty.
ms.assetid: 35e1ccc2-ffc1-47a6-aba8-5a5cb442e8ae
title: ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb3655ab62c8d11b4e9ee777d01a8e6bf5d63a1f
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884119"
---
# <a name="parameterref"></a>ParameterRef

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un élément ParameterRef définit une référence à un élément ParameterInit. Un élément ScoredProperty qui contient un élément ParameterRef n’a pas d’élément de valeur explicitement défini. Au lieu de cela, l’élément ScoredProperty reçoit sa valeur de l’élément ParameterInit référencé par un élément ParameterRef.

## <a name="element-tag"></a>Balise d’élément

&lt;ParameterRef&gt;

## <a name="xml-attributes"></a>Attributs XML

Le tableau suivant répertorie les attributs XML qui peuvent être liés à cet élément.



| Attribut XML   | Détails                                                                                                                        |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Contient l’attribut Name de l’élément ParameterDef référencé dans le contexte du document actif.<br/> |



 

Pour plus d’informations, consultez la section [attributs XML](xml-attributes.md) .

## <a name="element-information"></a>Informations sur les éléments

Le tableau suivant répertorie les éléments qui peuvent être des parents de cet élément, les éléments qui peuvent être des enfants de cet élément, ainsi que toutes les restrictions applicables à l’élément lui-même.



| Catégorie                   | Détails                                                                                           |
|----------------------------|---------------------------------------------------------------------------------------------------|
| Éléments parents<br/> | ScoredProperty <br/>                                                                        |
| Éléments enfants<br/>  | Aucun autorisé.<br/>                                                                        |
| Élément This<br/>    | Aucune donnée de caractères n’est autorisée.<br/> Les frères enfants en double ne sont pas autorisés.<br/> |



 

## <a name="configuration-dependencies"></a>Dépendances de configuration

Les éléments ParameterRef ne peuvent pas avoir de dépendances de configuration.

## <a name="example"></a>Exemple

L’exemple suivant illustre l’utilisation d’éléments ParameterRef pour permettre aux utilisateurs d’entrer des paramètres de taille de média personnalisés.

``` syntax
<psf:Option name="psk:CustomMediaSize" constrained="psk:None">
  <psf:ScoredProperty name="psk:MediaSizeWidth">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
  </psf:ScoredProperty>
  <psf:ScoredProperty name="psk:MediaSizeHeight">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
  </psf:ScoredProperty>
  <psf:Property name="psk:DisplayName">
    <psf:Value xsi:type="xs:string">Fabrikam User Custom</psf:Value>
  </psf:Property>
</psf:Option>
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




