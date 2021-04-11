---
title: Fonctions du SDK du format Windows Media
description: Fonctions
ms.assetid: 10fa8f96-8030-4727-af5d-7c06229d05d8
keywords:
- Windows Media Format SDK, fonctions
- ASF (Advanced Systems Format), fonctions
- ASF (format des systèmes avancés), fonctions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cab464c3384a65776b993c2423f174debd7a89d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383575"
---
# <a name="windows-media-format-sdk-functions"></a>Fonctions du SDK du format Windows Media

Le kit de développement logiciel (SDK) du format Windows Media comprend des fonctions permettant de créer des objets, ainsi que des fonctions d’assistance pour simplifier certaines procédures.

Ce kit de développement logiciel (SDK) prend en charge les fonctions suivantes pour la création initiale d’objets. Si un objet n’est pas listé ci-dessous, vous devez le créer à l’aide d’une interface à partir d’un autre objet. Pour plus d'informations, consultez [Objets](objects.md).



| Fonction                                                                             | Description                                                                                                                                             |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WMCheckURLExtension**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlextension)                                   | Examine l’extension de nom de fichier dans l’URL ou le nom de fichier qui est passé comme argument.                                                               |
| [**WMCheckURLScheme**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlscheme)                                         | Examine un protocole réseau et le compare à une liste interne de schémas pris en charge.                                                                    |
| [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer)                             | Crée un objet de restauration de sauvegarde.                                                                                                                       |
| [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85))                                   | Encapsule les certificats de l’utilisateur dans un objet.                                                                                                           |
| [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration)                     | Crée un objet d’inscription d’appareil.                                                                                                                   |
| [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor)                           | Crée un objet de transchiffreur DRM.                                                                                                                      |
| [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor)                                             | Crée un objet d’éditeur de métadonnées.                                                                                                                       |
| [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)                                           | Crée un objet indexeur.                                                                                                                              |
| [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent)             | Crée un objet agent de révocation de licence.                                                                                                              |
| [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)                             | Crée un objet de gestionnaire de profils.                                                                                                                       |
| [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader)                                             | Crée un objet lecteur.                                                                                                                                |
| [**WMCreateSecureChannel**](/previous-versions/windows/desktop/api/Wmsecure/nf-wmsecure-wmcreatesecurechannel)                               | Crée un objet qui implémente [**IWMSecureChannel**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel).                                                                         |
| [**WMCreateSecureChannel \_ certifié**](/previous-versions/windows/desktop/api/wmsecure/nf-wmsecure-wmcreatesecurechannel_certified)          | Crée un objet qui implémente [**IWMSecureChannel**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel).                                                                         |
| [**WMCreateSecureChannel \_ certifié \_ des**](/previous-versions/windows/desktop/api/wmsecure/nf-wmsecure-wmcreatesecurechannel_certified_des) | Crée un objet qui implémente [**IWMSecureChannel**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel)..                                                                        |
| [**WMCreateSecureChannel \_ des**](/previous-versions/windows/desktop/api/wmsecure/nf-wmsecure-wmcreatesecurechannel_des)                      | Crée un objet qui implémente [**IWMSecureChannel**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel).                                                                         |
| [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader)                                     | Crée un objet lecteur synchrone.                                                                                                                    |
| [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)                                             | Crée un objet Writer.                                                                                                                                |
| [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)                             | Crée un objet de récepteur de fichiers de writer.                                                                                                                      |
| [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink)                       | Crée un objet récepteur réseau du writer.                                                                                                                   |
| [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink)                             | Crée un objet récepteur push de l’enregistreur.                                                                                                                      |
| [**WMIsAvailableOffline**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmisavailableoffline)                                 | Vérifie qu’un fichier ASF peut être lu à partir d’une copie mise en cache.                                                                                             |
| [**WMIsContentProtected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected)                                 | Vérifie un fichier pour le contenu DRM protégé.                                                                                                                |
| [**WMValidateData**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmvalidatedata)                                             | Vérifie que les données à partir du début d’un fichier sont cohérentes avec la section d’en-tête d’un type de fichier pris en charge par le kit de développement logiciel (SDK) du format Windows Media. |



 

Les fonctions suivantes fournissent des raccourcis pratiques pour l’analyse des fichiers.



| Fonction                                             | Description                                                                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**WMCheckURLExtension**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlextension)   | Tente de déterminer si un fichier est lisible par les objets du kit de développement logiciel (SDK) du format Windows Media, en fonction de l’extension de nom de fichier.              |
| [**WMCheckURLScheme**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlscheme)         | Détermine si un protocole réseau est pris en charge par les objets du kit de développement logiciel (SDK) du format Windows Media.                                           |
| [**WMIsAvailableOffline**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmisavailableoffline) | Détermine si un fichier est disponible pour la lecture hors connexion.                                                                                 |
| [**WMIsContentProtected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected) | Vérifie un fichier pour le contenu DRM protégé.                                                                                                     |
| [**WMValidateData**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmvalidatedata)             | Tente de déterminer si un fichier est lisible par les objets du kit de développement logiciel (SDK) du format Windows Media en analysant les données au début du fichier. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Objets**](objects.md)
</dt> <dt>

[**Guide de référence de programmation**](programming-reference.md)
</dt> </dl>

 

 
