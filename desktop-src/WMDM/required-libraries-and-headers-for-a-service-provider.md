---
title: Bibliothèques et en-têtes requis pour un fournisseur de services
description: Bibliothèques et en-têtes requis pour un fournisseur de services
ms.assetid: 13ef830d-c1cf-4e4c-8fbd-20b5c38b9208
keywords:
- Windows Media Gestionnaire de périphériques, bibliothèques
- Gestionnaire de périphériques, bibliothèques
- Guide de programmation, bibliothèques
- fournisseurs de services, bibliothèques
- création de fournisseurs de services, bibliothèques
- libraries
- Windows Media Gestionnaire de périphériques, fichiers d’en-tête
- Gestionnaire de périphériques, fichiers d’en-tête
- Guide de programmation, fichiers d’en-tête
- fournisseurs de services, fichiers d’en-tête
- création de fournisseurs de services, fichiers d’en-tête
- fichiers d'en-tête
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b987d389216a3349c6797517b48c03bbb4d0f1eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310226"
---
# <a name="required-libraries-and-headers-for-a-service-provider"></a>Bibliothèques et en-têtes requis pour un fournisseur de services

Cette section répertorie les bibliothèques, les fichiers d’en-tête ou les fichiers IDL que vous devrez inclure pour développer une application ou un plug-in Windows Media Gestionnaire de périphériques. Comme mentionné dans la [compilation des fichiers IDL fournis avec le kit de développement logiciel (SDK](compiling-the-idl-files-supplied-with-the-sdk.md)), le kit de développement logiciel (SDK) contient à la fois des fichiers IDL et des fichiers d’en-tête prédéfinis, et votre application peut utiliser (Notez que certains fichiers d’en-tête n’ont pas de fichiers IDL correspondants et que vous ne pouvez pas les créer vous-même.) Si vous générez vos propres fichiers IDL, incluez les dépendances listées dans compilation des fichiers IDL fournis avec le kit de développement logiciel (SDK).

Toutes les applications n’ont pas besoin de tous les fichiers ; Lisez la description pour savoir si votre application a besoin d’un fichier.



| En-tête ou bibliothèque prédéfinie       | IDL équivalent                                                                | Description                                                                                                                                                                                                                                                    |
|----------------------------------|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mssachlp. lib                     | aucun                                                                          | Requis par tous les fournisseurs de services. Définit les objets Windows Media Gestionnaire de périphériques.                                                                                                                                                                               |
| Initguid. h                       | aucun (en-tête du kit de développement Platform SDK)                                                    | Requis par tous les fournisseurs de services pour définir les valeurs **GUID** à l’aide du fichier mswmdm. h prédéfini. Vous devez inclure Initguid. h une fois et une seule fois dans votre projet. Cet en-tête redéfinit la macro **définir le \_ GUID** afin d’éviter les problèmes d’attribution de noms de **GUID** externes. |
| mswmdm. h                         | WMDM. idl<br/> WMSP. idl<br/> icomponentauthenticate. idl<br/> | Requis par tous les fournisseurs de services. Définit toutes les interfaces, les structures, les métadonnées, les codes d’erreur et d’autres constantes du fournisseur de services.                                                                                                                        |
| sac. h                            | aucun                                                                          | Requis par tous les fournisseurs de services. Définit les protocoles SAC.                                                                                                                                                                                                      |
| SCServer. h                       | aucun                                                                          | Requis par tous les fournisseurs de services. Déclare la classe [CSecureChannelServer](csecurechannelserver-class.md) .                                                                                                                                                  |
| wmdmlog. hwmdmlog \_ i. c<br/> | Wmdmlog. idl                                                                   | Requis par les fournisseurs de services qui utilisent l’interface [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger) .                                                                                                                                                                       |
| WMSDK. h                          | aucun (fourni par le kit de développement logiciel (SDK) Windows Media Format)                                   | Requis pour les fournisseurs de services qui utilisent les méthodes du kit de développement logiciel (SDK) du format Windows Media.                                                                                                                                                                                      |
| wmvcore. lib                      | aucun                                                                          | Requis par les fournisseurs de services qui utilisent les objets ou les fonctions du kit de développement logiciel (SDK) du format Windows Media.                                                                                                                                                                          |
| mmreg. h                          | aucun (en-tête du kit de développement Platform SDK)                                                    | Requis par les fournisseurs de services qui font référence à différentes définitions de format Windows Media standard, telles que **WAVEFORMATEX**.                                                                                                                                      |
| MtpExt. h                         | aucun                                                                          | Requis pour les fournisseurs de services qui gèrent [**IMDSPDevice3 ::D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice3-deviceiocontrol) sur les appareils MTP. Définit différentes constantes et structures MTP standard.                                                                        |
| Key. c                            | aucun                                                                          | Définit une clé et un certificat auprès de Microsoft. La version fournie avec le kit de développement logiciel (SDK) comprend une clé factice de test qui permet d’utiliser des fichiers Windows Media protégés non DRM.                                                                                     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création d’un fournisseur de services**](creating-a-service-provider.md)
</dt> </dl>

 

 





