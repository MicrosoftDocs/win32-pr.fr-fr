---
description: Vous trouverez un exemple d’utilisation de requêtes de base de données basées sur des scripts dans le kit de développement logiciel (SDK) Windows Installer, car l’utilitaire WiRunSQL.vbs.
ms.assetid: aa38dbe5-411d-432e-b3fe-09994fc59c75
title: Exemples de requêtes de base de données utilisant SQL et script
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd839151b40ddd5e9a265c6c370c27a4a9fd125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755628"
---
# <a name="examples-of-database-queries-using-sql-and-script"></a>Exemples de requêtes de base de données utilisant SQL et script

Vous trouverez un exemple d’utilisation de requêtes de base de données basées sur des scripts dans le [Kit de développement logiciel](platform-sdk-components-for-windows-installer-developers.md) (SDK) Windows Installer en tant qu' WiRunSQL.vbs de l’utilitaire. Cet utilitaire gère les requêtes de base de données à l’aide de la version Windows Installer de SQL décrite dans la section [syntaxe SQL](sql-syntax.md).

**Supprimer un enregistrement d’une table**

La ligne de commande suivante supprime l’enregistrement dont la clé primaire est rouge de la table des [fonctionnalités](feature-table.md) de la base de données Test.msi.

**Cscript WiRunSQL.vbs Test.msi fonctionnalité «supprimer de la \` fonctionnalité \` where \` \` . \` Feature \` = 'Red' "**

**Ajouter une table à une base de données**

La ligne de commande suivante ajoute la table de [répertoires](directory-table.md) à la base de données Test.msi.

**CScript WiRunSQL.vbs Test.msi "CREATE TABLE \` Directory \` ( \` répertoire \` char (72) not null, \` répertoire \_ parent \` char (72), \` DefaultDir \` char (255) not null répertoire de clé primaire localisable \` \` )"**

**Supprimer une table d’une base de données**

La ligne de commande suivante supprime la table des [fonctionnalités](feature-table.md) de la base de données Test.msi.

**Cscript WiRunSQL.vbs Test.msi « supprimer la \` fonctionnalité de table \` »**

**Ajouter une nouvelle colonne à une table**

La ligne de commande suivante ajoute la colonne test à la table [CustomAction](customaction-table.md) de la base de données Test.msi.

**CScript WiRunSQL.vbs Test.msi « ALTER TABLE \` CustomAction \` Add \` test \` Integer »**

**Insérer un nouvel enregistrement dans une table**

La ligne de commande suivante insère un nouvel enregistrement dans la table des [fonctionnalités](feature-table.md) de la base de données Test.msi.

**Cscript WiRunSQL.vbs Test.msi fonctionnalité d’insertion \` \` ( \` fonctionnalité) \` . \` Fonctionnalité \` \` \` . \` Fonction \_ parente \` , \` fonctionnalité \` . \` Titre \` , \` fonctionnalité \` . \` Description \` , \` fonctionnalité \` . \` Affichage \` , \` fonctionnalité \` . \` Niveau \` , \` fonctionnalité \` . \` Répertoire \_ \` , \` fonctionnalité \` . \` Valeurs d’attribut \` ) (« tennis », « sport », « tennis », « tournoi », 25, 3, « SPORTDIR », 2)»**

Cela insère l’enregistrement suivant dans la table des [fonctionnalités](feature-table.md) de Test.msi.

[Fonctionnalité](feature-table.md) Tableau



| Fonctionnalité | Parent de la fonctionnalité \_ | Intitulé  | Description | Afficher | Level | Répertoire\_ | Attributs |
|---------|-----------------|--------|-------------|---------|-------|-------------|------------|
| Tennis  | Sport           | Tennis | Oppos  | 25      | 3     | SPORTDIR    | 2          |



 

Notez que les données binaires ne peuvent pas être insérées directement dans une table à l’aide de l’instruction INSERT INTO ou de la mise à jour de requêtes SQL. Pour plus d’informations, consultez [Ajout de données binaires à une table à l’aide de SQL](adding-binary-data-to-a-table-using-sql.md).

**Modifier un enregistrement existant dans une table**

La ligne de commande suivante remplace la valeur existante dans le champ titre par « performances ». L’enregistrement mis à jour comporte « arts » comme clé primaire et figure dans la table des fonctionnalités de la base de données Test.msi.

**Cscript WiRunSQL.vbs Test.msi «mettre à jour la \` fonctionnalité de jeu de fonctionnalités \` \` \` . \` Title \` = « performance » où se trouve la \` fonctionnalité \` . \` Fonctionnalité \` = « Arts »**

**Sélectionner un groupe d’enregistrements**

La ligne de commande suivante sélectionne le nom et le type de tous les contrôles qui appartiennent au ErrorDialog dans la base de données Test.msi.

**CScript WiRunSQL.vbs Test.msi « sélectionner \` le contrôle \` , \` tapez \` à partir du \` contrôle \` où boîte de \` dialogue \_ \` = «ErrorDialog »»**

**Conserver une table en mémoire**

La ligne de commande suivante verrouille la table des [composants](component-table.md) de la base de données Test.msi en mémoire.

**CScript WiRunSQL.vbs Test.msi « ALTER TABLE \` Component \` Hold »**

**Libérer une table en mémoire**

La ligne de commande suivante libère la table des [composants](component-table.md) de la base de données Test.msi à partir de la mémoire.

**CScript WiRunSQL.vbs Test.msi « ALTER TABLE \` Component \` Free »**

 

 



