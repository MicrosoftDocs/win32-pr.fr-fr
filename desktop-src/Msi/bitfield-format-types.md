---
description: Les types de format de champ binaire des données configurables peuvent être utilisés dans des champs de base de données Integer.
ms.assetid: 3b05392e-4276-4970-ae43-9ee00bc9f476
title: Types de format de champ de format binaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b443f7ee363d1a2b48eb580623018264df8d50be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524175"
---
# <a name="bitfield-format-types"></a>Types de format de champ de format binaire

Les types de format de champ binaire des données configurables peuvent être utilisés dans des champs de base de données Integer. L’utilisateur doit choisir une valeur dans un sous-ensemble spécifié. C’est par convention uniquement et n’est pas appliqué par Mergemod.dll. L’attribut msmConfigItemNonNullable est implicite dans ce format de données et n’a pas besoin d’être défini. NULL n’est jamais une valeur valide pour ce type.

Le type de format de champ de format binaire suivant existe.

[Type de champ de type binaire arbitraire](arbitrary-bitfield-type.md)

Les éléments configurables du type de format de champ de binaire sont utilisés dans les colonnes d’entiers et peuvent en général être remplacés par n’importe quel entier. L’utilisateur doit choisir une valeur dans un sous-ensemble spécifié. Toutefois, il s’agit uniquement d’une convention, qui n’est pas appliquée par Mergemod.dll. L’auteur doit préparer le module pour qu’il gère n’importe quelle valeur.

 

 



