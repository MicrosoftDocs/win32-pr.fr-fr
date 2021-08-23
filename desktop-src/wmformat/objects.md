---
title: Objets (SDK du format Windows Media 11)
description: Objets
ms.assetid: f884e115-d41a-4f36-bcef-dfaef78510af
keywords:
- Windows Media Format SDK, objets
- ASF (Advanced Systems Format), objets
- ASF (format des systèmes avancés), objets
- objets, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ccd206a548093602f609a11ed11a8d98b910bc35eefb6ba55b985427ac1d212
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707449"
---
# <a name="objects-windows-media-format-11-sdk"></a>Objets (SDK du format Windows Media 11)

le kit de développement logiciel (SDK) Windows Media Format utilise plusieurs objets pour lire, écrire, modifier et indexer des fichiers ASF, ainsi que pour créer et modifier des profils. Chaque objet prend en charge un certain nombre d’interfaces. Certaines interfaces sont prises en charge dans plusieurs objets. Dans ce cas, toutes les différences d’implémentation sont présentées dans la section de référence de l’interface.

les objets du kit de développement logiciel (SDK) Windows Media Format sont conformes à COM. Pour faciliter le développement, chaque objet est associé à une fonction ou à une méthode de création. Vous devez créer des objets à l’aide de la fonction ou de la méthode de création plutôt que manuellement à l’aide de la fonction COM **CoCreateInstance**.

Certaines interfaces ont un nombre ajouté à leur nom, tel que **IWMProfile2** et **IWMWriter3**. Dans chaque cas, les versions numérotées héritent de toutes les méthodes des versions antérieures et ajoutent de nouvelles fonctionnalités.

Sur chaque page d’objet de cette référence, les interfaces incluses dans l’objet COM principal sont répertoriées en premier, suivies des interfaces de rappel qui doivent être implémentées par l’application.

Le tableau suivant répertorie les objets pris en charge par ce kit de développement logiciel (SDK), ainsi qu’une description des fonctionnalités de chacune d’elles et de la fonction utilisée pour la créer.



| Object                                                          | Description                                                                                                                                              | Fonction de création                                                        |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Restauration de sauvegarde](backup-restorer-object.md)                   | Sauvegarde les licences, généralement sur des supports amovibles, puis restaure ces licences sur un autre ordinateur.                                           | [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer)                 |
| [Inscription de l’appareil](device-registration-object.md)           | Gère la base de données d’inscription des appareils, qui contient des entrées pour les périphériques de lecture multimédia disponibles via une connexion réseau.             | [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration)         |
| [Transcrypteur DRM](drm-transcryptor-object.md)                 | convertit les données multimédias protégées par drm dans un flux de données qui peut être envoyé aux appareils qui utilisent le protocole Windows media DRM 10 pour les périphériques réseau. | [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor)               |
| [Indexeur](indexer-object.md)                                   | Crée un index pour les fichiers ASF pour permettre la recherche dans des fichiers avec des flux vidéo.                                                                            | [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)                               |
| [Agent de révocation des licences](license-revocation-agent-object.md) | Gère la révocation de licence.                                                                                                                              | [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) |
| [Metadata Editor](metadata-editor-object.md)                   | Modifie les métadonnées dans un en-tête de fichier ASF.                                                                                                                    | [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor)                                 |
| [Gestionnaire de profil](profile-manager-object.md)                   | Fournit des interfaces pour créer, charger et enregistrer des profils. Un profil est requis pour écrire un fichier ASF.                                                      | [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)                 |
| [Lecteur](reader-object.md)                                     | Lit les fichiers ASF. Cet objet utilise un modèle d’appel asynchrone pour ses opérations.                                                                      | [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader)                                 |
| [Lecteur synchrone](synchronous-reader-object.md)             | Lit les fichiers ASF à l’aide d’appels synchrones.                                                                                                                 | [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader)                         |
| [Écrit](writer-object.md)                                     | Écrit des fichiers ASF.                                                                                                                                        | [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)                                 |
| [Récepteur de fichiers de l’enregistreur](writer-file-sink-object.md)                 | Contrôle les fichiers ASF écrits par l’objet Writer.                                                                                                         | [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)                 |
| [Récepteur réseau de l’enregistreur](writer-network-sink-object.md)           | Contrôle le streaming réseau en direct des fichiers ASF écrits par l’objet Writer.                                                                               | [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink)           |
| [Récepteur push de l’enregistreur](writer-push-sink-object.md)                 | Contrôle la remise de contenu de diffusion en continu aux serveurs de publication.                                                                                            | [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink)                 |



 

Le tableau suivant répertorie les objets qui dépendent d’autres objets. Ces objets sont créés par des méthodes d’objets existants.



| Object                                                        | Description                                                                                                                                                                                                                                                                                                                           | Méthode de création                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Partage de bande passante](bandwidth-sharing-object.md)             | Gère les informations de partage de bande passante dans un profil. Il peut exister plusieurs objets de partage de bande passante pour un profil. Il existe différentes méthodes pour créer un objet de partage de bande passante, selon que vous souhaitez créer un nouvel objet de partage de bande passante ou accéder à un objet existant.                                           | [**IWMProfile3 :: CreateNewBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing) NI<br/> [**IWMProfile3::GetBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)<br/>                                                                                                                                                                                                                                      |
| [Buffer](buffer-object.md)                                   | Contient un exemple de média et toutes les extensions d’unité de données associées. Utilisé pour les exemples d’écriture et de lecture.                                                                                                                                                                                                                           | [**IWMWriter :: AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample) NI<br/> [**IWMReaderAllocatorEx::AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex)<br/> OR<br/> [**IWMReaderAllocatorEx::AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex)<br/> OR<br/> Créé automatiquement par l’objet lecteur ou un objet lecteur synchrone pour l’exemple de remise.<br/> |
| [Propriétés du média d’entrée](input-media-properties-object.md)   | Gère les propriétés d’une entrée. Un objet de propriétés d’entrée peut exister pour chaque entrée.                                                                                                                                                                                                                                             | [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops)                                                                                                                                                                                                                                                                                                                                                                      |
| [Exclusion mutuelle](mutual-exclusion-object.md)               | Gère les informations d’exclusion mutuelle dans un profil. Les utilisations courantes de l’exclusion mutuelle sont le contenu à vitesse de transmission multiple et les pistes audio dans plusieurs langues. Il existe différentes méthodes pour créer un objet d’exclusion mutuelle, selon que vous souhaitez créer un nouvel objet d’exclusion mutuelle ou accéder à un objet existant.         | [**IWMProfile :: CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) NI<br/> [**IWMProfile::GetMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)<br/>                                                                                                                                                                                                                                              |
| [Propriétés du média de sortie](output-media-properties-object.md) | Gère les propriétés d’une sortie. Un objet de propriétés de média de sortie peut exister pour chaque sortie. Ces objets peuvent être créés par le lecteur ou par le lecteur synchrone                                                                                                                                                            | [**IWMReader :: GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) NI<br/> [**IWMSyncReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)<br/>                                                                                                                                                                                                                                                                      |
| [Profil](profile-object.md)                                 | Contient les données d’un profil pendant qu’il est en cours de manipulation. Les objets de profil sont créés chaque fois que le profil doit être manipulé. Il existe différentes méthodes pour créer un objet de profil selon que vous souhaitez créer un nouveau profil ou accéder à un profil existant.                                                  | [**IWMProfileManager :: CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) NI<br/> [**IWMProfileManager::LoadProfileByData**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebydata)<br/> OR<br/> [**IWMProfileManager::LoadProfileByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)<br/> OR<br/> [**IWMProfileManager::LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile)<br/>          |
| [Configuration de flux](stream-configuration-object.md)       | Gère les propriétés d’un flux dans un profil. Les objets de configuration de flux sont créés par les objets de flux chaque fois que vous avez besoin d’accéder aux informations relatives à un flux. Il existe différentes méthodes pour créer un objet de configuration de flux selon que vous souhaitez créer un flux ou un accès et un objet existant. | [**IWMProfile :: CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream) NI<br/> [**IWMProfile :: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)<br/> OR<br/> [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber)<br/>                                                                                                                                                                                   |
| [Hiérarchisation des flux](stream-prioritization-object.md)     | Gère la liste des priorités de flux pour un profil. Les flux sont supprimés par ordre de priorité, si la bande passante disponible est limitée. Un profil ne peut contenir qu’un seul objet de priorité de flux.                                                                                                                  | [**IWMProfile3::CreateNewStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization)                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de référence de programmation**](programming-reference.md)
</dt> </dl>

 

 





