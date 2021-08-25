---
title: Fichiers d’en-tête et de bibliothèque requis pour une application
description: Fichiers d’en-tête et de bibliothèque requis pour une application
ms.assetid: 922627d5-03a8-4b5b-be00-6f2c3500dd66
keywords:
- Windows Gestionnaire de périphériques de média, bibliothèques
- Gestionnaire de périphériques, bibliothèques
- Guide de programmation, bibliothèques
- applications de bureau, bibliothèques
- création d’applications Windows Media Gestionnaire de périphériques de bibliothèques
- libraries
- Windows Gestionnaire de périphériques de média, fichiers d’en-tête
- Gestionnaire de périphériques, fichiers d’en-tête
- Guide de programmation, fichiers d’en-tête
- applications de bureau, fichiers d’en-tête
- création d’applications Windows Media Gestionnaire de périphériques, fichiers d’en-tête
- fichiers d'en-tête
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b6630f4ff752b53ed69633d1e63a62093e4a4fbd16f65ccb1cc709aae120a07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863069"
---
# <a name="required-library-and-header-files-for-an-application"></a>Fichiers d’en-tête et de bibliothèque requis pour une application

cette section répertorie les bibliothèques, les fichiers d’en-tête ou les fichiers IDL que vous devez inclure pour développer une application ou un plug-in Windows Media Gestionnaire de périphériques. Comme mentionné dans la [compilation des fichiers IDL fournis avec le kit de développement logiciel (SDK](compiling-the-idl-files-supplied-with-the-sdk.md)), le kit de développement logiciel (SDK) contient à la fois des fichiers IDL et des fichiers d’en-tête prédéfinis, et votre application peut utiliser (Notez que certains fichiers d’en-tête n’ont pas de fichiers IDL correspondants et que vous ne pouvez pas les créer vous-même.) Si vous générez vos propres fichiers IDL, incluez les dépendances listées dans compilation des fichiers IDL fournis avec le kit de développement logiciel (SDK).

Toutes les applications n’ont pas besoin de tous les fichiers ; Lisez la description pour savoir si votre application a besoin d’un fichier.



| En-tête ou bibliothèque prédéfinie       | IDL équivalent                                | Description                                                                                                                                                                                                                                               |
|----------------------------------|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mssachlp. lib                     | aucun                                          | Requis par toutes les applications. contient des objets Windows Media Gestionnaire de périphériques.                                                                                                                                                                              |
| wmvcore. lib                      | aucun                                          | requis par les applications qui utilisent des objets ou des fonctions du kit de développement logiciel (SDK) Windows Media Format.                                                                                                                                                                          |
| Initguid. h                       | aucun (en-tête du kit de développement Platform SDK)                    | Requis par toutes les applications pour définir les valeurs **GUID** à l’aide du fichier mswmdm. h prédéfini. Vous devez inclure Initguid. h une fois et une seule fois dans votre projet. Cet en-tête redéfinit la macro **définir le \_ GUID** afin d’éviter les problèmes d’attribution de noms de **GUID** externes. |
| mmreg. h                          | aucun (en-tête du kit de développement Platform SDK)                    | requis par les applications qui font référence à différentes définitions de format de média Windows standard, telles que **WAVEFORMATEX**.                                                                                                                                      |
| mswmdm. h                         | WMDM. idlicomponentauthenticate. idl<br/> | Requis par toutes les applications. Définit toutes les interfaces d’application, ainsi que les structures, les métadonnées, les erreurs et d’autres constantes.                                                                                                                        |
| sac. h                            | aucun                                          | Requis par toutes les applications. Définit les protocoles SAC.                                                                                                                                                                                                      |
| scclient. h                       | aucun                                          | Requis par toutes les applications. Déclare la classe [CSecureChannelClient](csecurechannelclient-class.md) .                                                                                                                                                  |
| wmdmlog. hwmdmlog \_ i. c<br/> | Wmdmlog. idl                                   | Requis par les applications qui utilisent l’interface [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger) .                                                                                                                                                                       |
| wmdrmdeviceapp. h                 | WMDRMDeviceApp. idl                            | Requis par les applications ou les plug-ins qui mettent à jour des composants DRM ou des compteurs de jeux sur les appareils.                                                                                                                                                          |
| WMSDK. h                          | aucun (fourni par Windows Media Format SDK)   | requis pour les applications qui utilisent les méthodes du kit de développement logiciel (SDK) Windows Media Format.                                                                                                                                                                                      |
| MtpExt. h                         | aucun                                          | Requis pour les applications qui appellent [**IWMDMDevice3 ::D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) sur les appareils MTP. Définit différentes constantes et structures MTP standard.                                                                          |
| Key. c                            | aucun                                          | Définit une clé et un certificat auprès de Microsoft. la version fournie avec le kit de développement logiciel (SDK) comprend une clé factice de test qui permet d’utiliser des fichiers multimédias Windows protégés non DRM.                                                                                |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de programmation**](programming-guide.md)
</dt> </dl>

 

 





