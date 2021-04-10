---
description: Les sections suivantes décrivent l’utilisation des propriétés de programme d’installation intégrées et des propriétés supplémentaires définies par l’auteur du package.
ms.assetid: 5a2f1cd4-2bbd-414a-a814-8b9fdab434b4
title: Utilisation de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edab44953f6ccd210d5baa3c446363a1131dc745
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113243"
---
# <a name="using-properties"></a>Utilisation de propriétés

Les sections suivantes décrivent l’utilisation des propriétés de programme d’installation intégrées et des propriétés supplémentaires définies par l’auteur du package. Les propriétés peuvent être des propriétés [publiques](public-properties.md) ou [privées](private-properties.md). Chaque propriété qui doit être définie lors de l’initialisation du programme d’installation doit avoir son nom et sa valeur initiale listés dans la [table des propriétés](property-table.md). Les propriétés ayant une valeur NULL ne sont pas répertoriées dans la table des propriétés. Vous pouvez récupérer ou définir des propriétés à partir de programmes et d’actions personnalisées et définir des propriétés publiques à partir de la ligne de commande. Le processus d’installation peut être modifié à l’aide de propriétés dans des instructions conditionnelles.

[Restrictions sur les noms de propriété](restrictions-on-property-names.md)

[Initialisation des valeurs de propriété](initialization-of-property-values.md)

[Obtention et définition des propriétés](getting-and-setting-properties.md)

[Utilisation des propriétés dans les instructions conditionnelles](using-properties-in-conditional-statements.md)

[Utilisation d’une propriété de répertoire dans un chemin d’accès](using-a-directory-property-in-a-path.md)

> [!Note]  
> N’utilisez pas de propriétés pour les mots de passe ou d’autres informations qui doivent rester sécurisées. Le programme d’installation peut écrire la valeur d’une propriété créée dans la table de propriétés ou créée au moment de l’exécution dans un journal ou dans le registre système.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des propriétés](about-properties.md)
</dt> <dt>

[Référence de propriété](property-reference.md)
</dt> </dl>

 

 



