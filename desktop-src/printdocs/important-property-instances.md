---
description: Pour qu’un client crée un PrintTicket, le document PrintCapabilities doit fournir les propriétés des instances de fonctionnalité et des instances d’option dans la fonctionnalité.
ms.assetid: 8169b74f-13e0-4f6b-81e2-1824d932ee50
title: Instances de propriété importantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4691b73b1206ee092c171b213a3815925b7f53c6
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409122"
---
# <a name="important-property-instances"></a>Instances de propriété importantes

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Pour qu’un client PrintCapabilities puisse construire un PrintTicket raisonnable, le document PrintCapabilities doit fournir certaines propriétés des instances de fonctionnalité ainsi que des instances d’option dans la fonctionnalité. Un module d’interface utilisateur générique requiert ces informations pour construire une interface utilisateur. Cela nécessite à son tour que les mots clés du schéma d’impression définissent quelques instances de propriété qui s’affichent en tant qu’enfants des éléments Feature et option.

Les éléments de fonctionnalité peuvent contenir la propriété suivante.



| Propriété                  | Valeurs                                 | Objectif                                                                                                                                                                                                                                                                                                       |
|---------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SelectionType <br/> | PickOne<br/> PickMany<br/> | Spécifie le nombre d’options qui peuvent être sélectionnées pour cette fonctionnalité à un moment donné, soit un (PickOne), soit plusieurs (PickMany). Le client peut utiliser ces informations pour construire un PrintTicket. Ces informations affectent le comportement de l’interface utilisateur, ainsi que la validation PrintTicket par le fournisseur.<br/> |



 

Les éléments option peuvent contenir la propriété suivante.



| Propriété                   | Valeurs                           | Objectif                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IdentityOption <br/> | True<br/> False<br/> | La sélection de la propriété IdentityOption est interprétée comme signifiant « désactiver cette fonctionnalité ». Une fonctionnalité qui contient une propriété SelectionType dont la valeur est PickMany doit également contenir une option qui a une propriété IdentityOption. Le code d’interface utilisateur (ou la construction du client d’un PrintTicket) doit désélectionner une autre option si la propriété IdentityOption est sélectionnée.<br/> |



 

Les éléments Feature, option et ParameterDef peuvent contenir la propriété suivante.



| Propriété              | Valeurs                          | Objectif                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayUI <br/> | Afficher<br/> Masquer<br/> | Spécifie si l’élément parent doit être affiché dans l’interface utilisateur. Afficher indique que l’élément doit être affiché dans l’interface utilisateur. Masquer indique que l’élément ne doit pas être affiché dans l’interface utilisateur. Si cette propriété n’est pas définie pour un élément, l’interprétation par défaut est Show, ce qui signifie que l’élément est affiché.<br/> |



 

Les éléments Feature, option et ParameterDef peuvent contenir la propriété suivante.



| Propriété                | Valeur             | Objectif                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName <br/> | String<br/> | Spécifie la chaîne d’affichage de l’élément parent, en remplaçant le nom d’affichage par défaut. Peut être utilisé par les fournisseurs PrintCapabilities pour présenter un nom complet localisé et convivial. La valeur de nom complet par défaut est l’attribut de nom de l’élément parent. <br/> Dans le cas d’éléments option, si l’attribut name n’est pas fourni, la propriété DisplayName doit être présente.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




