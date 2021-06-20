---
description: En savoir plus sur l’élément PrintCapabilities, qui représente la racine du document PrintCapabilities.
ms.assetid: f503b62f-02e1-4621-8799-a8b6ad12f489
title: PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2158fd651849df2e4ea24c640065f1041569741a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407022"
---
# <a name="printcapabilities"></a>PrintCapabilities

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un élément PrintCapabilities représente la racine du document PrintCapabilities. Le document PrintCapabilities contient toutes les informations nécessaires pour décrire les attributs des appareils pris en charge, en fonction d’une configuration d’appareil particulière.

## <a name="element-tag"></a>Balise d’élément

<PrintCapabilities>

## <a name="xml-attributes"></a>Attributs XML

Le tableau suivant répertorie les attributs XML qui peuvent être liés à cet élément.



| Attribut XML      | Détails                                                                                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| version<br/> | Spécifie la version du schéma qui définit les types d’éléments et leur structure. L’attribut version est de type entier. La version actuelle du schéma est « 1 ». Cet attribut est obligatoire. <br/> |



 

Pour plus d’informations, consultez la section [attributs XML](xml-attributes.md) .

## <a name="element-information"></a>Informations sur les éléments

Le tableau suivant répertorie les éléments qui peuvent être des parents de cet élément, les éléments qui peuvent être des enfants de cet élément, ainsi que toutes les restrictions applicables à l’élément lui-même.



| Category                   | Détails                                                                                                           |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| Éléments parents<br/> | Racine du document uniquement.<br/>                                                                                    |
| Éléments enfants<br/>  | *Fonctionnalité* (zéro ou plus)<br/> *ParameterDef* (zéro ou plus)<br/> *Property* (zéro, un ou plusieurs)<br/> |
| Élément This<br/>    | Aucune donnée de caractères n’est autorisée.<br/> Les frères enfants en double ne sont pas autorisés.<br/>                 |



 

## <a name="configuration-dependencies"></a>Dépendances de configuration

L’élément racine ne peut pas avoir de dépendances de configuration.

## <a name="example"></a>Exemple

Consultez l' [exemple de document PrintCapabilities](printcapabilities-document-example.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




