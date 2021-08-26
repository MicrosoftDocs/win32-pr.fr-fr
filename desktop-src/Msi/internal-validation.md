---
description: Lors de la création d’un package d’installation, vous pouvez utiliser la fonction MsiViewModify ou la méthode View. Modify pour vous assurer que les données que vous entrez sont syntaxiquement correctes.
ms.assetid: c960e9df-dcd6-44d2-8662-40a1dea81f45
title: Validation interne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44184a87f7d8bd28b3603d81bb83ae28ec68471e6c9c849bf9322dc5e968c886
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043299"
---
# <a name="internal-validation"></a>Validation interne

Lors de la création d’un package d’installation, vous pouvez utiliser la fonction [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) ou la méthode View. Modify pour vous assurer que les données que vous entrez sont syntaxiquement correctes. Pour plus d’informations, consultez [**Modify, méthode**](view-modify.md). Au niveau le plus bas, la colonne d’une table de base de données peut stocker des entiers (courts ou longs), des chaînes ou des données binaires. Toutefois, un package d’installation requiert des entiers ou des chaînes spécifiques dans certaines tables. Ces spécifications sont conservées dans le [ \_ tableau de validation](-validation-table.md). Par exemple, la colonne de nom de [fichier](file-table.md) de la table de fichiers est une colonne de chaîne, mais elle stocke spécifiquement un nom de fichier. Par conséquent, non seulement votre entrée doit être une chaîne, mais elle doit également respecter la configuration requise pour nommer les fichiers.

Les différentes valeurs enum de validation utilisées avec la fonction [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) autorisent la validation immédiate à différents niveaux. L' \_ énumération du champ Validate MSIMODIFY \_ peut être utilisée pour valider des champs individuels d’un enregistrement. Elle ne valide pas les clés étrangères. L' \_ enum MSIMODIFY Validate valide une ligne entière et comprend la validation de la clé étrangère. Si vous insérez une nouvelle ligne dans une table, utilisez l’MSIMODIFY \_ valider une \_ nouvelle énumération pour vérifier que vous ajoutez des données valides et que vous utilisez des clés primaires uniques. Une insertion échoue si les clés primaires ne sont pas uniques. Si un appel à **MsiViewModify** avec l’une des énumérations de validation retourne une erreur, vous pouvez effectuer des appels répétés à [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora) pour diagnostiquer le problème. **MsiViewGetError** indique la colonne dans laquelle l’erreur s’est produite, ainsi que la valeur enum pour aider à résoudre le problème. Pour plus d’informations, consultez [**méthode GetError**](view-geterror.md).

Vous pouvez également utiliser la validation interne pour vous assurer que les autres auteurs entrent correctement les données dans votre table personnalisée. Ajoutez chacune des colonnes de votre table personnalisée à la \_ table de validation en utilisant le nom de la table et le nom de la colonne personnalisés comme clé primaire. Fournissez une description ou un objectif de chaque colonne dans la colonne Description du \_ tableau de validation. Entrez les exigences applicables à chaque colonne en utilisant les colonnes Nullable, MinValue, MaxValue, keytable, KeyColumn, Category et set :

-   Si la colonne accepte la valeur null, entrez un « Y ». Si ce n’est pas le cas, entrez un « N ».
-   Si la colonne est une colonne d’entiers et peut contenir une plage d’entiers, entrez cette plage à l’aide des colonnes MinValue et MaxValue.
-   Les colonnes clés étrangères sont identifiées à l’aide des colonnes keytable et KeyColumn.
-   Pour les colonnes de type chaîne, spécifiez une catégorie telle que nom de fichier, GUID ou identificateur. Pour plus d’informations, consultez [types de données des colonnes](column-data-types.md).
-   Si les données ne peuvent concerner qu’un nombre spécifique de valeurs (chaîne ou entier), utilisez la colonne définir pour répertorier les valeurs acceptables.

La liste suivante répertorie les colonnes (en plus de la table, de la colonne et de la description) de la \_ table de validation qui peuvent être renseignées si votre colonne est du type spécifié. (Notez que vous n’avez pas besoin de renseigner toutes les colonnes.)



| Type    | Colonnes                                                          |
|---------|------------------------------------------------------------------|
| Entier | Nullable, MinValue, MaxValue, keytable, KeyColumn, Set           |
| String  | Nullable, keytable, KeyColumn, Category, Set, MinValue, MaxValue |
| Binary  | Nullable, Category (la catégorie doit être « Binary »)                   |



 

Les environnements de création peuvent utiliser MSIMODIFY \_ valider la \_ suppression. Cet enum part du principe que vous souhaitez supprimer la ligne. Aucune validation de champ ou de clé étrangère n’est effectuée. Cette énumération effectue en fait une validation de clé étrangère inverse. Il vérifie la \_ table de validation pour rechercher des références dans les colonnes keytable et KeyColumn de la table à laquelle appartient la ligne « Deleted ». S’il existe des colonnes qui répertorient la table contenant la ligne « supprimée » comme clé étrangère potentielle, elle parcourt cette colonne pour voir si des valeurs font référence à des valeurs dans la ligne « supprimée ». Une erreur de retour signifie que vous rompez l’intégrité relationnelle de la base de données en supprimant la ligne.

 

 



