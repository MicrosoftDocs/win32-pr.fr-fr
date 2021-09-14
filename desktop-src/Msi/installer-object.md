---
description: Un objet installer doit être initialement créé pour charger la prise en charge d’Automation qui est nécessaire pour que COM accède aux fonctions du programme d’installation. Cet objet fournit des wrappers pour créer les objets de niveau supérieur et accéder à leurs méthodes.
ms.assetid: fefc3e39-073e-4869-86b7-27d20a3b337b
title: Objet installer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4afddcce55a739ad322be10c736a6e9119f5c9eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012140"
---
# <a name="installer-object"></a>Objet installer

Un objet **installer** doit être initialement créé pour charger la prise en charge d’Automation qui est nécessaire pour que com accède aux fonctions du programme d’installation. Cet objet fournit des wrappers pour créer les objets de niveau supérieur et accéder à leurs méthodes.

Vous pouvez créer l’objet **installer** à partir du ProgID « windowsinstaller. installer ».

## <a name="members"></a>Membres

L’objet **installer** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **installer** possède ces méthodes.



| Méthode                                                                   | Description                                                                                                                                                                                     |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddSource**](installer-addsource.md)                                 | Ajoute une source à la liste des sources réseau valides dans la liste de ressources réseau.<br/>                                                                                                                |
| [**AdvertiseProduct**](installer-advertiseproduct.md)                   | Publie un package d’installation.<br/>                                                                                                                                                  |
| [**AdvertiseScript**](installer-advertisescript.md)                     | Publie un package d’installation. <br/>                                                                                                                                                 |
| [**ApplyMultiplePatches**](installer-applymultiplepatches.md)           | Applique un ou plusieurs correctifs aux produits éligibles pour recevoir le correctif. Définit la propriété [**patch**](patch.md) sur le chemin d’accès des packages de correctifs fournis.<br/>                          |
| [**ApplyPatch**](installer-applypatch.md)                               | Appelle une installation et définit la propriété [**patch**](patch.md) sur le chemin d’accès du package correctif pour chaque produit indiqué par le package correctif comme pouvant recevoir le correctif.<br/> |
| [**ClearSourceList**](installer-clearsourcelist.md)                     | Supprime toutes les sources réseau de la source d’alimentation.<br/>                                                                                                                                     |
| [**CollectUserInfo**](installer-collectuserinfo.md)                     | Appelle une séquence de l’Assistant de l’interface utilisateur qui collecte et stocke les informations utilisateur et le code du produit.<br/>                                                                        |
| [**ConfigureFeature**](installer-configurefeature.md)                   | Configure l’état installé d’une fonctionnalité de produit.<br/>                                                                                                                                 |
| [**ConfigureProduct**](installer-configureproduct.md)                   | Installe ou désinstalle un produit.<br/>                                                                                                                                                    |
| [**CreateAdvertiseScript**](installer-createadvertisescript.md)         | Génère un script de publication.<br/>                                                                                                                                                       |
| [**CreateRecord**](installer-createrecord.md)                           | Retourne un nouvel objet [**Record**](record-object.md) avec le nombre demandé de champs.<br/>                                                                                            |
| [**EnableLog**](installer-enablelog.md)                                 | Active la journalisation du type de message sélectionné pour toutes les sessions d’installation suivantes dans l’espace de processus actuel.<br/>                                                                  |
| [**ExtractPatchXMLData**](installer-extractpatchxmldata.md)             | Extrait des informations d’un correctif sous la forme d’une chaîne XML.<br/>                                                                                                                                  |
| [**FileHash**](installer-filehash.md)                                   | Prend le chemin d’accès à un fichier et retourne un hachage 128 bits de ce fichier.<br/>                                                                                                                    |
| [**FileSignatureInfo**](installer-filesignatureinfo.md)                 | Prend le chemin d’accès à un fichier et retourne un **SAFEARRAY** d’octets qui représente le hachage ou le certificat encodé.<br/>                                                                   |
| [**FileSize**](installer-filesize.md)                                   | Retourne la taille du fichier spécifié.<br/>                                                                                                                                              |
| [**FileVersion**](installer-fileversion.md)                             | Retourne la chaîne de version ou la chaîne de langue du chemin d’accès spécifié.<br/>                                                                                                                 |
| [**ForceSourceListResolution**](installer-forcesourcelistresolution.md) | Oblige le programme d’installation à rechercher dans la liste source une source de produit valide la prochaine fois qu’une source est requise.<br/>                                                                        |
| [**InstallProduct**](installer-installproduct.md)                       | Ouvre un package d’installation et Initialise une session d’installation.<br/>                                                                                                                  |
| [**LastErrorRecord**](installer-lasterrorrecord.md)                     | Retourne un objet [**Record**](record-object.md) qui contient des paramètres d’erreur pour l’erreur la plus récente de la fonction qui a produit l’enregistrement d’erreur.<br/>                          |
| [**OpenDatabase**](installer-opendatabase.md)                           | Ouvre une base de données existante ou en crée une nouvelle.<br/>                                                                                                                                     |
| [**OpenPackage**](installer-openpackage.md)                             | Ouvre un package d’installation à utiliser avec les fonctions qui accèdent à la base de données du produit et au moteur d’installation.<br/>                                                                               |
| [**OpenProduct**](installer-openproduct.md)                             | Ouvre un package d’installation pour un produit installé à l’aide du code de produit.<br/>                                                                                                          |
| [**ProvideAssembly**](installer-provideassembly.md)                     | Retourne le chemin d’accès installé d’un assembly.<br/>                                                                                                                                           |
| [**ProvideComponent**](installer-providecomponent.md)                   | Retourne le chemin d’accès complet au composant et effectue toute installation nécessaire.<br/>                                                                                                             |
| [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) | Retourne le chemin d’accès complet au composant et effectue toute installation nécessaire.<br/>                                                                                                             |
| [**RegistryValue**](installer-registryvalue.md)                         | Lit les informations relatives à une clé de Registre spécifiée de valeur.<br/>                                                                                                                           |
| [**ReinstallFeature**](installer-reinstallfeature.md)                   | Réinstalle les fonctionnalités ou corrige les problèmes liés aux fonctionnalités installées.<br/>                                                                                                                    |
| [**ReinstallProduct**](installer-reinstallproduct.md)                   | Réinstalle un produit ou corrige les problèmes d’installation dans un produit installé.<br/>                                                                                                      |
| [**RemovePatches**](installer-removepatches.md)                         | Supprime un ou plusieurs correctifs pour les produits éligibles pour recevoir le correctif. <br/>                                                                                                              |
| [**UseFeature**](installer-usefeature.md)                               | Incrémente le nombre d’utilisations d’une fonctionnalité particulière et retourne l’état d’installation de cette fonctionnalité.<br/>                                                                             |



 

### <a name="properties"></a>Propriétés

L’objet **installer** possède ces propriétés.



| Propriété                                                                    | Type d’accès           | Description                                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClientsEx**](installer-components.md)<br/>                        |                       | Retourne un objet [**RecordList**](recordlist-object.md) qui répertorie les produits qui utilisent un composant installé spécifié.<br/> **[Windows Installer 4,5 et versions antérieures](not-supported-in-windows-installer-4-5.md):** Non pris en charge.<br/>       |
| [**ComponentClients**](installer-componentclients.md)<br/>           |                       | Retourne un objet [**StringList**](stringlist-object.md) énumérant l’ensemble des clients d’un composant spécifié.<br/>                                                                                                                           |
| [**ComponentPath**](installer-componentpath.md)<br/>                 |                       | Retourne le chemin d’accès complet à un composant installé.<br/>                                                                                                                                                                                            |
| [**ComponentPathEx**](installer-componentpathex.md)<br/>             |                       | Retourne un objet [**RecordList**](recordlist-object.md) qui donne le chemin d’accès complet d’un composant installé spécifié. <br/> **[Windows Installer 4,5 et versions antérieures](not-supported-in-windows-installer-4-5.md):** Non pris en charge.<br/>       |
| [**ComponentQualifiers**](installer-componentqualifiers.md)<br/>     |                       | Retourne un objet [**StringList**](stringlist-object.md) énumérant l’ensemble des qualificateurs inscrits pour le composant spécifié.<br/>                                                                                                          |
| [**Composants**](installer-components.md)<br/>                       |                       | Retourne un objet [**StringList**](stringlist-object.md) énumérant l’ensemble des composants installés pour tous les produits.<br/>                                                                                                                      |
| [**ComponentsEx**](installer-componentsex.md)<br/>                   |                       | Retourne un objet [**RecordList**](recordlist-object.md) qui répertorie les composants installés.<br/> **[Windows Installer 4,5 et versions antérieures](not-supported-in-windows-installer-4-5.md):** Non pris en charge.<br/>                                    |
| [**Environnement**](installer-environment.md)<br/>                     | Lecture/écriture<br/> | Valeur de chaîne pour une variable d’environnement du processus en cours.<br/>                                                                                                                                                                        |
| [**FeatureParent**](installer-featureparent.md)<br/>                 |                       | Spécifie la fonctionnalité parente d’une fonctionnalité.<br/>                                                                                                                                                                                                  |
| [**Éléments**](installer-features.md)<br/>                           |                       | Retourne un objet [**StringList**](stringlist-object.md) énumérant l’ensemble des fonctionnalités publiées pour le produit spécifié.<br/>                                                                                                               |
| [**FeatureState**](installer-featurestate.md)<br/>                   |                       | Retourne l’état installé d’une fonctionnalité.<br/>                                                                                                                                                                                                   |
| [**FeatureUsageCount**](installer-featureusagecount.md)<br/>         |                       | Retourne le nombre de fois que la fonctionnalité a été utilisée.<br/>                                                                                                                                                                                 |
| [**FeatureUsageDate**](installer-featureusagedate.md)<br/>           |                       | Retourne la date de la dernière utilisation de la fonctionnalité spécifiée.<br/>                                                                                                                                                                                  |
| [**FileAttributes**](installer-fileattributes.md)<br/>               |                       | Retourne un nombre qui représente les attributs de fichier combinés pour le chemin d’accès désigné à un fichier ou un dossier.<br/>                                                                                                                                  |
| [**Correctifs**](installer-patches.md)<br/>                             |                       | Retourne un objet [**StringList**](stringlist-object.md) qui contient tous les correctifs appliqués au produit.<br/>                                                                                                                              |
| [**PatchesEx**](installer-patchesex.md)<br/>                         |                       | Énumère une collection d’objets [**patch**](patch-object.md) .<br/>                                                                                                                                                                           |
| [**PatchFiles**](installer-patchfiles.md)<br/>                       |                       | Retourne un objet [**StringList**](stringlist-object.md) qui contient une liste de fichiers qui peuvent être mis à jour par la liste de correctifs fournie.<br/>                                                                                                 |
| [**PatchInfo**](installer-patchinfo.md)<br/>                         |                       | Retourne des informations sur un correctif.<br/>                                                                                                                                                                                                          |
| [**PatchTransforms**](installer-patchtransforms.md)<br/>             |                       | Retourne la liste délimitée par des points-virgules des transformations qui se trouvent dans le package de correctifs spécifié et appliquées au produit spécifié.<br/>                                                                                                            |
| [**ProductElevated**](installer-productelevated.md)<br/>             |                       | Retourne la valeur true si le produit est managé ou false si le produit n’est pas géré.<br/>                                                                                                                                                              |
| [**ProductInfo**](installer-productinfo.md)<br/>                     |                       | Retourne la valeur de l’attribut spécifié pour un produit installé ou publié.<br/>                                                                                                                                                         |
| [**ProductInfoFromScript**](installer-productinfofromscript.md)<br/> |                       | Retourne la valeur de l’attribut spécifié qui est stocké dans un script de publication.<br/>                                                                                                                                                         |
| [**Produits**](installer-products.md)<br/>                           |                       | Retourne un objet [**StringList**](stringlist-object.md) énumérant l’ensemble de tous les produits installés ou publiés pour l’utilisateur et l’ordinateur actuels. <br/>                                                                                     |
| [**ProductsEx**](installer-productsex.md)<br/>                       |                       | Énumère une collection d’objets [**Product**](product-object.md) .<br/>                                                                                                                                                                       |
| [**ProductState**](installer-productstate-property.md)<br/>          |                       | Retourne les informations sur l’état d’installation d’un produit.<br/>                                                                                                                                                                                        |
| [**QualifierDescription**](installer-qualifierdescription.md)<br/>   |                       | Retourne une chaîne de texte qui décrit le composant qualifié.<br/>                                                                                                                                                                               |
| [**RelatedProducts**](installer-relatedproducts.md)<br/>             |                       | Retourne un objet [**StringList**](stringlist-object.md) énumérant l’ensemble de tous les produits installés ou publiés pour l’utilisateur et l’ordinateur actuels avec une propriété [**UpgradeCode**](upgradecode.md) spécifiée dans leur table de propriétés.<br/> |
| [**ShortcutTarget**](installer-shortcuttarget.md)<br/>               |                       | Examine un raccourci et retourne son produit, son nom de fonctionnalité et son composant, le cas échéant.<br/>                                                                                                                                                       |
| [**SummaryInformation**](installer-summaryinformation.md)<br/>       |                       | Retourne un objet [**SummaryInfo**](summaryinfo-object.md) qui peut être utilisé pour examiner, mettre à jour et ajouter des propriétés au flux d’informations de synthèse d’un package ou d’une transformation.<br/>                                                              |
| [**UILevel**](installer-uilevel.md)<br/>                             | Lecture/écriture<br/> | Indique le type d’interface utilisateur à utiliser lors de l’ouverture et du traitement des packages suivants dans l’espace de processus actuel.<br/>                                                                                                           |
| [**Version**](installer-version.md)<br/>                             |                       | retourne la représentation sous forme de chaîne de la version actuelle de Windows Installer.<br/>                                                                                                                                                              |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation de l’interface d’automatisation](using-the-automation-interface.md)
</dt> <dt>

[Windows Exemples de scripts d’installation](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




