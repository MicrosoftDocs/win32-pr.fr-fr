---
description: Une spécification de l’exemple est que les informations de compte d’utilisateur sont lues à partir d’une table personnalisée dans la base de données d’installation et ne sont pas codées en dur dans l’action personnalisée.
ms.assetid: 1545b4f1-3ccf-4745-90d8-15f1f79d8455
title: Ajout d’une table CustomUserAccounts personnalisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d58366c725ecc135b9583c926a16383a5ad5a01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106525023"
---
# <a name="adding-a-custom-customuseraccounts-table"></a>Ajout d’une table CustomUserAccounts personnalisée

Une spécification de l’exemple est que les informations de compte d’utilisateur sont lues à partir d’une table personnalisée dans la base de données d’installation et ne sont pas codées en dur dans l’action personnalisée.

Ajoutez une table personnalisée à l’exemple de base de données d’installation nommée CustomUserAccounts pour contenir les informations du compte d’utilisateur. Pour obtenir un exemple d’ajout d’une table personnalisée [, consultez Exemples de requêtes de base de données avec SQL et script](examples-of-database-queries-using-sql-and-script.md) . Utilisez le schéma suivant pour la table CustomUserAccounts. Pour obtenir une explication des types de colonnes, consultez [format de définition de colonne](column-definition-format.md) .



| Colonne     | Type | Clé | Nullable | Description                                                                                                                                                                                                                                                                                                |
|------------|------|-----|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UserName   | S72  | O   | N        | Nom du compte d’utilisateur en cours de création.                                                                                                                                                                                                                                                                        |
| Mot de passe   | S72  |     | N        | Nom de la propriété contenant le mot de passe du compte. Il s’agit d’une [propriété publique](public-properties.md) définie sur la ligne de commande ou par le biais d’un [contrôle d’édition](edit-control.md) dans l’interface utilisateur. Ce contrôle d’édition doit avoir l' [attribut de contrôle de mot de passe](password-control-attribute.md). |
| Attributs | i4   |     | O        | Attributs du compte. Celles-ci sont définies en tant que valeurs **DWORD** pour le \_ membre indicateurs usri1 de la \_ structure informations utilisateur \_ 1.                                                                                                                                                                              |



 

Une fois la table CustomUserAccounts ajoutée à la base de données, vous pouvez modifier cette table à l’aide d’Orca, un éditeur de tables fourni avec le kit de développement logiciel (SDK) Windows Installer, ou un autre éditeur. Entrez l’enregistrement suivant dans la table CustomUserAccounts pour créer un compte d’utilisateur sécurisé par mot de passe pour un utilisateur nommé TestUser. Notez que 512 est la valeur numérique du \_ compte normal UF \_ .

Table CustomUserAccounts



| UserName | Mot de passe         | Attributs |
|----------|------------------|------------|
| UtilisateurTest | TESTUSERPASSWORD | 512        |



 

Ajoutez les enregistrements suivants au \_ tableau de validation pour la table personnalisée.

[\_Tableau de validation](-validation-table.md)



| Table de charge de travail              | Colonne     | Nullable | MinValue | MaxValue   | Keytable | KeyColumn | Category                     | Définissez | Description |
|--------------------|------------|----------|----------|------------|----------|-----------|------------------------------|-----|-------------|
| CustomUserAccounts | UserName   | N        |          |            |          |           | [Text](text.md)             |     |             |
| CustomUserAccounts | Mot de passe   | N        |          |            |          |           | [Identificateur](identifier.md) |     |             |
| CustomUserAccounts | Attributs | O        | 0        | 2147483647 |          |           | null                         |     |             |



 

Continuez à [créer les tables ActionText et Error](authoring-the-actiontext-and-error-tables.md).

 

 



