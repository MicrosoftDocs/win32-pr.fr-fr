---
description: Les types de format entier des données configurables peuvent être utilisés dans des champs de base de données de type texte ou entier. L’attribut msmConfigItemNonNullable est implicite dans ce format de données et n’a pas besoin d’être défini. NULL n’est jamais une valeur valide pour ce type.
ms.assetid: 63fb9c0d-e7f1-4c1d-bb83-2833c5fff18d
title: Types de format d’entier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cf5d4ad0d7ef9ba8adb1ddb919e284dbd2a10b2eafc7c43f72d6d0ee777f743
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117805627"
---
# <a name="integer-format-types"></a>Types de format d’entier

Les types de format entier des données configurables peuvent être utilisés dans des champs de base de données de type texte ou entier. L’attribut msmConfigItemNonNullable est implicite dans ce format de données et n’a pas besoin d’être défini. NULL n’est jamais une valeur valide pour ce type.

Le type de format entier suivant existe.

[Type d’entier arbitraire](arbitrary-integer-type.md)

Les éléments configurables du type de format entier sont utilisés dans les colonnes de type texte ou entier et peuvent en général être remplacés par n’importe quel entier positif ou négatif. Toutefois, certains éléments configurables peuvent également avoir des restrictions sémantiques caractéristiques. Par exemple, un élément configurable particulier qui doit être un entier compris entre 0 et 100 a une restriction sémantique supplémentaire. Ces restrictions ne sont pas appliquées par Mergemod.dll et par conséquent, les auteurs de module doivent être préparés à gérer toute chaîne conforme au type de format entier spécifié.

 

 



