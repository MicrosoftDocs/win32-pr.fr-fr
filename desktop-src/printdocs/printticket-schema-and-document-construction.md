---
description: En savoir plus sur le format PrintTicket, qui exprime les informations de configuration à l’aide de l’infrastructure de schéma d’impression XML.
ms.assetid: 573c2c82-aeb9-4ef2-8a1b-40b4db6ac6e4
title: Schéma PrintTicket et construction de document
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5998aeb534bbbeb16681a4136cf33425a7eefad7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521404"
---
# <a name="printticket-schema-and-document-construction"></a>Schéma PrintTicket et construction de document

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

La méthode actuelle de spécification des informations de configuration d’appareil à l’aide d’une structure DEVMODE souffre de plusieurs limitations. Premièrement, la structure DEVMODE est une structure binaire, qui peut entraîner des problèmes de versions différentes. Deuxièmement, elle est divisée en une partie publique non extensible et une partie privée est accessible uniquement par les pilotes, et uniquement par le pilote spécifique qui l’a créée. Le format PrintTicket exprime les informations de configuration à l’aide de l’infrastructure de schéma d’impression XML, ce qui élimine ces lacunes de la structure DEVMODE.

Le schéma PrintTicket résout chacun des deux problèmes que vous venez de mentionner. Tout d’abord, le schéma PrintTicket est un fichier texte basé sur XML, ce qui signifie que les problèmes d’extensibilité et de contrôle de version sont éliminés. Deuxièmement, les informations de configuration sont disponibles pour tous les clients, ce qui signifie que n’importe quel client ou fournisseur peut stocker et récupérer toutes les informations contenues dans un PrintTicket. Les options sont décrites à l’aide de la même technique que celle utilisée par l’infrastructure du schéma d’impression et le document PrintCapabilities dérivé. Pour cette raison, le PrintTicket fournit tous les avantages de portabilité potentiels du modèle de définition d’option à réaliser. Pour plus d’informations, consultez [structure du schéma d’impression](print-schema-framework.md) . Le public visé pour cette section comprend les groupes suivants :

-   Implémenteurs d’une interface de fournisseur PrintTicket/PrintCapabilities

-   Consommateurs du PrintTicket

-   Clients d’une interface de fournisseur PrintTicket/PrintCapabilities

Les membres de la première catégorie de la liste précédente sont appelés fournisseurs PrintTicket dans le reste de cette section. Les membres des deux dernières catégories sont appelés consommateurs PrintTicket.

## <a name="relationship-to-print-schema-and-printcapabilities-schema"></a>Relation avec le schéma d’impression et le schéma PrintCapabilities

Les schémas PrintTicket et PrintCapabilities sont des parties spécialisées du schéma d’impression. Les principales différences structurelles entre ces sous-ensembles du schéma d’impression sont que le schéma PrintTicket contient des instances Property et ParameterInit qui ne sont pas contenues dans le schéma PrintCapabilities, tandis que le schéma PrintCapabilities inclut des instances Property et ParameterDef qui ne sont pas contenues dans le schéma PrintTicket. À l’exception de ces différences, les schémas PrintCapabilities et PrintTicket sont généralement mis en miroir l’un de l’autre dans le contenu, en partageant les fonctionnalités, les options, les ScoredProperty et les instances de valeur. Tout contenu partagé doit être tenu à jour. Par exemple, si une modification est apportée à la fonctionnalité MediaSize dans le schéma PrintCapabilities, la même modification doit être apportée dans le schéma PrintTicket.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



