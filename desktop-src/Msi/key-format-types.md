---
description: Les types de format de clé des données configurables peuvent être utilisés dans les champs de texte pour fournir une clé dans une table de base de données.
ms.assetid: 9f3ce218-1243-4eba-9866-113200fefa30
title: Types de format de clé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a22c4149ec89bd9a1745c28fe17cdafcbcfeaee827dcb35bd8c6badbf2acfb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692489"
---
# <a name="key-format-types"></a>Types de format de clé

Les types de format de clé des données configurables peuvent être utilisés dans les champs de texte pour fournir une clé dans une table de base de données. L’attribut msmConfigItemNonNullable est implicite dans ce format de données et n’a pas besoin d’être défini. NULL n’est jamais une valeur valide pour ce type. Les réponses à tous les éléments de format de clé doivent être au [format spécial CMSM](cmsm-special-format.md).

Les types de format de clé suivants existent :

[Type de répertoire](directory-type.md)

[Type de fichier](file-type.md)

[Type de propriété](property-type.md)

[Type de dialogue](dialog-type.md)

[Type binaire](binary-type.md)

[Type d’icône](icon-type.md)

Les éléments configurables du type de format de clé sont utilisés dans les colonnes de texte pour fournir une clé de base de données. en général, il est possible de remplacer par n’importe quelle chaîne de texte. Les types individuels peuvent avoir des restrictions syntaxiques supplémentaires, mais ces restrictions ne sont pas appliquées par Mergemod.dll. Certains éléments configurables peuvent également présenter des restrictions sémantiques caractéristiques. Par exemple, un élément configurable spécifique peut être une clé de la [table binaire](binary-table.md) vers une ligne contenant une image bitmap. Ces restrictions ne sont pas appliquées par Mergemod.dll et par conséquent, les auteurs de module doivent être préparés à gérer toute chaîne conforme au type de format de clé spécifié. Sauf spécification contraire de la signification sémantique ou des attributs, NULL est une réponse valide.

 

 



