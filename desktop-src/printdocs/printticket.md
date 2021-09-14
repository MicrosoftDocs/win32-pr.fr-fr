---
description: Recherche des informations sur l’élément PrintTicket. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: fe6bd921-cbf3-4cca-afae-82d3822206ba
title: PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a38638083f6a6aabd0290fa3466a30fd50f7375
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196704"
---
# <a name="printticket"></a>PrintTicket

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un élément PrintTicket est l’élément racine du document PrintTicket. Un élément PrintTicket contient toutes les informations de mise en forme du travail requises pour générer un travail.

## <a name="element-tag"></a>Balise d’élément

&lt;PrintTicket&gt;

## <a name="xml-attributes"></a>Attributs XML

Le tableau suivant répertorie les attributs XML qui peuvent être liés à cet élément.



| Attribut XML      | Détails                                                                                                                                                                                   |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| version<br/> | Spécifie la version du schéma qui définit les types d’éléments et leur structure, un littéral de type entier. La version actuelle du schéma est « 1 ». Cet attribut est obligatoire. <br/> |



 

Pour plus d’informations, consultez la section [attributs XML](xml-attributes.md) .

## <a name="element-information"></a>Informations sur les éléments

Le tableau suivant répertorie les éléments qui peuvent être des parents de cet élément, les éléments qui peuvent être des enfants de cet élément, ainsi que toutes les restrictions applicables à l’élément lui-même.



| Category                   | Détails                                                                                                            |
|----------------------------|--------------------------------------------------------------------------------------------------------------------|
| Éléments parents<br/> | Racine du document uniquement.<br/>                                                                                     |
| Éléments enfants<br/>  | *Fonctionnalité* (zéro ou plus)<br/> *ParameterInit* (zéro ou plus)<br/> *Property* (zéro, un ou plusieurs)<br/> |
| Élément This<br/>    | Aucune donnée de caractères n’est autorisée.<br/> Les frères enfants en double ne sont pas autorisés.<br/>                  |



 

## <a name="configuration-dependencies"></a>Dépendances de configuration

Les dépendances de configuration s’appliquent uniquement aux éléments d’un document PrintCapabilities.

## <a name="example"></a>Exemple

Consultez l' [exemple PrintTicket](printticket-example.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




