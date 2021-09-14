---
description: modifiez l’une des autres colonnes localisables dans la base de données MNPFren.msi à l’aide d’un éditeur de tables comme Orca ou SQL requêtes.
ms.assetid: b62cf529-71a0-47ff-99ea-a182c0fe4479
title: Localiser des colonnes de base de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed36b1adb2c496c9019b482c929e449187b1e0bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011944"
---
# <a name="localizing-database-columns"></a>Localiser des colonnes de base de données

modifiez l’une des autres colonnes localisables dans la base de données MNPFren.msi à l’aide d’un éditeur de tables comme Orca ou SQL requêtes. Pour déterminer les colonnes d’une table particulière qui peuvent être localisées dans une autre langue, consultez la rubrique de référence pour cette table de base de données. Consultez [tables de base de données](database-tables.md) pour obtenir la liste de toutes les tables de base de données.

Par exemple, il peut être nécessaire de localiser le champ de texte de certains enregistrements dans la [table de contrôle](control-table.md) en français. La chaîne « êtes-vous sûr de vouloir annuler \[ \] l’installation de ProductName ? » la [boîte de dialogue annuler](cancel-dialog.md) peut être modifiée dans ce tableau pour être affichée en français. L’enregistrement d’origine dans .msi fichier se présente comme suit.

[Table de contrôle](control-table.md) (partielle) du fichier de .msi d’origine



| Dialogue\_  | Control | Type | X   | O   | Largeur | Hauteur | Attributs | Propriété | Texte                                                          | Contrôle \_ suivant | Aide |
|-----------|---------|------|-----|-----|-------|--------|------------|----------|---------------------------------------------------------------|---------------|------|
| CancelDlg | Texte    | Texte | 48  | 15  | 194   | 30     | 3          |          | Êtes-vous sûr de vouloir annuler \[ \] l’installation de ProductName ? |               |      |



 

vous pouvez utiliser un éditeur de table pour modifier le champ de texte, tel que l’éditeur de table Orca fourni avec le kit de développement logiciel (SDK) ou un autre éditeur de table, ou utiliser une requête de SQL pour modifier le champ de texte de l’enregistrement de la table de contrôle. un exemple illustrant des requêtes de base de données basées sur des scripts est fourni dans le kit de développement logiciel (SDK) Windows Installer, car l’utilitaire WiRunSQL.vbs. utilisez la ligne de commande suivante pour modifier le champ avec WiRunSQL.vbs et l’hôte de Script Windows. consultez également [des exemples de requêtes de base de données à l’aide de SQL et de Script](examples-of-database-queries-using-sql-and-script.md).

**Cscript WiRunSQL.vbs MNPFren.msi « contrôle de mise à jour du contrôle SET. Text = 'Etes-... vouloir annuler l’installation de \[ ProductName \] ? » WHERE Control. Dialog \_ = 'CancelDlg’et Control. Control = 'text' "**

[Table de contrôle](control-table.md) (partielle) dans MNPFren.msi



| Dialogue\_  | Control | Type | X   | O   | Largeur | Hauteur | Attributs | Propriété | Texte                                                                | Contrôle \_ suivant | Aide |
|-----------|---------|------|-----|-----|-------|--------|------------|----------|---------------------------------------------------------------------|---------------|------|
| CancelDlg | Texte    | Texte | 48  | 15  | 194   | 30     | 3          |          | Êtes-vous sûr de vouloir annuler l’installation de \[ ProductName \] ? |               |      |



 

Si l’installation de MNPFren.msi est annulée par l’utilisateur, la **boîte de dialogue annuler** s’affiche : « êtes-vous sûr de vouloir annuler L’INSTALLATION de MNP2000 ? »

Lors de l’utilisation de cette méthode pour localiser le texte de l’interface utilisateur dans un autre langage, l’interface utilisateur localisée doit être testée pour s’assurer que la taille des contrôles est suffisamment grande pour afficher l’intégralité du texte localisé. Ce test doit être testé à l’aide de tous les paramètres de taille de police disponibles pour l’affichage. Le texte localisé peut nécessiter plus d’espace que le texte d’origine et peut être tronqué s’il est affiché dans un contrôle qui est trop petit.

[Continuer](updating-productlanguage-and-productcode-properties.md)

 

 



