---
description: ICE32 valide que les clés et les clés étrangères du fichier. msi sont des mêmes types de définition de taille et de colonne.
ms.assetid: cc488ec5-e17a-4829-9763-38ba3c33bfde
title: ICE32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d6ff9e4de592ac073050b357aff0c63d984f0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536718"
---
# <a name="ice32"></a>ICE32

ICE32 valide que les clés et les clés étrangères du fichier. msi sont des mêmes types de définition de taille et de colonne. Cette action personnalisée ICE effectue la comparaison à l’aide de la [ \_ table de validation](-validation-table.md) et à l’aide des types de définition retournés par [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo). Pour plus d’informations, consultez [format de définition de colonne](column-definition-format.md).

## <a name="result"></a>Résultats

ICE32 publie des erreurs si le fichier. msi contient des clés étrangères aux clés d’un type de données de longueur de colonne ou de colonne différent.

## <a name="example"></a>Exemple

ICE32 publie deux erreurs pour l’exemple ci-dessous :

-   Une clé étrangère et une clé définie ont une taille différente.
-   Une clé étrangère et une clé définies diffèrent dans leur type de définition.

[ \_ Table de validation](-validation-table.md) (partielle)



| Table de charge de travail | Colonne  | Keytable | KeyColumn |
|-------|---------|----------|-----------|
| Fichier  | Version | Fichier     | 1         |
| Ailes  | Colonne8 | Ailes     | 1         |



 

Définitions de colonne (partielles)



| Table de charge de travail | Colonne  | Type | Taille |
|-------|---------|------|------|
| Fichier  | Fichier    | s    | 72   |
| Fichier  | Version | S    | 32   |
| Ailes  | Column1 | i    | 2    |
| Ailes  | Colonne8 | S    | 32   |



 

La colonne de version de la table de fichiers peut être une clé étrangère vers un autre fichier de la table de fichiers. Cela se produit avec les fichiers d’accompagnement. Toutefois, la colonne version autorise uniquement une longueur de chaîne de 32, alors que la colonne fichier autorise une longueur de chaîne de 72. Pour corriger cette erreur, modifiez les longueurs de chaîne pour qu’elles correspondent.

Une clé étrangère et une clé définies diffèrent dans leurs types de définition. Le Column8 de la table de rabats est listé comme clé étrangère à Colonne1. Column8 est une colonne de chaîne et Colonne1 est une colonne de type entier. Les paires clé étrangère et clé doivent être définies de sorte que leurs types de données correspondent.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



