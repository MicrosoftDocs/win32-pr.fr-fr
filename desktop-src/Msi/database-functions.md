---
description: Ce document est destiné aux développeurs qui écrivent leurs propres programmes d’installation et développeurs qui souhaitent en savoir plus sur les tables de la base de données du programme d’installation. Pour obtenir des informations générales sur le programme d’installation, consultez à propos de Windows Installer.
ms.assetid: 95516437-9708-4f4e-a5c2-7bcd4741c776
title: Fonctions de base de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4a4233437d24944c8bb7fe5c7de6412e700022b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752797"
---
# <a name="database-functions"></a>Fonctions de base de données

Ce document est destiné aux développeurs qui écrivent leurs propres programmes d’installation et développeurs qui souhaitent en savoir plus sur les tables de la base de données du programme d’installation. Pour obtenir des informations générales sur le programme d’installation, consultez [à propos de Windows Installer](about-windows-installer.md).

Vous pouvez utiliser les fonctions d’installation pour accéder à la base de données et au processus d’installation. Ces fonctions ne doivent être utilisées que par les actions d’installation personnalisée et les outils de création. Certaines fonctions d’accès au programme d’installation requièrent des chaînes de requête SQL pour interroger la base de données. Les requêtes doivent adhérer à la [syntaxe SQL](sql-syntax.md)du programme d’installation.

Cette rubrique répertorie les fonctions d’accès à la base de données du programme d’installation par catégorie.

## <a name="general-database-access-functions"></a>Fonctions générales d’accès aux bases de données



| Fonction                                                             | Description                                                                             |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)                       | Valide les modifications apportées à une base de données.                                                          |
| [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa)       | Retourne les noms de toutes les colonnes clés primaires.                                       |
| [**MsiDatabaseIsTablePersistent**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta) | Retourne une énumération décrivant l’état d’une table.                                 |
| [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa)                   | Prépare une requête de base de données et crée un objet de vue.                                    |
| [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase)                 | Retourne la base de données active pour l’installation.                                       |
| [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo)                 | Retourne des définitions ou des noms de colonnes.                                                    |
| [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea)                           | Ouvre un fichier de base de données pour l’accès aux données.                                                  |
| [**MsiViewClose**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose)                                 | Libère le jeu de résultats pour une vue exécutée.                                           |
| [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute)                             | Exécute la requête de vue et fournit les paramètres requis.                               |
| [**MsiViewFetch**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch)                                 | Extrait l’enregistrement séquentiel suivant de la vue.                                       |
| [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora)                           | Retourne l’erreur qui s’est produite dans la fonction [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) . |
| [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify)                               | Met à jour un enregistrement extrait.                                                               |



 

## <a name="database-management-functions"></a>Fonctions de gestion de base de données



| Fonction                                                               | Description                                                      |
|------------------------------------------------------------------------|------------------------------------------------------------------|
| [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) | Crée des informations de synthèse pour une transformation existante.           |
| [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)         | Applique une transformation à une base de données.                               |
| [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)                         | Exporte une table d’une base de données ouverte dans un fichier d’archive de texte.    |
| [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)   | Génère un fichier de transformation de différences entre deux bases de données. |
| [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)                         | Importe une table d’archive de texte du programme d’installation dans une base de données ouverte.   |
| [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)                           | Fusionne deux bases de données.                                   |
| [**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)                     | Retourne l’état de la base de données.                               |



 

## <a name="record-processing-functions"></a>Fonctions de traitement des enregistrements



| Fonction                                                 | Description                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------|
| [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord)               | Crée un objet record avec le nombre spécifié de champs.      |
| [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)               | Met en forme les données et les propriétés des champs d’enregistrement à l’aide d’une chaîne de format. |
| [**MsiRecordClearData**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata)         | Affecte la valeur null à tous les champs d’un enregistrement.                            |
| [**MsiRecordDataSize**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize)           | Retourne la longueur d’un champ d’enregistrement.                           |
| [**MsiRecordGetFieldCount**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) | Retourne le nombre de champs dans un enregistrement.                       |
| [**MsiRecordGetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger)       | Retourne la valeur entière d’un champ d’enregistrement.                  |
| [**MsiRecordGetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa)         | Retourne la valeur de chaîne d’un champ d’enregistrement.                     |
| [**MsiRecordIsNull**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull)               | Indique si un champ d’enregistrement a la valeur null.                         |
| [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream)       | Lit les octets d’un champ de flux d’enregistrement dans une mémoire tampon.           |
| [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger)       | Définit un champ d’enregistrement sur un champ de type entier.                        |
| [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama)         | Définit un champ de flux d’enregistrement à partir d’un fichier.                         |
| [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa)         | Copie une chaîne dans le champ désigné.                      |



 

## <a name="summary-information-property-functions"></a>Fonctions de propriété des informations de résumé



| Fonction                                                                 | Description                                                            |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa)             | Obtient le handle du flux d’informations récapitulatives de la base de données du programme d’installation.    |
| [**MsiSummaryInfoGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)           | Obtient une propriété unique à partir des informations de résumé.                   |
| [**MsiSummaryInfoGetPropertyCount**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertycount) | Retourne le nombre de propriétés dans le flux d’informations de résumé.        |
| [**MsiSummaryInfoPersist**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfopersist)                   | Écrit les informations de résumé modifiées dans le flux d’informations de synthèse. |
| [**MsiSummaryInfoSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya)           | Définit une propriété d’informations de résumé unique.                            |



 

## <a name="installer-state-access-functions"></a>Fonctions d’accès à l’état du programme d’installation



| Fonction                                               | Description                                                 |
|--------------------------------------------------------|-------------------------------------------------------------|
| [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage)               | Retourne la langue numérique de l’installation actuelle.   |
| [**MsiGetLastErrorRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlasterrorrecord) | Retourne le dernier enregistrement d’erreur retourné pour le processus appelant. |
| [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode)                       | Retourne l’un des États d’installation internes booléens.    |
| [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)               | Obtient la valeur d’une propriété du programme d’installation.                    |
| [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya)               | Définit la valeur d’une propriété d’installation.                 |
| [**MsiSetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode)                       | Définit un état booléen du moteur interne.                      |



 

## <a name="installer-action-functions"></a>Fonctions d’action du programme d’installation



| Fonction                                             | Description                                                               |
|------------------------------------------------------|---------------------------------------------------------------------------|
| [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona)                   | Exécute une action intégrée, une action personnalisée ou une action de l’Assistant interface utilisateur. |
| [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) | Évalue une expression conditionnelle contenant des noms et des valeurs de propriété.  |
| [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)       | Envoie un enregistrement d’erreur au programme d’installation pour traitement.                    |
| [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea)                   | Exécute une séquence d’action.                                              |



 

## <a name="installer-location-functions"></a>Fonctions d’emplacement du programme d’installation



| Fonction                                     | Description                                                       |
|----------------------------------------------|-------------------------------------------------------------------|
| [**MsiGetSourcePath**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha) | Retourne le chemin d’accès source complet d’un dossier dans la table de répertoires. |
| [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) | Retourne le chemin d’accès cible complet d’un dossier dans la table de répertoires. |
| [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) | Définit le chemin d’accès cible complet d’un dossier dans la table de répertoires.    |



 

## <a name="installer-selection-functions"></a>Fonctions de sélection du programme d’installation



| Fonction                                                     | Description                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------|
| [**MsiEnumComponentCosts**](/windows/desktop/api/Msiquery/nf-msiquery-msienumcomponentcostsa)       | Énumère l’espace disque par lecteur requis pour installer un composant. |
| [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)         | Obtient l’état d’un composant.                                    |
| [**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)               | Retourne l’espace disque requis par une fonctionnalité.                        |
| [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)             | Obtient l’état d’une fonctionnalité.                                         |
| [**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) | Retourne un état d’installation valide.                                  |
| [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea)         | Définit un composant à l’état spécifié.                             |
| [**MsiSetFeatureAttributes**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeatureattributesa)   | Modifie les attributs par défaut d’une fonctionnalité au moment de l’exécution.            |
| [**MsiSetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea)             | Affecte un état spécifié à une fonctionnalité.                                 |
| [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel)             | Définit le niveau d’installation d’une installation complète du produit.          |
| [**MsiVerifyDiskSpace**](/windows/desktop/api/Msiquery/nf-msiquery-msiverifydiskspace)             | Vérifie que l’espace disque est suffisant.                                    |



 

## <a name="user-interface-functions"></a>Fonctions de l’interface utilisateur



| Fonction                                           | Description                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [**MsiEnableUIPreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)   | Active le mode aperçu de l’interface utilisateur.                             |
| [**MsiPreviewBillboard**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda) | Affiche un tableau blanc avec le contrôle hôte dans la boîte de dialogue affichée. |
| [**MsiPreviewDialog**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga)       | Affiche une boîte de dialogue non modale et inactive.                         |



 

Toutes les fonctions prennent en charge les appels ANSI et Unicode. Pour utiliser ces fonctions, incluez MsiQuery. h et liez-le à msi. lib.

## <a name="installation-functions"></a>Fonctions d’installation

Outre les fonctions d’accès à la base de données listées ci-dessus, vous créez un package d’installation pour une application à l’aide des fonctions de programme d’installation listées dans la section [référence des fonctions du programme](installer-function-reference.md) d’installation.

 

 



