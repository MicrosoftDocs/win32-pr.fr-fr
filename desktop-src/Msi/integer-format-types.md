---
description: Les types de format entier des données configurables peuvent être utilisés dans des champs de base de données de type texte ou entier. L’attribut msmConfigItemNonNullable est implicite dans ce format de données et n’a pas besoin d’être défini. NULL n’est jamais une valeur valide pour ce type.
ms.assetid: 63fb9c0d-e7f1-4c1d-bb83-2833c5fff18d
title: Types de format d’entier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 184ef6380f25474a9e2ad07be7a4eb6d00706aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757035"
---
# <a name="integer-format-types"></a>Types de format d’entier

Les types de format entier des données configurables peuvent être utilisés dans des champs de base de données de type texte ou entier. L’attribut msmConfigItemNonNullable est implicite dans ce format de données et n’a pas besoin d’être défini. NULL n’est jamais une valeur valide pour ce type.

Le type de format entier suivant existe.

[Type d’entier arbitraire](arbitrary-integer-type.md)

Les éléments configurables du type de format entier sont utilisés dans les colonnes de type texte ou entier et peuvent en général être remplacés par n’importe quel entier positif ou négatif. Toutefois, certains éléments configurables peuvent également avoir des restrictions sémantiques caractéristiques. Par exemple, un élément configurable particulier qui doit être un entier compris entre 0 et 100 a une restriction sémantique supplémentaire. Ces restrictions ne sont pas appliquées par Mergemod.dll et par conséquent, les auteurs de module doivent être préparés à gérer toute chaîne conforme au type de format entier spécifié.

 

 



