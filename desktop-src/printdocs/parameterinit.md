---
description: En savoir plus sur l’élément ParameterInit, qui définit une valeur pour une instance d’un élément ParameterDef.
ms.assetid: d5419c40-43e9-49ff-a378-9aeb0757e400
title: ParameterInit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e0e0cadbf26d6ff516ab0ace90165e11420a9b7
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118974"
---
# <a name="parameterinit"></a>ParameterInit

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Définit une valeur pour une instance d’un élément ParameterDef. Un élément ParameterInit est la cible de la référence effectuée par un élément ParameterRef.

## <a name="element-tag"></a>Balise d’élément

<ParameterInit>

## <a name="xml-attributes"></a>Attributs XML

Le tableau suivant répertorie les attributs XML qui peuvent être liés à cet élément.



| Attribut XML   | Détails                                                                                                                               |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Contient l’attribut Name de l’élément ParameterDef qui doit être initialisé dans le contexte du document actif.<br/> |



 

Pour plus d’informations, consultez la section [attributs XML](xml-attributes.md) .

## <a name="element-information"></a>Informations sur les éléments

Le tableau suivant répertorie les éléments qui peuvent être des parents de cet élément, les éléments qui peuvent être des enfants de cet élément, ainsi que toutes les restrictions applicables à l’élément lui-même.



| Category                   | Nom ou restriction                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------------|
| Éléments parents<br/> | PrintTicket (racine PrintTicket)<br/>                                                         |
| Éléments enfants<br/>  | Valeur (un)<br/>                                                                            |
| Élément This<br/>    | Aucune donnée de caractères n’est autorisée.<br/> Les frères enfants en double ne sont pas autorisés.<br/> |



 

## <a name="configuration-dependencies"></a>Dépendances de configuration

None

## <a name="example"></a>Exemple

L’exemple suivant initialise un paramètre avec la valeur 1. L’exemple de [ParameterDef](parameterdef.md) montre comment définir tous les éléments de propriété requis pour ce paramètre.

``` syntax
<psf:ParameterInit name="psk:PageCopyCount">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
</psf:ParameterInit>
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




