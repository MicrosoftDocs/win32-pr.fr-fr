---
title: Détails du code
description: Cette section répertorie le code source de l’implémentation du composant fournisseur d’exemples ADSI. Toutes les références de code source dans ce document sont susceptibles d’être modifiées et sont disponibles dans l’exemple de répertoire de code inclus dans le kit de développement logiciel (SDK) ADSI.
ms.assetid: 207912e5-ac17-48c7-9536-981a8e92e8cf
ms.tgt_platform: multiple
keywords:
- Détails du code ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d959357f2cdd094b26cde4f649c3286389b8415
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031848"
---
# <a name="code-details"></a>Détails du code

Cette section répertorie le code source de l’implémentation du composant fournisseur d’exemples ADSI. Toutes les références de code source dans ce document sont susceptibles d’être modifiées et sont disponibles dans l’exemple de répertoire de code inclus dans le kit de développement logiciel (SDK) ADSI.

> [!Note]  
> Les [](/windows/desktop/api/Iads/nn-iads-iads) méthodes IADs **GETEX** et biais **ne sont pas** implémentées dans le composant fournisseur d’exemples ADSI. Autrement dit, le code qui implémente Active Directory objets qui héritent de **IADs** n’ont pas **de méthodes** **GETEX** et déconseillées. Cela comprend l’objet de classe de schéma qui prend en charge [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass), l’objet de propriété qui prend en charge [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty), l’objet générique Active Directory qui prend en charge les **IAD** et tout objet conteneur qui prend en charge [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer). En outre, les objets de syntaxe ne sont pas présents dans l’exemple de composant fournisseur. Toutefois, l’architecture ADSI requiert que les objets de syntaxe soient inclus dans l’objet conteneur de schéma, tout comme les objets de classe et de propriété de schéma.

 

Le tableau suivant répertorie les fichiers de code source inclus dans le répertoire de l’exemple de fournisseur dans le kit de développement logiciel (SDK) des interfaces de service Active Directory.



| Fichier de code source                 | Description                                                                                                                                                       |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [cclsobj. cpp](cclsobj-cpp.md)   | Routines d’objets de classe de schéma.                                                                                                                                     |
| [cdispmgr. cpp](cdispmgr-cpp.md) | Implémentation du gestionnaire de répartition.                                                                                                                                  |
| [cenumns. cpp](cenumns-cpp.md)   | Routines d’énumération d’espaces de noms.                                                                                                                                   |
| [cenumsch. cpp](cenumsch-cpp.md) | Routines d’énumération de schéma.                                                                                                                                      |
| [cenumobj. cpp](cenumobj-cpp.md) | Routines d’énumération d’objets génériques.                                                                                                                              |
| [cenumvar. cpp](cenumvar-cpp.md) | Implémentation de base pour les classes dérivées xxxEnumVariant.                                                                                                           |
| [cgenobj. cpp](cgenobj-cpp.md)   | Routines d’objets génériques.                                                                                                                                          |
| [cnamcf. cpp](cnamcf-cpp.md)     | Routines de fabrique de classes d’espace de noms.                                                                                                                                 |
| [cnamesp. cpp](cnamesp-cpp.md)   | Routines d’objets d’espace de noms.                                                                                                                                        |
| [Common. cpp](common-cpp.md)     | Code commun à tous les objets de fournisseur.                                                                                                                              |
| [Core. cpp](core-cpp.md)         | Implémentations pour les propriétés’Core’partagées par tous les objets Active Directory.                                                                                     |
| [cProps. cpp](cprops-cpp.md)     | Fonctionnalités du cache de propriétés.                                                                                                                                          |
| [cprov. cpp](cprov-cpp.md)       | Routines d’objets fournisseurs de niveau supérieur.                                                                                                                               |
| [cprovcf. cpp](cprovcf-cpp.md)   | Routines de fabrique de classe d’objet de niveau supérieur.                                                                                                                 |
| [cprpobj. cpp](cprpobj-cpp.md)   | Routines d’objets de propriété.                                                                                                                                         |
| [cschobj. cpp](cschobj-cpp.md)   | Routines d’objet de schéma.                                                                                                                                           |
| [getobj. cpp](getobj-cpp.md)     | Fonction GetObject.                                                                                                                                                |
| [Globals. cpp](globals-cpp.md)   | Exemples de composants du fournisseur ADSI.                                                                                                                          |
| [Guid. cpp](guid-cpp.md)         | Exemples de CLSID du composant fournisseur et LIBIDs.                                                                                                                     |
| [LibMain. cpp](libmain-cpp.md)   | LibMain pour adssmp.dll.                                                                                                                                           |
| [Memory. cpp](memory-cpp.md)     | Exemples de routines de gestion de la mémoire du composant fournisseur.                                                                                                            |
| [Pack. cpp](pack-cpp.md)         | Exemple de composant fournisseur/décompresser des données dans des VARIANTEs.                                                                                                          |
| [parse. cpp](parse-cpp.md)       | Analyse du chemin d’accès pour l’exemple d’espace de noms du composant fournisseur.                                                                                                            |
| [Property. cpp](property-cpp.md) | Obtient et place les propriétés par nom.                                                                                                                                   |
| [Object. cpp](object-cpp.md)     | Exemple de code de type d’objet de composant fournisseur pour le filtrage.                                                                                                   |
| [regdsapi. cpp](regdsapi-cpp.md) | Exemple d’API du service d’annuaire du Registre du composant fournisseur.                                                                                                       |
| smpoper. cpp                      | Routines de conversion de données.                                                                                                                                         |
| [stdfact. cpp](stdfact-cpp.md)   | Implémentation de [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) standard.                                                                                                  |
| adssmp. inf                       | Exemple de données de registre de magasin de données d’annuaire. Pour plus d’informations, consultez [installation du composant de l’exemple de fournisseur](installing-the-example-provider-component.md). |



 

 

 