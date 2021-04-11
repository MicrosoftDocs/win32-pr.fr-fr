---
title: Fichiers de code pour l’exemple de fournisseur source
description: Fichiers de code pour l’exemple de fournisseur source
ms.assetid: bd6bfc98-a805-4e04-8a80-7af42ed3dbef
keywords:
- Gestionnaire de périphériques Windows Media, exemples
- Gestionnaire de périphériques, exemples
- Windows Media Gestionnaire de périphériques, exemple de fournisseur de services
- Gestionnaire de périphériques, exemple de fournisseur de services
- fournisseurs de services, exemples
- exemples, fournisseurs de services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64b8af4b34310ae183ce55b2e52d3dd346dc6665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100725"
---
# <a name="code-files-for-the-source-provider-sample"></a>Fichiers de code pour l’exemple de fournisseur source

L’exemple de projet de fournisseur source comprend les fichiers de code source suivants, avec des en-têtes associés :



| Fichier                   | Description                                                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| hdsppch. cpp            | Comprend des fichiers ATL standard.                                                                                                                                                                                    |
| Key. c                  | Contient une clé d’authentification factice.                                                                                                                                                                            |
| loghelp. cpp            | Contient des fonctions qui journalisent l’activité et les erreurs à l’aide de la classe **WMDMLogger** , qui est implémentée dans le fichier système WMDMLOG.dll.                                                                         |
| MDServiceProvider. cpp  | Implémente une classe, CMDServiceProvider, qui implémente les interfaces [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider) et IComponentAuthenticate.                                                             |
| MDSP. cpp               | Point d’entrée et code d’enregistrement de la DLL.                                                                                                                                                                          |
| MDSPDevice. cpp         | Implémente une classe, CMDSPDevice, qui implémente les interfaces [**IMDSPDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2), [**IMDSPDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol)et **ISpecifyPropertyPages** .                          |
| MDSPEnumDevice. cpp     | Implémente une classe, CMDSPEnumDevice, qui implémente l’interface [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice) .                                                                                                  |
| MDSPEnumStorage. cpp    | Implémente une classe, CMDSPEnumStorage, qui implémente l’interface [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage) .                                                                                               |
| MDSPStorage. cpp        | Implémente une classe, CMDSPStorage, qui implémente les interfaces [**IMDSPStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2), [**IMDSPObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo)et [**IMDSPObject**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject) .                    |
| MDSPStorageGlobals. cpp | Implémente une classe, CMDSPStorageGlobals, qui implémente l’interface [**IMDSPStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals) .                                                                                      |
| MDSPutil. cpp           | Contient diverses fonctions utilitaires pour la gestion des appareils et des fichiers.                                                                                                                                              |
| PropPage. cpp           | Implémente une classe, CPropPage, qui hérite des classes ATL **IPropertyPageImpl** (pour implémenter IPropertyPage) et **CDialogImpl**, qui hérite de la classe ATL CDialogImpl (pour gérer les fenêtres et les messages). |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Exemple de fournisseur de services**](sample-service-provider.md)
</dt> </dl>

 

 




