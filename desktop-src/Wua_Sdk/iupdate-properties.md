---
description: L’interface IUpdate définit les propriétés suivantes.
ms.assetid: d87544f1-a107-440f-8ce0-77d9f2d90578
title: Propriétés IUpdate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df3f67f95936ea54dd09131e605da9e439caa43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526692"
---
# <a name="iupdate-properties"></a>Propriétés IUpdate

L’interface [**IUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate) définit les propriétés suivantes.



| Propriété                                                                           | Description                                                                                                                                                                         |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutoSelectOnWebSites**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_autoselectonwebsites)                       | Obtient une valeur booléenne qui indique si la mise à jour est marquée comme étant automatiquement sélectionnée par Windows Update.                                                                   |
| [**BundledUpdates**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_bundledupdates)                                   | Obtient une interface qui contient des informations sur la liste triée des mises à jour regroupées pour la mise à jour.                                                                           |
| [**CanRequireSource**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_canrequiresource)                               | Obtient une valeur booléenne qui indique si le média source de la mise à jour est requis pour l’installation ou la désinstallation.                                                          |
| [**Catégories**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_categories)                                           | Obtient une interface qui contient une collection de catégories auxquelles la mise à jour appartient.                                                                                             |
| [**Échéance**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deadline)                                               | Obtient la date à laquelle la mise à jour doit être installée.                                                                                                                                |
| [**DeltaCompressedContentAvailable**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deltacompressedcontentavailable) | Obtient une valeur booléenne qui indique si le contenu Delta-compressé est disponible sur un serveur pour la mise à jour.                                                                       |
| [**DeltaCompressedContentPreferred**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deltacompressedcontentpreferred) | Obtient une valeur booléenne qui indique s’il faut préférer le contenu Delta-compressée pendant le téléchargement et l’installation ou la désinstallation de la mise à jour si le contenu compressé Delta est disponible. |
| [**DeploymentAction**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deploymentaction)                               | Obtient l’action pour laquelle la mise à jour est déployée.                                                                                                                                   |
| [**Description**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_description)                                         | Obtient la description localisée de la mise à jour.                                                                                                                                       |
| [**DownloadContents**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_downloadcontents)                               | Obtient des informations de fichier sur le contenu de téléchargement de la mise à jour.                                                                                                                    |
| [**DownloadPriority**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_downloadpriority)                               | Obtient la priorité de téléchargement suggérée de la mise à jour.                                                                                                                                 |
| [**EulaAccepted**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_eulaaccepted)                                       | Obtient une valeur booléenne qui indique si les termes du contrat de licence logiciel Microsoft associés à la mise à jour sont acceptés pour l’ordinateur.                                 |
| [**EulaText**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_eulatext)                                               | Obtient le texte localisé complet des termes du contrat de licence logiciel Microsoft associés à la mise à jour.                                                                           |
| [**HandlerID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_handlerid)                                             | Obtient le gestionnaire d’installation de la mise à jour.                                                                                                                                             |
| [**Identité**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_identity)                                               | Obtient une interface qui contient l’identificateur unique de la mise à jour.                                                                                                                |
| [**Image**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_image)                                                     | Obtient une interface qui contient des informations à propos d’une image associée à la mise à jour.                                                                                      |
| [**InstallationBehavior**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_installationbehavior)                       | Obtient une interface qui contient les options d’installation de la mise à jour.                                                                                                             |
| [**IsBeta**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isbeta)                                                   | Obtient une valeur booléenne qui indique si la mise à jour est une version bêta.                                                                                                           |
| [**IsDownloaded**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isdownloaded)                                       | Obtient une valeur booléenne qui indique si tout le contenu de la mise à jour est mis en cache sur l’ordinateur.                                                                                       |
| [**IsHidden**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden)                                               | Obtient une valeur booléenne qui indique si une mise à jour est masquée par un utilisateur.                                                                                                          |
| [**IsInstalled**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isinstalled)                                         | Obtient une valeur booléenne qui indique si la mise à jour est installée sur un ordinateur lors de l’exécution de la recherche.                                                                     |
| [**IsMandatory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ismandatory)                                         | Obtient une valeur booléenne qui indique si l’installation de la mise à jour est obligatoire.                                                                                            |
| [**IsUninstallable**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isuninstallable)                                 | Obtient une valeur booléenne qui indique si un utilisateur peut désinstaller la mise à jour d’un ordinateur.                                                                                        |
| [**KBArticleIDs**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_kbarticleids)                                       | Obtient une collection d’ID d’Articles de la base de connaissances Microsoft associés à la mise à jour.                                                                                      |
| [**Langages**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_languages)                                              | Obtient une interface qui contient les langues prises en charge par la mise à jour.                                                                                                     |
| [**LastDeploymentChangeTime**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_lastdeploymentchangetime)               | Obtient la date de la dernière publication de la mise à jour, au format UTC (temps universel coordonné), sur le serveur qui déploie la mise à jour.                                               |
| [**MaxDownloadSize**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_maxdownloadsize)                                 | Obtient la taille de téléchargement maximale de la mise à jour.                                                                                                                                       |
| [**MinDownloadSize**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_mindownloadsize)                                 | Obtient la taille minimale de téléchargement de la mise à jour.                                                                                                                                       |
| [**MoreInfoUrls**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_moreinfourls)                                       | Obtient une collection de chaînes spécifiques au langage qui spécifient les liens hypertexte vers des informations supplémentaires sur la mise à jour.                                                                    |
| [**MsrcSeverity**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_msrcseverity)                                       | Obtient le niveau de gravité de la mise à jour du centre de réponse aux incidents de sécurité Microsoft.                                                                                                          |
| [**RecommendedCPUSpeed**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_recommendedcpuspeed)                         | Obtient la vitesse d’UC recommandée utilisée pour installer la mise à jour, en mégahertz (MHz).                                                                                                      |
| [**RecommendedHardDiskSpace**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_recommendedharddiskspace)               | Obtient l’espace libre recommandé qui doit être disponible sur le disque dur avant l’installation de la mise à jour. L’espace libre est spécifié en mégaoctets (Mo).                             |
| [**RecommendedMemory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_recommendedmemory)                             | Obtient la taille de mémoire physique recommandée qui doit être disponible sur votre ordinateur avant d’installer la mise à jour. La taille de la mémoire physique est exprimée en mégaoctets (Mo).         |
| [**ReleaseNotes**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_releasenotes)                                       | Obtient les notes de publication localisées pour la mise à jour.                                                                                                                                    |
| [**SecurityBulletinIDs**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_securitybulletinids)                         | Obtient une collection de valeurs de chaîne qui contiennent les ID de bulletin de sécurité associés à la mise à jour.                                                                      |
| [**SupersededUpdateIDs**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_supersededupdateids)                         | Obtient une collection d’identificateurs de mise à jour. Cette collection d’identificateurs spécifie les mises à jour qui sont remplacées par la mise à jour.                                                    |
| [**SupportUrl**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_supporturl)                                           | Obtient un lien hypertexte vers les informations de prise en charge propres à la langue pour la mise à jour.                                                                                                       |
| [**Intitulé**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title)                                                     | Obtient le titre localisé de la mise à jour.                                                                                                                                             |
| [**Entrer**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_type)                                                       | Obtient le type de la mise à jour.                                                                                                                                                        |
| [**UninstallationBehavior**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_uninstallationbehavior)                   | Obtient une interface qui contient les options de désinstallation de la mise à jour.                                                                                                          |
| [**UninstallationNotes**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_uninstallationnotes)                         | Obtient les notes de désinstallation de la mise à jour.                                                                                                                                       |
| [**UninstallationSteps**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_uninstallationsteps)                         | Obtient une interface qui contient les étapes de désinstallation de la mise à jour.                                                                                                            |



 

 

 



