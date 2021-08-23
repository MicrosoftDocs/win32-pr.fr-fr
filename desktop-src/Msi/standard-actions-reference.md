---
description: le Windows Installer a les actions standard suivantes.
ms.assetid: 219b5eb6-501f-4e30-b398-4ed5e0cdf2ab
title: Informations de référence sur les actions standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e88b4b60e3dd13dc4830a1ea4ba2d16a439546d1ced3dc2a8b7552780548d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627629"
---
# <a name="standard-actions-reference"></a>Informations de référence sur les actions standard

le Windows Installer a les actions standard suivantes.



| Nom de l'action                                                     | Brève description de l’action                                                                                                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ADMIN](admin-action.md)                                       | Action de niveau supérieur utilisée pour une installation administrative.                                                                                                                   |
| [PUBLIÉS](advertise-action.md)                               | Action de niveau supérieur appelée pour installer ou supprimer des composants publiés.                                                                                                         |
| [AllocateRegistrySpace](allocateregistryspace-action.md)       | Valide que l’espace libre spécifié par [**AVAILABLEFREEREG**](availablefreereg.md) existe dans le registre.                                                               |
| [AppSearch](appsearch-action.md)                               | Recherche les versions précédentes des produits et détermine que les mises à niveau sont installées.                                                                                        |
| [BindImage](bindimage-action.md)                               | Lie les exécutables aux dll importées.                                                                                                                                           |
| [CCPSearch](ccpsearch-action.md)                               | Utilise des signatures de fichiers pour vérifier que les produits éligibles sont installés sur un système avant l’exécution d’une mise à niveau.                                              |
| [CostFinalize](costfinalize-action.md)                         | Termine le processus de coût d’installation interne commencé par l' [action CostInitialize](costinitialize-action.md).                                                               |
| [CostInitialize](costinitialize-action.md)                     | Démarre le processus d’évaluation des coûts d’installation.                                                                                                                                      |
| [CreateFolders](createfolders-action.md)                       | Crée des dossiers vides pour les composants.                                                                                                                                         |
| [CreateShortcuts](createshortcuts-action.md)                   | Crée des raccourcis.                                                                                                                                                            |
| [DeleteServices](deleteservices-action.md)                     | Supprime les services système.                                                                                                                                                      |
| [DisableRollback](disablerollback-action.md)                   | Désactive la restauration pour le reste de l’installation.                                                                                                                      |
| [DuplicateFiles](duplicatefiles-action.md)                     | Duplique les fichiers installés par l’action InstallFiles.                                                                                                                        |
| [ExecuteAction](executeaction-action.md)                       | Vérifie la propriété [**EXECUTEACTION**](executeaction.md) pour déterminer quelle action de niveau supérieur commence la séquence d’exécution, puis exécute cette action.                          |
| [FileCost](filecost-action.md)                                 | Initialise le calcul du coût du disque à l’aide du programme d’installation. Le coût du disque n’est pas finalisé tant que l’action CostFinalize n’est pas exécutée.                                                |
| [FindRelatedProducts](findrelatedproducts-action.md)           | Détecte la correspondance entre la [table de mise à niveau](upgrade-table.md) et les produits installés.                                                                                 |
| [ForceReboot](forcereboot-action.md)                           | Utilisé dans la séquence d’action pour inviter l’utilisateur à redémarrer le système pendant l’installation.                                                                           |
| [INSTALLER](install-action.md)                                   | Action de niveau supérieur appelée pour installer ou supprimer des composants.                                                                                                                    |
| [InstallAdminPackage](installadminpackage-action.md)           | Copie la base de données du programme d’installation sur le point d’installation d’administration.                                                                                                       |
| [InstallExecute](installexecute-action.md)                     | Exécute un script contenant toutes les opérations de la séquence d’action depuis le début de l’installation ou de la dernière action InstallFinalize. Ne met pas fin à la transaction.   |
| [InstallFiles](installfiles-action.md)                         | Copie les fichiers de la source vers le répertoire de destination.                                                                                                                    |
| [InstallFinalize](installfinalize-action.md)                   | Exécute un script contenant toutes les opérations de la séquence d’action depuis le début de l’installation ou de la dernière action InstallFinalize. Marque la fin d'une transaction. |
| [InstallInitialize](installinitialize-action.md)               | Marque le début d’une transaction.                                                                                                                                         |
| [InstallSFPCatalogFile](installsfpcatalogfile-action.md)       | l’action InstallSFPCatalogFile installe les catalogues utilisés par Windows Me pour la Protection des fichiers Windows.                                                                        |
| [InstallValidate](installvalidate-action.md)                   | Vérifie que tous les volumes avec des coûts attribués disposent de suffisamment d’espace pour l’installation.                                                                                   |
| [IsolateComponents](isolatecomponents-action.md)               | Traite la [table IsolatedComponent](isolatedcomponent-table.md)                                                                                                          |
| [LaunchConditions](launchconditions-action.md)                 | Évalue un ensemble d’instructions conditionnelles contenues dans la table LaunchCondition qui doivent toutes avoir la valeur true pour que l’installation puisse se poursuivre.                          |
| [MigrateFeatureStates](migratefeaturestates-action.md)         | Migre les États des fonctionnalités actuelles vers l’installation en attente.                                                                                                                  |
| [MoveFiles](movefiles-action.md)                               | Localise des fichiers existants, déplace ou copie ces fichiers vers un nouvel emplacement.                                                                                                     |
| [MsiConfigureServices](msiconfigureservices-action.md)         | Configure un service pour le système. **[Windows Installer 4,5 et versions antérieures](not-supported-in-windows-installer-4-5.md):** Non pris en charge.<br/>                           |
| [Action MsiPublishAssemblies](msipublishassemblies-action.md)  | Gère la publication des assemblys common language runtime et des assemblys Win32 en cours d’installation.                                                                |
| [MsiUnpublishAssemblies](msiunpublishassemblies-action.md)     | Gère la publication d’assemblys common language runtime et d’assemblys Win32 en cours de suppression.                                                                  |
| [InstallODBC](installodbc-action.md)                           | Installe les pilotes, les traducteurs et les sources de données ODBC.                                                                                                                     |
| [InstallServices](installservices-action.md)                   | Inscrit un service auprès du système.                                                                                                                                          |
| [PatchFiles](patchfiles-action.md)                             | Interroge la table des correctifs pour déterminer les correctifs appliqués à des fichiers spécifiques, puis effectue la mise à jour corrective par octet des fichiers.                                       |
| [ProcessComponents](processcomponents-action.md)               | Inscrit les composants, leurs chemins d’accès aux clés et les clients des composants.                                                                                                                 |
| [PublishComponents](publishcomponents-action.md)               | Publie les composants spécifiés dans la table PublishComponent.                                                                                                            |
| [PublishFeatures](publishfeatures-action.md)                   | Écrit l’état des fonctionnalités de chaque fonctionnalité dans le registre système.                                                                                                             |
| [PublishProduct](publishproduct-action.md)                     | Publie les informations sur le produit avec le système.                                                                                                                                |
| [RegisterClassInfo](registerclassinfo-action.md)               | Gère l’inscription des informations de classe COM dans le système.                                                                                                            |
| [RegisterComPlus](registercomplus-action.md)                   | L’action RegisterComPlus inscrit des applications COM+.                                                                                                                       |
| [RegisterExtensionInfo](registerextensioninfo-action.md)       | Inscrit les informations relatives à l’extension auprès du système.                                                                                                                      |
| [RegisterFonts](registerfonts-action.md)                       | Inscrit les polices installées auprès du système.                                                                                                                                    |
| [RegisterMIMEInfo](registermimeinfo-action.md)                 | Inscrit les informations MIME auprès du système.                                                                                                                                   |
| [RegisterProduct](registerproduct-action.md)                   | Inscrit les informations sur le produit auprès du programme d’installation et stocke la base de données du programme d’installation sur l’ordinateur local.                                                                     |
| [RegisterProgIdInfo](registerprogidinfo-action.md)             | Inscrit les informations ProgId OLE auprès du système.                                                                                                                             |
| [RegisterTypeLibraries](registertypelibraries-action.md)       | Inscrit les bibliothèques de types avec le système.                                                                                                                                     |
| [RegisterUser](registeruser-action.md)                         | Inscrit les informations utilisateur pour identifier l’utilisateur d’un produit.                                                                                                                 |
| [RemoveDuplicateFiles](removeduplicatefiles-action.md)         | Supprime les fichiers installés par l’action DuplicateFiles.                                                                                                                         |
| [RemoveEnvironmentStrings](removeenvironmentstrings-action.md) | Modifie les valeurs des variables d’environnement.                                                                                                                                 |
| [RemoveExistingProducts](removeexistingproducts-action.md)     | Supprime les versions installées d’un produit.                                                                                                                                      |
| [RemoveFiles](removefiles-action.md)                           | Supprime les fichiers précédemment installés par l’action InstallFiles.                                                                                                                |
| [RemoveFolders](removefolders-action.md)                       | Supprime les dossiers vides liés à l’ensemble de composants à supprimer.                                                                                                                 |
| [RemoveIniValues](removeinivalues-action.md)                   | Supprime .ini informations de fichier associées à un composant spécifié dans la table IniFile.                                                                                     |
| [RemoveODBC](removeodbc-action.md)                             | Supprime les sources de données, les traducteurs et les pilotes ODBC.                                                                                                                          |
| [RemoveRegistryValues](removeregistryvalues-action.md)         | Supprime les clés de registre d’une application qui ont été créées à partir de la table du Registre.                                                                                            |
| [RemoveShortcuts](removeshortcuts-action.md)                   | Gère la suppression d’un raccourci publié dont la fonctionnalité est sélectionnée pour la désinstallation.                                                                                   |
| [ResolveSource](resolvesource-action.md)                       | Détermine l’emplacement source et définit la propriété [**SourceDir**](sourcedir.md) .                                                                                          |
| [RMCCPSearch](rmccpsearch-action.md)                           | Utilise des signatures de fichiers pour vérifier que les produits éligibles sont installés sur un système avant l’exécution d’une mise à niveau.                                              |
| [ScheduleReboot](schedulereboot-action.md)                     | Invite l’utilisateur à redémarrer le système à la fin de l’installation.                                                                                                         |
| [SelfRegModules](selfregmodules-action.md)                     | Traite les modules de la table SelfReg et les enregistre s’ils sont installés.                                                                                              |
| [SelfUnregModules](selfunregmodules-action.md)                 | Annule l’enregistrement des modules de la table SelfReg qui sont configurés pour être désinstallés.                                                                                                  |
| [SÉQUENCE](sequence-action.md)                                 | Exécute les actions dans une table spécifiée par la propriété [**Sequence**](sequence.md) .                                                                                           |
| [Action SetODBCFolders](setodbcfolders-action.md)              | Recherche dans le système les pilotes ODBC existants et définit le répertoire cible pour les nouveaux pilotes ODBC.                                                                                   |
| [StartServices](startservices-action.md)                       | Démarre les services système.                                                                                                                                                       |
| [StopServices](stopservices-action.md)                         | Arrête les services système.                                                                                                                                                        |
| [UnpublishComponents](unpublishcomponents-action.md)           | Gère l’annulation de la publication des composants à partir de la table PublishComponent et supprime les informations relatives aux composants publiés.                                                 |
| [UnpublishFeatures](unpublishfeatures-action.md)               | Supprime les informations de mappage de l’état de sélection et du composant de fonctionnalité du Registre système.                                                                               |
| [UnregisterClassInfo](unregisterclassinfo-action.md)           | Gère la suppression des classes COM du Registre système.                                                                                                                  |
| [UnregisterComPlus](unregistercomplus-action.md)               | L’action UnregisterComPlus supprime les applications COM+ du Registre.                                                                                                     |
| [UnregisterExtensionInfo](unregisterextensioninfo-action.md)   | Gère la suppression des informations relatives à l’extension à partir du système.                                                                                                         |
| [UnregisterFonts](unregisterfonts-action.md)                   | Supprime les informations d’inscription relatives aux polices installées du système.                                                                                                       |
| [UnregisterMIMEInfo](unregistermimeinfo-action.md)             | Annule l’enregistrement des informations relatives à MIME dans le registre système.                                                                                                                |
| [UnregisterProgIdInfo](unregisterprogidinfo-action.md)         | Gère l’annulation de l’inscription des informations ProgId OLE avec le système.                                                                                                         |
| [UnregisterTypeLibraries](unregistertypelibraries-action.md)   | Annule l’inscription des bibliothèques de types avec le système.                                                                                                                                   |
| [ValidateProductID](validateproductid-action.md)               | Définit la propriété [**ProductID**](productid.md) sur l’identificateur complet du produit.                                                                                                  |
| [WriteEnvironmentStrings](writeenvironmentstrings-action.md)   | Modifie les valeurs des variables d’environnement.                                                                                                                                 |
| [WriteIniValues](writeinivalues-action.md)                     | Écrit .ini informations sur le fichier.                                                                                                                                                 |
| [WriteRegistryValues](writeregistryvalues-action.md)           | Définit les informations du Registre.                                                                                                                                                 |



 

 

 




