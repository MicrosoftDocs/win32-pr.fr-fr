---
description: les chaînes de requête SQL pour les Windows Installer sont limitées aux formats suivants.
ms.assetid: badee528-fa69-43ab-965e-d9e6f2529b99
title: Syntaxe SQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee1b7d1179a8b6035186a9a5e78f46fdc857ac18
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413921"
---
# <a name="sql-syntax"></a>Syntaxe SQL

les chaînes de requête SQL pour les Windows Installer sont limitées aux formats suivants.



| Action                             | Requête                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sélectionner un groupe d’enregistrements          | SÉLECTIONNER \[ distinct \] {Column-List} de {table-List} \[ où {Operation-List} \] \[ classer par {Column-List}\]                                                                                                                                                                                                                                                                                                                                                                                                       |
| Supprimer des enregistrements d’une table        | SUPPRIMER de {table} \[ où {Operation-List}\]                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Modifier des enregistrements existants dans une table | UPDATE {table-List} SET {Column} = {constante} \[ , {Column} = {constant} \] \[ ,... \] \[ OÙ les \] requêtes de mise à jour de {Operation-List} ne fonctionnent que sur les colonnes clés non primaires.<br/>                                                                                                                                                                                                                                                                                                                                      |
| Ajouter des enregistrements à une table             | insertion dans {table} ({column-list}) values ({constant-list}) les \[ \] données binaires temporaires ne peuvent pas être insérées dans une table directement à l’aide des requêtes INSERT INTO ou UPDATE SQL. Pour plus d’informations, consultez [Ajout de données binaires à une table à l’aide de SQL](adding-binary-data-to-a-table-using-sql.md).<br/>                                                                                                                                                                                                       |
| Ajouter une table                        | CREATE TABLE {table} ({Column} {type de colonne}) \[ conservent \] les types de colonne doivent être spécifiés pour chaque colonne lors de l’ajout d’une table. Au moins une colonne de clé primaire doit être spécifiée pour la création d’une nouvelle table. Les substitutions possibles pour {Column type} dans la version ci-dessus sont : CHAR \[ ({Size}) \] \| caractère \[ ({Size}) \] \| LongChar \| short \| int \| entier \| long \| Object \[ not null \] \[ temporaire \] \[ localisable \] \[ , colonne... \] \[ ,... \] Colonne de clé primaire \[ , colonne \] \[ ,... \] .<br/> |
| Supprimer une table                     | SUPPRIMER la TABLE {table}                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Ajout d’une colonne                       | ALTER TABLE {table} ADD {COLUMN} {type de colonne} le type de colonne doit être spécifié lors de l’ajout d’une colonne. Les substitutions possibles pour {Column type} dans la version ci-dessus sont : CHAR \[ ({Size}) \] \| caractère \[ ({Size}) \] \| LongChar \| short \| int \| entier \| long \| Object \[ not null \] \[ temporaire \] \[ localisable \] \[ Hold \] .<br/>                                                                                                                                                                  |
| Conservation et libération de tables temporaires     | ALTER TABLE {table Name} HOLDALTER TABLE {table Name} FREE<br/> L’utilisateur peut utiliser les commandes HOLD et FREE pour contrôler l’étendue de la durée de vie d’une table temporaire ou d’une colonne temporaire. le nombre de suspensions sur une table est incrémenté pour chaque opération de SQL de conservation sur cette table et décrémentée pour chaque SQL opération libre sur la table. Lorsque le dernier nombre de conservations est libéré sur une table, toutes les colonnes temporaires deviennent inaccessibles. Si toutes les colonnes sont temporaires, la table devient inaccessible.<br/>     |



 

pour plus d’informations, consultez [exemples de requêtes de base de données à l’aide d’SQL et de Script](examples-of-database-queries-using-sql-and-script.md).

### <a name="sql-grammar"></a>Grammaire SQL

Les paramètres facultatifs sont indiqués entre crochets \[ \] . Lorsque plusieurs choix sont répertoriés, les paramètres facultatifs sont séparés par une barre verticale.

Une {constant} est soit une chaîne, soit un entier. Une chaîne doit être placée entre guillemets simples « example ». Une {constant-List} est une liste délimitée par des virgules d’une ou de plusieurs constantes.

L’option LOCALIZable définit un attribut de colonne qui indique que la colonne doit être localisée.

Une {Column} est une référence en colonnes à une valeur dans un champ d’une table.

Un {Marker} est une référence de paramètre à une valeur fournie par un enregistrement envoyé avec la requête. elle est représentée dans l’instruction SQL par un point d’interrogation. Pour plus d’informations sur l’utilisation des paramètres, consultez la fonction [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) ou la méthode [**Execute**](view-execute.md) .

la syntaxe d’SQL Windows Installer ne prend pas en charge l’échappement des guillemets simples (valeur ASCII 39) dans un littéral de chaîne. Toutefois, vous pouvez extraire ou créer l’enregistrement, définir le champ avec la propriété [**StringData**](record-stringdata.md) ou [**IntegerData**](record-integerdata.md) , puis appeler la méthode [**Modify**](view-modify.md) . Vous pouvez également créer un enregistrement et utiliser les marqueurs de paramètres ( ?) décrits dans la méthode [**Execute**](view-execute.md) . Vous pouvez également effectuer cette opération à l’aide des fonctions de base de données [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute), [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger)et [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa).

Une clause WHERE {Operation-List} est facultative et est un regroupement d’opérations à utiliser pour filtrer la sélection. Les opérations doivent être de l’un des types suivants :

-   {Column} = {colonne}
-   {column} = \|  <>  \|  >  \|  <  \|  >=  \| <= {constante}
-   {column} = \|  <>  \|  >  \|  <  \|  >=  \| <= {marqueur}
-   {Column} est null
-   {Column} n’est pas null

Pour les valeurs de chaîne, seules les opérations = ou <> sont possibles. Les comparaisons de valeurs d’objet sont limitées à IS NULL et IS NOT NULL.

Les opérations individuelles peuvent être regroupées par opérateur AND ou or. Le classement peut être imposé en utilisant des parenthèses ().

La clause ORDER BY est facultative et provoque un délai initial lors du tri. Le classement par chaîne regroupera des chaînes identiques, mais il n’utilisera pas l’ordre alphabétique des chaînes.

La clause DISTINCT est facultative et ne répète pas les enregistrements identiques dans le jeu de résultats retourné.

{Table-List} est une liste délimitée par des virgules d’un ou plusieurs noms de tables référencés sous la forme {table} dans la jointure.

{Column-List} est une liste délimitée par des virgules d’une ou plusieurs colonnes de table référencées comme {Column} sélectionnées. Les colonnes ambiguës peuvent être plus qualifiées comme {TableName. Column}. Un astérisque peut être utilisé comme liste de colonnes dans une requête SELECT pour représenter toutes les colonnes des tables référencées. Lorsque vous référencez des champs par position de colonne, sélectionnez les colonnes par leur nom au lieu d’utiliser l’astérisque. Un astérisque ne peut pas être utilisé comme liste de colonnes dans une requête INSERT INTO.

pour échapper les noms de table et de colonne qui sont en conflit avec les mots clés de SQL, mettez le nom entre deux points d’accent graves \` \` (valeur ASCII 96). Si un nom de colonne doit être placé dans une séquence d’échappement et qu’il est qualifié de {TableName. Column}, la table et la colonne doivent être placées dans une séquence d’échappement individuellement comme { \` TableName \` . \` colonne \` }. Il est recommandé que tous les noms de table et de colonne soient échappés de cette manière afin d’éviter les conflits avec les mots réservés et d’obtenir des performances significatives.

Les noms de table sont limités à 31 caractères. Pour plus d’informations, consultez [noms de tables](table-names.md). Les noms de table et de colonne respectent la casse. les mots clés SQL ne respectent pas la casse.

le nombre maximal d’expressions dans une clause where d’une requête SQL est limité à 32.

Seules les jointures internes sont prises en charge et sont spécifiées par une comparaison des colonnes de différentes tables. Les jointures circulaires ne sont pas prises en charge. une jointure circulaire est une requête de SQL qui lie trois tables ou plus dans un circuit. Par exemple, voici une jointure circulaire :

``` syntax
WHERE Table1.Field1=Table2.Field1 AND Table2.Field2=Table3.Field1 AND Table3.Field2=Table1.Field2.
```

Les colonnes qui font partie de la ou des clés primaires d’une table doivent être définies en premier par ordre de priorité, suivies de toutes les colonnes clés non primaires. Les colonnes persistantes doivent être définies avant les colonnes temporaires. La séquence de tri d’une colonne de texte n’est pas définie. Toutefois, les valeurs de texte identiques sont toujours regroupées.

Notez que lors de l’ajout ou de la création d’une colonne, vous devez spécifier le type de colonne.

Les tables ne peuvent pas contenir plus d’une colonne de type « Object ».

la taille maximale qui peut être spécifiée explicitement pour une colonne de type chaîne dans une requête SQL est 255. Une colonne de type chaîne de longueur infinie est représentée comme ayant la taille 0. Pour plus d’informations, consultez [format de définition de colonne](column-definition-format.md).

pour exécuter une instruction SQL, vous devez créer une vue. Toutefois, une vue qui ne crée pas de jeu de résultats, comme CREATE TABLE ou INSERT INTO, ne peut pas être utilisée avec [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) ou la méthode [**Modify**](view-modify.md) pour mettre à jour des tables via la vue.

Notez que vous ne pouvez pas extraire un enregistrement contenant des données binaires d’une base de données, puis utiliser cet enregistrement pour insérer les données dans une base de données complètement différente. Pour déplacer des données binaires d’une base de données vers une autre, exportez les données vers un fichier, puis importez-les dans la nouvelle base de données via une requête et la fonction [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) . Cela garantit que chaque base de données possède sa propre copie des données binaires.

 

 




