---
title: Fichiers d’en-tête et de bibliothèque requis pour une application
description: Fichiers d’en-tête et de bibliothèque requis pour une application
ms.assetid: 922627d5-03a8-4b5b-be00-6f2c3500dd66
keywords:
- Windows Media Gestionnaire de périphériques, bibliothèques
- Gestionnaire de périphériques, bibliothèques
- Guide de programmation, bibliothèques
- applications de bureau, bibliothèques
- création d’applications Windows Media Gestionnaire de périphériques, de bibliothèques
- libraries
- Windows Media Gestionnaire de périphériques, fichiers d’en-tête
- Gestionnaire de périphériques, fichiers d’en-tête
- Guide de programmation, fichiers d’en-tête
- applications de bureau, fichiers d’en-tête
- création d’applications Windows Media Gestionnaire de périphériques, de fichiers d’en-tête
- fichiers d'en-tête
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a4a8a04ee6c3fe603d52139e83f81a49d78dc45
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029339"
---
# <a name="required-library-and-header-files-for-an-application"></a>Fichiers d’en-tête et de bibliothèque requis pour une application

Cette section répertorie les bibliothèques, les fichiers d’en-tête ou les fichiers IDL que vous devrez inclure pour développer une application ou un plug-in Windows Media Gestionnaire de périphériques. Comme mentionné dans la [compilation des fichiers IDL fournis avec le kit de développement logiciel (SDK](compiling-the-idl-files-supplied-with-the-sdk.md)), le kit de développement logiciel (SDK) contient à la fois des fichiers IDL et des fichiers d’en-tête prédéfinis, et votre application peut utiliser (Notez que certains fichiers d’en-tête n’ont pas de fichiers IDL correspondants et que vous ne pouvez pas les créer vous-même.) Si vous générez vos propres fichiers IDL, incluez les dépendances listées dans compilation des fichiers IDL fournis avec le kit de développement logiciel (SDK).

Toutes les applications n’ont pas besoin de tous les fichiers ; Lisez la description pour savoir si votre application a besoin d’un fichier.



| En-tête ou bibliothèque prédéfinie       | IDL équivalent                                | Description                                                                                                                                                                                                                                               |
|----------------------------------|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mssachlp. lib                     | aucun                                          | Requis par toutes les applications. Contient les objets Windows Media Gestionnaire de périphériques.                                                                                                                                                                              |
| wmvcore. lib                      | aucun                                          | Requis par les applications qui utilisent les objets ou les fonctions du kit de développement logiciel (SDK) du format Windows Media.                                                                                                                                                                          |
| Initguid. h                       | aucun (en-tête du kit de développement Platform SDK)                    | Requis par toutes les applications pour définir les valeurs **GUID** à l’aide du fichier mswmdm. h prédéfini. Vous devez inclure Initguid. h une fois et une seule fois dans votre projet. Cet en-tête redéfinit la macro **définir le \_ GUID** afin d’éviter les problèmes d’attribution de noms de **GUID** externes. |
| mmreg. h                          | aucun (en-tête du kit de développement Platform SDK)                    | Requis par les applications qui font référence à différentes définitions de format Windows Media standard, telles que **WAVEFORMATEX**.                                                                                                                                      |
| mswmdm. h                         | WMDM. idlicomponentauthenticate. idl<br/> | Requis par toutes les applications. Définit toutes les interfaces d’application, ainsi que les structures, les métadonnées, les erreurs et d’autres constantes.                                                                                                                        |
| sac. h                            | aucun                                          | Requis par toutes les applications. Définit les protocoles SAC.                                                                                                                                                                                                      |
| scclient. h                       | aucun                                          | Requis par toutes les applications. Déclare la classe [CSecureChannelClient](csecurechannelclient-class.md) .                                                                                                                                                  |
| wmdmlog. hwmdmlog \_ i. c<br/> | Wmdmlog. idl                                   | Requis par les applications qui utilisent l’interface [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger) .                                                                                                                                                                       |
| wmdrmdeviceapp. h                 | WMDRMDeviceApp. idl                            | Requis par les applications ou les plug-ins qui mettent à jour des composants DRM ou des compteurs de jeux sur les appareils.                                                                                                                                                          |
| WMSDK. h                          | aucun (fourni par le kit de développement logiciel (SDK) Windows Media Format)   | Requis pour les applications qui utilisent les méthodes du kit de développement logiciel (SDK) du format Windows Media.                                                                                                                                                                                      |
| MtpExt. h                         | aucun                                          | Requis pour les applications qui appellent [**IWMDMDevice3 ::D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) sur les appareils MTP. Définit différentes constantes et structures MTP standard.                                                                          |
| Key. c                            | aucun                                          | Définit une clé et un certificat auprès de Microsoft. La version fournie avec le kit de développement logiciel (SDK) comprend une clé factice de test qui permet d’utiliser des fichiers Windows Media protégés non DRM.                                                                                |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de programmation**](programming-guide.md)
</dt> </dl>

 

 





