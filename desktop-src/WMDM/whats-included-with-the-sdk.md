---
title: Éléments inclus dans le kit de développement logiciel (SDK)
description: Éléments inclus dans le kit de développement logiciel (SDK)
ms.assetid: c17de30b-d4b4-4698-accf-721b6c267769
keywords:
- Windows Gestionnaire de périphériques de média, kit de développement logiciel (SDK)
- Gestionnaire de périphériques, kit de développement logiciel (SDK)
- Windows SDK Media Gestionnaire de périphériques
- SDK Gestionnaire de périphériques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36e621ac4de7fee296bf9d2c3ffb4e1d357824510b37a6ded73efd66b91f38d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004899"
---
# <a name="whats-included-with-the-sdk"></a>Éléments inclus dans le kit de développement logiciel (SDK)

le tableau suivant décrit le contenu du kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques. Tous les fichiers ou dossiers sont décrits par rapport au chemin d’installation du kit de développement logiciel (SDK) racine.



| Fichier                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMDM\\                     | dossier de niveau supérieur pour le kit de développement logiciel (SDK) Gestionnaire de périphériques Windows Media. Ce dossier comprend le makefile pour la génération de tous les exemples d’applications.                                                                                                                                                                                                                                                                                                              |
| MIDL\\                      | dossier qui contient tous les fichiers IDL requis pour générer les en-têtes nécessaires pour Windows méthodes de Gestionnaire de périphériques de média. Toutefois, au lieu d’utiliser ces fichiers, vous pouvez utiliser les fichiers d’en-tête fournis dans le \\ dossier Inc.<br/> Pour afficher la liste de ces fichiers IDL et savoir quels fichiers d’en-tête sont générés à partir des fichiers IDL, consultez compilation des fichiers [IDL fournis avec le kit de développement logiciel (SDK)](compiling-the-idl-files-supplied-with-the-sdk.md).<br/> |
| Inc \\ ....<br/>       | Dossier qui comprend tous les en-têtes qui définissent les interfaces et les types de données dans ce kit de développement logiciel (SDK).                                                                                                                                                                                                                                                                                                                                                         |
| mswmdm. h                   | Définit toutes les interfaces d’application, les interfaces de fournisseur de services, les interfaces de fournisseur de contenu sécurisé, les codes d’erreur, les constantes, les structures et l’interface [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .                                                                                                                                                                                                                            |
| mswmdm \_ i. c                | Définit l’interface [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) .                                                                                                                                                                                                                                                                                                                                                                               |
| MtpExt. h                   | Définit les structures spécifiques à MTP requises pour les applications appelant [**IWMDMDevice3 ::D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol).                                                                                                                                                                                                                                                                                                            |
| Resource. h                 | Définit différentes constantes de ressource utilisées par les exemples du kit de développement logiciel (SDK).                                                                                                                                                                                                                                                                                                                                                                                         |
| sac. h                      | Définit des données de canal authentifiées sécurisées requises par l’ensemble des applications et des fournisseurs de services.                                                                                                                                                                                                                                                                                                                                                       |
| scclient. h                 | Définit la classe [CSecureChannelClient](csecurechannelclient-class.md) requise par toutes les applications.                                                                                                                                                                                                                                                                                                                                              |
| SCServer. h                 | Définit la classe [CSecureChannelServer](csecurechannelserver-class.md) requise par tous les fournisseurs de services.                                                                                                                                                                                                                                                                                                                                         |
| WMDM \_ ver. h                | informations de version facultatives sur Windows Gestionnaire de périphériques de média.                                                                                                                                                                                                                                                                                                                                                                                    |
| wmdmlog. h, wmdmlog \_ i. c    | Requis pour les applications ou les fournisseurs de services qui utilisent l’interface [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger) .                                                                                                                                                                                                                                                                                                                                           |
| wmdrmdeviceapp. h           | Requis pour les applications qui gèrent le contrôle de contenu (consultez [contrôle de l’utilisation du contenu](metering-content-usage.md)).                                                                                                                                                                                                                                                                                                                                  |
| wmsstd. h                   | Définit les macros d’assistance utilisées par les exemples du kit de développement logiciel (SDK).                                                                                                                                                                                                                                                                                                                                                                                                      |
| lib\\                      | dossier contenant les bibliothèques Windows Media Gestionnaire de périphériques.                                                                                                                                                                                                                                                                                                                                                                                       |
| mssachlp. lib               | bibliothèque statique requise par tous les Windows Gestionnaire de périphériques les applications multimédias et les fournisseurs de services.                                                                                                                                                                                                                                                                                                                                                 |
| drmcrypto. lib              | bibliothèque statique requise par tous les Windows Media Gestionnaire de périphériques les applications et les fournisseurs de services qui utilisent DRM.                                                                                                                                                                                                                                                                                                                                    |
| MDSP \\ ....<br/>      | Dossier qui contient le code d’un exemple de fournisseur de services. Pour plus d’informations sur cet exemple, notamment sur la façon de le compiler et de l’exécuter, consultez [exemple de fournisseur de services](sample-service-provider.md).                                                                                                                                                                                                                                                    |
| applications \\ ....<br/>      | Dossier qui contient deux sous-dossiers qui contiennent deux moitiés du code pour un exemple d’application de bureau fournie avec le kit de développement logiciel (SDK). Pour plus d’informations sur cet exemple, notamment sur la façon de le compiler, consultez [exemple d’application de bureau](sample-desktop-application.md).                                                                                                                                                                                      |
| DeviceKit \\ ....<br/> | dossier qui contient une suite d’outils permettant de tester votre appareil mobile à l’aide d’Windows Media Gestionnaire de périphériques 11. Les tests incluent l’énumération et le transfert d’appareils et de fichiers, les fonctionnalités DRM et la conformité MTP. Ces outils ont leur propre fichier de documentation.                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Prise en main**](getting-started.md)
</dt> </dl>

 

 





