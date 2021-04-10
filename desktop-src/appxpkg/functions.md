---
title: API de requête de package
description: En savoir plus sur l’API de requête de package, que vous pouvez utiliser pour obtenir des informations sur les packages d’application installés sur le système. Chaque package d’application contient les fichiers qui constituent une application Windows et un fichier manifeste décrivant le logiciel à Windows.
ms.assetid: EDDFC8B1-E224-4921-BED6-FC81711BA5BF
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 5632edf661b4ea82177473bbb35f2674674500c6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031065"
---
# <a name="package-query-api"></a>API de requête de package

En savoir plus sur l’API de requête de package, que vous pouvez utiliser pour obtenir des informations sur les packages d’application installés sur le système. Chaque package d’application contient les fichiers qui constituent une application Windows et un fichier manifeste décrivant le logiciel à Windows.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                 | Description                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClosePackageInfo**](/windows/desktop/api/AppModel/nf-appmodel-closepackageinfo)<br/>                                               | Ferme une référence aux informations de package spécifiées.<br/>                                                                                              |
| [**FindPackagesByPackageFamily**](/windows/desktop/api/AppModel/nf-appmodel-findpackagesbypackagefamily)<br/>                         | Recherche les packages avec le nom de famille spécifié pour l’utilisateur actuel. <br/>                                                                              |
| [**FormatApplicationUserModelId**](/windows/desktop/api/AppModel/nf-appmodel-formatapplicationusermodelid)<br/>                       | Construit un [ID de modèle utilisateur d’application](appx-packaging-glossary.md) à partir du nom de la famille de packages et de l’ID d’application relatif du package (Praid). <br/> |
| [**GetApplicationUserModelId**](/windows/desktop/api/Appmodel/nf-appmodel-getapplicationusermodelid)<br/>                             | Obtient l' [ID du modèle utilisateur](appx-packaging-glossary.md) de l’application pour le processus spécifié.<br/>                                                          |
| [**GetApplicationUserModelIdFromToken**](/windows/desktop/api/Appmodel/nf-appmodel-getapplicationusermodelidfromtoken)<br/>           | Obtient l' [ID du modèle utilisateur](appx-packaging-glossary.md) de l’application pour le jeton spécifié.<br/>                                                            |
| [**GetCurrentApplicationUserModelId**](/windows/desktop/api/Appmodel/nf-appmodel-getcurrentapplicationusermodelid)<br/>               | Obtient l' [ID du modèle utilisateur](appx-packaging-glossary.md) de l’application pour le processus en cours.<br/>                                                            |
| [**GetCurrentPackageFamilyName**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagefamilyname)<br/>                         | Obtient le nom de la famille de packages pour le processus appelant.<br/>                                                                                                 |
| [**GetCurrentPackageFullName**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagefullname)<br/>                             | Obtient le nom complet du package pour le processus appelant.<br/>                                                                                                   |
| [**GetCurrentPackageId**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackageid)<br/>                                         | Obtient l’identificateur de package (ID) du processus appelant.<br/>                                                                                             |
| [**GetCurrentPackageInfo**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackageinfo)<br/>                                     | Obtient les informations de package pour le processus appelant.<br/>                                                                                                 |
| [**GetCurrentPackageInfo2**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackageinfo2)<br/>                                     | Obtient les informations de package pour le processus appelant, avec l’option permettant de spécifier le type de dossier du package.<br/>                                                                                               |
| [**GetCurrentPackagePath**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagepath)<br/>                                     | Obtient le chemin d’accès du package pour le processus appelant.<br/>                                                                                                        |
| [**GetCurrentPackagePath2**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagepath2)<br/>                                     | Obtient le chemin d’accès au package pour le processus appelant, avec l’option permettant de spécifier le type de dossier du package.<br/>                                                                                                        |
| [**GetPackageApplicationIds**](/windows/desktop/api/AppModel/nf-appmodel-getpackageapplicationids)<br/>                               | Obtient les ID des applications dans le package spécifié.<br/>                                                                                                        |
| [**GetPackageFamilyName**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefamilyname)<br/>                                       | Obtient le nom de la famille de packages pour le processus spécifié.<br/>                                                                                               |
| [**GetPackageFamilyNameFromToken**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefamilynamefromtoken)<br/>                     | Obtient le nom de la famille de packages pour le jeton spécifié.<br/>                                                                                                 |
| [**GetPackageFullName**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefullname)<br/>                                           | Obtient le nom complet du package pour le processus spécifié.<br/>                                                                                                 |
| [**GetPackageFullNameFromToken**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefullnamefromtoken)<br/>                         | Obtient le nom complet du package pour le jeton spécifié.<br/>                                                                                                   |
| [**GetPackageId**](/windows/desktop/api/AppModel/nf-appmodel-getpackageid)<br/>                                                       | Obtient l’identificateur de package (ID) pour le processus spécifié.<br/>                                                                                           |
| [**GetPackageInfo**](/windows/desktop/api/AppModel/nf-appmodel-getpackageinfo)<br/>                                                   | Obtient les informations de package pour le package spécifié.<br/>                                                                                               |
| [**GetPackageInfo2**](/windows/desktop/api/AppModel/nf-appmodel-getpackageinfo2)<br/>                                                   | Obtient les informations de package pour le package spécifié, avec l’option permettant de spécifier le type de dossier du package.<br/>                                                                                               |
| [**GetPackagePath**](/windows/desktop/api/AppModel/nf-appmodel-getpackagepath)<br/>                                                   | Obtient le chemin d’accès pour le package spécifié.<br/>                                                                                                              |
| [**GetPackagePathByFullName**](/windows/desktop/api/AppModel/nf-appmodel-getpackagepathbyfullname)<br/>                               | Obtient le chemin d’accès du package spécifié.<br/>                                                                                                               |
| [**GetPackagePathByFullName2**](/windows/desktop/api/AppModel/nf-appmodel-getpackagepathbyfullname2)<br/>                               | Obtient le chemin d’accès du package spécifié, avec l’option permettant de spécifier le type de dossier du package.<br/>                                                                                                               |
| [**GetPackagesByPackageFamily**](/windows/desktop/api/AppModel/nf-appmodel-getpackagesbypackagefamily)<br/>                           | Obtient les packages avec le nom de famille spécifié pour l’utilisateur actuel. <br/>                                                                               |
| [**GetStagedPackageOrigin**](/windows/desktop/api/AppModel/nf-appmodel-getstagedpackageorigin)<br/>                                   | Obtient l’origine du package spécifié.<br/>                                                                                                             |
| [**GetStagedPackagePathByFullName**](/windows/desktop/api/AppModel/nf-appmodel-getstagedpackagepathbyfullname)<br/>                   | Obtient le chemin d’accès du package intermédiaire spécifié.<br/>                                                                                                        |
| [**GetStagedPackagePathByFullName2**](/windows/desktop/api/AppModel/nf-appmodel-getstagedpackagepathbyfullname2)<br/>                   | Obtient le chemin d’accès du package intermédiaire spécifié, avec l’option permettant de spécifier le type de dossier du package.<br/>                                                                                                        |
| [**OpenPackageInfoByFullName**](/windows/desktop/api/AppModel/nf-appmodel-openpackageinfobyfullname)<br/>                             | Ouvre les informations de package du package spécifié.<br/>                                                                                               |
| [**PackageFamilyNameFromFullName**](/windows/desktop/api/AppModel/nf-appmodel-packagefamilynamefromfullname)<br/>                     | Obtient le nom de la famille de packages pour le nom complet du package spécifié.<br/>                                                                                     |
| [**PackageFamilyNameFromId**](/windows/desktop/api/AppModel/nf-appmodel-packagefamilynamefromid)<br/>                                 | Obtient le nom de la famille de packages pour l’identificateur de package spécifié.<br/>                                                                                    |
| [**PackageFullNameFromId**](/windows/desktop/api/AppModel/nf-appmodel-packagefullnamefromid)<br/>                                     | Obtient le nom complet du package pour l’identificateur de package (ID) spécifié.<br/>                                                                                 |
| [**PackageIdFromFullName**](/windows/desktop/api/AppModel/nf-appmodel-packageidfromfullname)<br/>                                     | Obtient l’identificateur de package (ID) pour le nom complet du package spécifié.<br/>                                                                                 |
| [**PackageNameAndPublisherIdFromFamilyName**](/windows/desktop/api/AppModel/nf-appmodel-packagenameandpublisheridfromfamilyname)<br/> | Obtient le nom du package et l’identificateur de l’éditeur (ID) pour le nom de la famille de packages spécifiée.<br/>                                                            |
| [**ParseApplicationUserModelId**](/windows/desktop/api/AppModel/nf-appmodel-parseapplicationusermodelid)<br/>                         | Déconstruit un [ID de modèle d’utilisateur d’application](appx-packaging-glossary.md) en fonction du nom de la famille de packages et de l’ID d’application relatif du package (Praid).<br/>      |
| [**PackageOrigin**](/windows/desktop/api/AppModel/ne-appmodel-packageorigin)<br/>                                                     | Spécifie l’origine d’un package. <br/>                                                                                                                   |
| [**Constantes d’identité**](identity-constants.md)<br/>                                           | Spécifie la longueur des chaînes pour les champs d’identité du package.<br/>                                                                                |
| [**Constantes de package**](package-constants.md)<br/>                                             | Spécifie la manière dont les packages doivent être traités.<br/>                                                                                                           |
| [**ID du PACKAGE \_**](/windows/desktop/api/AppModel/ns-appmodel-package_id)<br/>                                                          | Représente les informations d’identification du package, telles que le nom, la version et le serveur de publication.<br/>                                                                  |
| [**\_informations sur le package**](/windows/desktop/api/AppModel/ns-appmodel-package_info)<br/>                                                      | Représente des informations d’identification de package qui incluent l’identificateur de package, le nom complet et l’emplacement d’installation.<br/>                                  |
| [**VERSION du PACKAGE \_**](/windows/desktop/api/AppModel/ns-appmodel-package_version)<br/>                                                | Représente les informations de version du package.<br/>                                                                                                           |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Concepts**
</dt> <dt>

[Packages d’applications et déploiement](/previous-versions/windows/apps/hh464929(v=win.10))
</dt> <dt>

[Glossaire](appx-packaging-glossary.md)
</dt> <dt>

**Référence**
</dt> <dt>

[Schéma de manifeste du package de l’application](/uwp/schemas/appxpackage/appx-package-manifest)
</dt> <dt>

[API d’empaquetage](interfaces.md)
</dt> <dt>

[API de déploiement de packages](package-deployment-api.md)
</dt> </dl>

 

