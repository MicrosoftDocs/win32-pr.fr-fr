---
title: Compilation des fichiers IDL fournis avec le kit de développement logiciel (SDK)
description: Compilation des fichiers IDL fournis avec le kit de développement logiciel (SDK)
ms.assetid: 718528eb-6ac4-466d-8dfd-d6f2b6c30303
keywords:
- Windows Media Gestionnaire de périphériques, fichiers IDL
- Gestionnaire de périphériques, fichiers IDL
- applications de bureau, fichiers IDL
- fournisseurs de services, fichiers IDL
- Guide de programmation, fichiers IDL
- fichiers IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87e24eec21a481de4603392942b40013ec55086c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513679"
---
# <a name="compiling-the-idl-files-supplied-with-the-sdk"></a>Compilation des fichiers IDL fournis avec le kit de développement logiciel (SDK)

Le kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques comprend les fichiers d’en-tête et les fichiers IDL source pour la plupart de ces fichiers d’en-tête. Les fichiers d’en-tête se trouvent dans le \\ \\ dossier Inc dans le chemin d’installation du kit de développement logiciel. Les fichiers IDL se trouvent dans le \\ \\ dossier IDL.

Les en-têtes précompilés sont bien plus simples à utiliser, et plusieurs fichiers IDL sont combinés en un seul en-tête fourni. Toutefois, si vous décidez de traiter vos propres fichiers d’en-tête à partir des fichiers IDL fournis, cette rubrique décrit les fichiers IDL qui créent les fichiers d’en-tête et décrit également les dépendances de chaque fichier IDL.

**IDL équivalent et fichiers d’en-tête fournis**



| **MIDL**                                                                                            | **En-tête fourni équivalent**               | **Description**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMDM. idl<br/> WMSP. idl<br/> WMSCP. idl<br/> icomponentauthenticate. idl<br/> | Mswmdm. h                                     | Les quatre fichiers IDL sont inclus dans cet en-tête fourni unique.<br/> **WMDM. idl** définit toutes les interfaces d’application et les structures, les constantes et les codes d’erreur requis.<br/> **Wmsp. idl** définit toutes les interfaces du fournisseur de services.<br/> **WMSCP. idl** définit toutes les interfaces, les valeurs GUID et les constantes requises par les fournisseurs de contenu sécurisé.<br/> **icomponentauthenticate. idl** définit l’interface [**icomponentauthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .<br/> |
| Wmdmlog. idl                                                                                        | Wmdmlog. h<br/> wmdmlog \_ i. c<br/> | Définit les interfaces de journalisation.<br/> Les deux fichiers d’en-tête fournis doivent être utilisés, plutôt que simplement le fichier. h, en raison d’un problème avec le fichier IDL.<br/>                                                                                                                                                                                                                                                                                                                                                |
| WMDRMDeviceApp. idl                                                                                 | Wmdrmdeviceapp. h                             | Définit les interfaces [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) et [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) utilisées par les applications qui mettent à jour la DRM sur les appareils ou le nombre de jeux de lecture sur les appareils.                                                                                                                                                                                                                                                                                                                 |



 

**Dépendances IDL**

Plusieurs des fichiers IDL fournis ont des dépendances de Build. Si vous envisagez de compiler les fichiers IDL vous-même, vous devez traiter ces dépendances externes dans l’ordre indiqué dans le tableau suivant.



|                            |                                                                                  |
|----------------------------|----------------------------------------------------------------------------------|
| **MIDL**                    | **Dépendances**                                                                 |
| icomponentauthenticate. idl | Importez « oaidl. idl »;<br/> \#inclure « icomponentauthenticate. idl »<br/> |
| WMDM. idl                   | Aucune dépendance externe                                                         |
| WmdmLog. idl                | Aucune dépendance externe                                                         |
| WMDRMDeviceApp. idl         | Aucune dépendance externe                                                         |
| WMSCP. idl                  | \#inclure « WMDRMDeviceApp. idl »<br/> \#inclure « WMSP. idl »<br/>        |
| WMSP. idl                   | \#inclure « WMDM. idl »                                                             |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Tâches communes aux applications et aux fournisseurs de services**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 





