---
description: Pour activer Windows Installer dans votre application, vous devez utiliser les fonctions du programme d’installation. Les tableaux de cette rubrique identifient les fonctions par catégorie.
ms.assetid: 05a16915-6b47-4d51-b62a-5a4d92b87e50
title: Référence des fonctions du programme d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9261789f21bd559e49c4e5718ef68ce9d0bb41c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951203"
---
# <a name="installer-function-reference"></a>Référence des fonctions du programme d’installation

Pour activer Windows Installer dans votre application, vous devez utiliser les fonctions du programme d’installation. Les tableaux de cette rubrique identifient les fonctions par catégorie.

## <a name="user-interface-and-logging-functions"></a>Interface utilisateur et fonctions de journalisation



| Nom                                                     | Description                                                                           |
|----------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)             | Active l’interface utilisateur interne du programme d’installation.                                 |
| [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)             | Active un gestionnaire d’interface utilisateur externe qui reçoit des messages dans un format de chaîne. |
| [**MsiSetExternalUIRecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord) | Active un gestionnaire d’interface utilisateur externe qui reçoit des messages dans un format d’enregistrement. |
| [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga)                     | Définit le mode de journalisation pour toutes les installations dans le processus appelant.                       |



 

## <a name="handle-management-functions"></a>Gérer les fonctions de gestion



| Nom                                             | Description                                                   |
|--------------------------------------------------|---------------------------------------------------------------|
| [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle)         | Ferme un handle d’installation ouvert.                           |
| [**MsiCloseAllHandles**](/windows/desktop/api/Msi/nf-msi-msicloseallhandles) | Ferme tous les descripteurs d’installation ouverts. N’utilisez pas pour le nettoyage. |



 

## <a name="installation-and-configuration-functions"></a>Fonctions d’installation et de configuration



| Nom                                                                     | Description                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta)                       | Publie un produit.                                                                                                                                                                                                        |
| [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)                   | Publie un produit.                                                                                                                                                                                                        |
| [**MsiAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta)                         | Copie un fichier de script de publication dans des emplacements spécifiés.                                                                                                                                                                    |
| [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)                           | Installe ou supprime une application ou une suite d’applications.                                                                                                                                                                     |
| [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)                       | Installe ou supprime une application ou une suite d’applications.                                                                                                                                                                     |
| [**MsiConfigureProductEx**](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)                   | Installe ou supprime une application ou une suite d’applications. Une ligne de commande de produit peut être spécifiée.                                                                                                                            |
| [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)                       | Réinstalle ou répare une installation.                                                                                                                                                                                       |
| [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)                       | Configure l’état installé d’une fonctionnalité.                                                                                                                                                                                 |
| [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)                       | Valide ou répare les fonctionnalités.                                                                                                                                                                                               |
| [**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta)         | Installe les composants manquants.                                                                                                                                                                                                 |
| [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)                   | Installe les fichiers manquants.                                                                                                                                                                                                      |
| [**MsiNotifySidChange**](/windows/desktop/api/Msi/nf-msi-msinotifysidchangea)                         | Notifie et met à jour les informations internes du Windows Installer avec les modifications apportées aux sid des utilisateurs. Disponible à partir de Windows Installer 3,1.                                                                                   |
| [**MsiProcessAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiprocessadvertisescripta)           | Traite un fichier de script de publication à des emplacements spécifiés.                                                                                                                                                                 |
| [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea)                 | Ajoute ou réorganise les sources d’un correctif ou d’un produit dans un contexte spécifié.                                                                                                                                                   |
| [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)             | Ajoute ou réorganise les sources d’un correctif ou d’un produit dans un contexte spécifié. Crée une liste source pour un correctif qui n’existe pas dans un contexte spécifié. Disponible dans Windows Installer 3,0.                                |
| [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)             | Supprime une source existante pour un produit ou un correctif dans un contexte spécifié. Disponible dans Windows Installer 3,0.                                                                                                               |
| [**MsiSourceListClearAll**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearalla)                   | Supprime toutes les sources existantes d’un type de source spécifique pour une instance de produit spécifiée.                                                                                                                                 |
| [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)               | Supprime toutes les sources existantes d’un type de source spécifique pour une instance de produit spécifiée. Disponible dans Windows Installer 3,0.                                                                                            |
| [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)     | Supprime l’inscription de la source actuelle du produit ou du correctif, qui est enregistré en tant que propriété « LastUsedSource ». Cette fonction n’affecte pas la liste des sources inscrites.                                      |
| [**MsiSourceListForceResolutionEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutionexa) | Supprime l’inscription de la source actuelle du produit ou du correctif, qui est enregistré en tant que propriété « LastUsedSource ». Cette fonction n’affecte pas la liste des sources inscrites. Disponible dans Windows Installer 3,0. |
| [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)                     | Récupère des informations sur la liste source pour un produit ou un correctif dans un contexte spécifique.                                                                                                                                    |
| [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)                     | Définit la source utilisée le plus récemment pour un produit ou un correctif dans un contexte spécifié. Disponible dans Windows Installer 3,0.                                                                                                       |
| [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)       | Énumère la liste des disques inscrits pour la source du média pour un correctif ou un produit. Disponible dans Windows Installer 3,0.                                                                                                    |
| [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)           | Ajoute ou met à jour un disque de la source du média d’un produit ou d’un correctif enregistré. Disponible dans Windows Installer 3,0.                                                                                                            |
| [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)      | Supprime un disque inscrit existant sous la source du média pour un produit ou un correctif dans un contexte spécifique. Disponible dans Windows Installer 3,0.                                                                                |
| [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)             | Énumère les sources dans la liste source d’un correctif ou d’un produit spécifié. Disponible dans Windows Installer 3,0.                                                                                                              |



 

## <a name="component-specific-functions"></a>Fonctions Component-Specific



| Nom                                                                     | Description                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)                         | Installe et retourne le chemin d’accès complet du composant pour un assembly.                                                                                                                                                                 |
| [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)                       | Installe et retourne le chemin d’accès complet du composant d’un composant.                                                                                                                                                                  |
| [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)     | Installe et retourne le chemin d’accès complet du composant d’un composant qualifié.                                                                                                                                                        |
| [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa) | Installe et retourne le chemin d’accès complet du composant d’un composant qualifié qui est publié par un produit.                                                                                                                         |
| [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)                       | Retourne le chemin d’accès complet ou la clé de Registre à un composant installé.                                                                                                                                                              |
| [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)                   | Retourne le chemin d’accès complet ou la clé de registre d’un composant installé parmi les comptes d’utilisateur et le contexte d’installation. **[Windows Installer 4,5 et versions antérieures](not-supported-in-windows-installer-4-5.md):** Non pris en charge.<br/> |
| [**MsiLocateComponent**](/windows/desktop/api/Msi/nf-msi-msilocatecomponenta)                         | Retourne le chemin d’accès complet à un composant installé sans code produit.                                                                                                                                                       |
| [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)                 | Retourne l’état installé pour un composant. Peut interroger des composants d’une instance d’un produit installé sous des comptes d’utilisateurs autres que l’utilisateur actuel. Disponible dans Windows Installer 3,0 ou version ultérieure.                        |



 

## <a name="application-only-functions"></a>Fonctions Application-Only



| Nom                                             | Description                                                            |
|--------------------------------------------------|------------------------------------------------------------------------|
| [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) | Stocke les informations utilisateur à partir d’un Assistant installation.                   |
| [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea)           | Incrémente le nombre d’utilisations d’une fonctionnalité et indique l’état de l’installation. |
| [**MsiUseFeatureEx**](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)       | Incrémente le nombre d’utilisations d’une fonctionnalité et indique l’état de l’installation. |
| [**MsiGetProductCode**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea)   | Retourne le code du produit à l’aide du code du composant.                         |



 

## <a name="system-status-functions"></a>Fonctions d’État du système



| Nom                                                             | Description                                                                                                                                                                                                                       |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa)                       | Énumère les produits publiés.                                                                                                                                                                                                   |
| [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)                   | Énumère toutes les instances de produits publiés ou installés dans un contexte spécifié. Disponible dans Windows Installer 3,0 ou version ultérieure.                                                                                    |
| [**MsiEnumRelatedProducts**](/windows/desktop/api/Msi/nf-msi-msienumrelatedproductsa)         | Énumère les produits actuellement installés avec un code de mise à niveau spécifié.                                                                                                                                                          |
| [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa)                       | Énumère les fonctionnalités publiées.                                                                                                                                                                                                    |
| [**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa)                   | Énumère les composants installés.                                                                                                                                                                                              |
| [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)               | Énumère les composants installés entre les comptes d’utilisateur et le contexte d’installation. **[Windows Installer 4,5 et versions antérieures](not-supported-in-windows-installer-4-5.md):** Non pris en charge.<br/>                                 |
| [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa)                         | Énumère les clients d’un composant installé.                                                                                                                                                                                 |
| [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)                     | Énumère les clients d’un composant installé entre les comptes d’utilisateur et le contexte d’installation. **[Windows Installer 4,5 et versions antérieures](not-supported-in-windows-installer-4-5.md):** Non pris en charge.<br/>                    |
| [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa) | Énumère les qualificateurs publiés pour un composant.                                                                                                                                                                             |
| [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea)             | Retourne l’état installé d’une fonctionnalité.                                                                                                                                                                                         |
| [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)         | Retourne l’état installé pour une fonctionnalité de produit. Peut interroger les fonctionnalités d’une instance d’un produit installé sous comptes d’utilisateur autres que l’utilisateur actuel. Disponible dans Windows Installer 3,0 ou version ultérieure.                        |
| [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)             | Retourne l’état installé pour une application ou une suite d’applications.                                                                                                                                                              |
| [**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)                 | Retourne les métriques d’utilisation d’une fonctionnalité.                                                                                                                                                                                              |
| [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)                   | Retourne des informations sur le produit pour les produits publiés et installés.                                                                                                                                                                 |
| [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa)               | Retourne des informations sur les produits publiés et installés. Peut récupérer des informations sur une instance d’un produit installé sous un compte d’utilisateur autre que l’utilisateur actuel. Disponible dans Windows Installer 3,0 ou version ultérieure. |
| [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa)                         | Retourne les informations utilisateur inscrites pour un produit installé.                                                                                                                                                                     |



 

## <a name="product-query-functions"></a>Fonctions de requête de produit



| Nom                                                               | Description                                                                            |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta)                           | Ouvre un produit à utiliser avec les fonctions qui accèdent à la base de données.                    |
| [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)                           | Ouvre un package à utiliser avec les fonctions qui accèdent à la base de données.                    |
| [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa)                       | Ouvre un package à utiliser avec les fonctions qui accèdent à la base de données.                    |
| [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)               | Vérifie si le produit est installé avec des privilèges élevés.                      |
| [**MsiGetProductInfoFromScript**](/windows/desktop/api/Msi/nf-msi-msigetproductinfofromscripta) | Retourne les informations sur le produit pour un fichier de script d’installation.                              |
| [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya)             | Récupère les propriétés de la base de données du produit.                                          |
| [**MsiGetShortcutTarget**](/windows/desktop/api/Msi/nf-msi-msigetshortcuttargeta)               | Examine un raccourci et retourne son produit, son nom de fonctionnalité et son composant, le cas échéant. |
| [**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)                     | Retourne des informations descriptives pour une fonctionnalité.                                         |
| [**MsiVerifyPackage**](/windows/desktop/api/Msi/nf-msi-msiverifypackagea)                       | Vérifie qu’un fichier spécifié est un package d’installation.                             |



 

## <a name="patching-functions"></a>Fonctions de mise à jour corrective



| Nom                                                                   | Description                                                                                                                                                        |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)                                 | Appelle une installation et applique un package de correctifs.                                                                                                               |
| [**MsiEnumPatches**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)                    | Retourne le GUID de chaque correctif appliqué à un produit, ainsi qu’une liste des transformations de chaque correctif qui s’appliquent au produit.                                  |
| [**MsiGetPatchInfo**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoa)                             | Retourne des informations sur un correctif.                                                                                                                                 |
| [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)                           | Désinstalle un correctif d’un produit. Disponible dans Windows Installer 3,0.                                                                                             |
| [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)         | Détermine la meilleure séquence d’application pour un ensemble de correctifs et de produits. Disponible dans Windows Installer 3,0.                                                     |
| [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)             | Applique un ou plusieurs correctifs aux produits. Disponible dans Windows Installer 3,0.                                                                                       |
| [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)                           | Énumère tous les correctifs appliqués à un produit dans un contexte particulier ou dans tous les contextes. Disponible dans Windows Installer 3,0.                                   |
| [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista)                     | Lorsque vous avez fourni une liste de fichiers. msp, cette fonction récupère la liste des fichiers qui peuvent être mis à jour par les correctifs pour le cible. Disponible dans Windows Installer 4,0. |
| [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)                         | Recherche des informations sur l’application d’un correctif spécifique à un produit spécifié. Disponible dans Windows Installer 3,0.                                     |
| [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)               | Extrait des informations d’un correctif. Disponible dans Windows Installer 3,0.                                                                                             |
| [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) | Détermine le meilleur ensemble de correctifs requis pour mettre à jour un produit ou un ensemble de produits. Disponible dans Windows Installer 3,0.                                            |



 

## <a name="file-query-functions"></a>Fonctions de requête de fichier



| Nom                                                                     | Description                                                                                                 |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)                                 | Prend le chemin d’accès à un fichier et retourne un hachage 128 bits de ce fichier.                                           |
| [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa) | Prend le chemin d’accès à un fichier qui a été signé numériquement et retourne le certificat du signataire et le hachage du fichier. |
| [**MsiGetFileVersion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona)                           | Retourne la chaîne de version et la chaîne de langue.                                                             |



 

## <a name="transaction-management-functions"></a>Fonctions de gestion des transactions



| Nom                                               | Description                                                                                                                                                                                         |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiBeginTransaction**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona) | Démarre le traitement des transactions d’une installation de plusieurs packages et retourne un identificateur pour la transaction. Cette fonction est disponible à partir de Windows Installer 4,5.                    |
| [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction)   | Demande que l’Windows Installer que le processus actuel soit le propriétaire de la transaction qui installe une installation de plusieurs packages. Cette fonction est disponible à partir de Windows Installer 4,5. |
| [**MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction)     | Valide ou restaure toutes les installations appartenant à la transaction. Cette fonction est disponible à partir de Windows Installer 4,5.                                                          |



 

## <a name="database-functions"></a>Fonctions de base de données

Outre les fonctions de Windows Installer identifiées dans les tables précédentes, vous pouvez manipuler les informations de la base de données d’installation à l’aide des fonctions d’accès à la base de données décrites dans la section [fonctions de base de données](database-functions.md) .

## <a name="installer-structures"></a>Structures du programme d’installation

En outre, certaines informations de la base de données d’installation sont gérées à l’aide des structures décrites dans la section [structures du programme d’installation](installer-structures.md) .

 

 




