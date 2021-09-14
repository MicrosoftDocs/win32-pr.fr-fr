---
description: Les types de format de texte des données configurables peuvent être des chaînes de texte de n’importe quelle longueur. Les valeurs NULL incorporées ne sont pas autorisées.
ms.assetid: 71b89f87-43ba-41cd-a969-765d45da4ba4
title: Types de format de texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a8f05a0804569667a74c52392d322f3fed2818
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119649"
---
# <a name="text-format-types"></a>Types de format de texte

Les types de format de texte des données configurables peuvent être des chaînes de texte de n’importe quelle longueur. Les valeurs NULL incorporées ne sont pas autorisées.

Les types de format de texte suivants existent :

[Texte arbitraire](arbitrary-text-type.md)

[RTF](rtf-type.md)

[Correct](formatted-type.md)

[Enum](enum-type.md)

[Type d’identificateur](identifier-type.md)

Les éléments configurables du type de format texte sont utilisés dans les champs de base de données non binaires. en général, ils peuvent être remplacés par toute chaîne de n’importe quelle longueur. Toutefois, certains éléments configurables ont également des restrictions sémantiques. Par exemple, un élément configurable qui doit être une clé étrangère dans une table spécifique a des restrictions sémantiques supplémentaires. Ces restrictions sémantiques ne sont pas appliquées par Mergemod.dll et par conséquent, les auteurs de module doivent être préparés à gérer toute chaîne conforme au type de format texte spécifié.

 

 



