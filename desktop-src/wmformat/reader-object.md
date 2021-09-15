---
title: Lecteur, objet
description: Lecteur, objet
ms.assetid: b5edbf8b-820f-4e09-a482-8efc2283360e
keywords:
- Windows Media Format SDK, Reader, objets
- ASF (Advanced Systems Format), objets Reader
- ASF (format des systèmes avancés), objets lecteur
- objets, lecteurs, objets
- objets Reader, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7958689fa7744286c92c294219fb2c963e55c860
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404664"
---
# <a name="reader-object"></a>Lecteur, objet

L’objet lecteur lit les exemples de données à partir de fichiers multimédias. L’objet lecteur prend actuellement en charge les fichiers à l’aide de la structure de fichiers ASF (Advanced Systems Format) et des fichiers MP3. Les données fournies par l’objet lecteur sont décompressées et prêtes à être rendues par défaut, mais les exemples peuvent être remis sans décompression si vous le souhaitez. Les exemples sont remis de manière asynchrone à partir de l’objet lecteur ; vous devez configurer une fonction de rappel pour les recevoir. Pour la lecture synchrone des fichiers ASF, utilisez l’objet lecteur synchrone. Ni le lecteur ni le lecteur synchrone n’affichent de données. Vous devez fournir vos propres routines de rendu pour afficher le média récupéré à partir d’un fichier.

Lorsqu’un fichier contient un média encodé qui peut être décodé avec un codec pris en charge par l’objet lecteur, vous pouvez contrôler le format de la sortie non compressée. Pour modifier le format de sortie décompressée d’un flux, vous devez récupérer l’objet de propriétés de média de sortie par défaut pour ce flux, y apporter des modifications, puis le réassigner au flux du lecteur. Les objets de propriétés de média de sortie sont subordonnés à l’objet lecteur et doivent être créés uniquement à l’aide de la méthode [**IWMReader :: GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) .

L’objet lecteur est créé par la fonction [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader), qui définit un pointeur vers une interface **IWMReader** . Les autres interfaces de l’objet Reader peuvent être obtenues en appelant la méthode **QueryInterface** .

Les interfaces suivantes sont prises en charge par l’objet lecteur.



| Interface                                                    | Description                                                                                                                                                                     |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IReferenceClock**](ireferenceclock.md)                   | Fournit l’accès à l’horloge système utilisée par le lecteur.                                                                                                                         |
| [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)                         | Gère l’acquisition de licence, les propriétés [*DRM*](wmformat-glossary.md) et l’individualisation du client.                                  |
| [**IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2)                       | Donne accès aux licences qui utilisent des niveaux de protection de sortie (OPL) pour spécifier des droits.                                                                                          |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)                       | Définit et récupère les informations d’en-tête, y compris les métadonnées, les [*marqueurs*](wmformat-glossary.md)et les données de script.                                                 |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)                     | Récupère des informations sur les codecs utilisés pour encoder le contenu dans le fichier. Hérite de toutes les méthodes de **IWMHeaderInfo**.                                      |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)                     | Prend en charge des tailles d’attribut volumineuses, des noms d’attributs dupliqués et la prise en charge de plusieurs langues. Hérite de toutes les méthodes de **IWMHeaderInfo** et **IWMHeaderInfo2**.              |
| [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)                       | Récupère la taille du paquet le plus volumineux dans le fichier chargé dans le lecteur.                                                                                                      |
| [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)                     | Récupère la taille du plus petit paquet du fichier chargé dans le lecteur.                                                                                                     |
| [**IWMProfile**](iwmprofile.md)                             | Fournit l’accès aux informations de profil du fichier chargé dans le lecteur.                                                                                                    |
| [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)                           | Récupère l’identificateur global unique (GUID), le cas échéant, associé au profil. Hérite de toutes les méthodes de **IWMProfile**.                                            |
| [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)                           | Prend en charge le partage de bande passante et les informations de hiérarchisation des flux dans le profil. Hérite de toutes les méthodes de **IWMProfile** et **IWMProfile2**.                             |
| [**IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)                               | Fournit des fonctionnalités de lecture de fichiers de base, notamment des opérations telles que ouvrir, fermer, démarrer, suspendre, reprendre, arrêter et obtenir et définir les propriétés de sortie.                  |
| [**IWMReaderAccelerator**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderaccelerator)         | Communique avec l’accélération vidéo DirectX.                                                                                                                                   |
| [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)               | Fournit des fonctionnalités avancées du lecteur, telles qu’une horloge fournie par l’utilisateur, une allocation de mémoire tampon, des statistiques de retour et des notifications de sélection de flux.                              |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)             | Fournit une plage supplémentaire de méthodes avancées pour un objet lecteur existant. Hérite de toutes les méthodes de **IWMReaderAdvanced**.                                           |
| [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3)             | Fournit une recherche avancée et un contrôle de diffusion en continu. Hérite de toutes les méthodes de **IWMReaderAdvanced** et **IWMReaderAdvanced2**.                                               |
| [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)             | Fournit des options de lecture avancées incluant la prise en charge de plusieurs langues. Hérite de toutes les méthodes de **IWMReaderAdvanced**, **IWMReaderAdvanced2** et **IWMReaderAdvanced3**. |
| [**IWMReaderNetworkConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig)     | Contrôle les paramètres de configuration réseau.                                                                                                                                        |
| [**IWMReaderNetworkConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2)   | Fournit l’accès aux paramètres de configuration réseau avancés. Hérite de toutes les méthodes de **IWMReaderNetworkConfig**.                                                          |
| [**IWMReaderStreamClock**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderstreamclock)         | Définit et annule des minuteries sur les horloges de flux, et récupère la valeur actuelle d’une horloge de flux spécifiée.                                                                          |
| [**IWMReaderTimecode**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode)               | Fournit des informations sur les plages de codes temporels SMPTE dans le fichier chargé dans le lecteur.                                                                                             |
| [**IWMReaderTypeNegotiation**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation) | Teste si les modifications apportées aux propriétés de sortie d’un flux fonctionnent correctement.                                                                                                |



 

Les interfaces de rappel suivantes peuvent être implémentées dans l’application pour suivre la progression d’un objet lecteur.



| Interface                                                      | Description                                                                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)         | Acquiert les informations d’identification des utilisateurs et vérifie qu’ils sont autorisés à accéder à un site distant.                                               |
| [**IWMReaderAllocatorEx**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderallocatorex)           | Fournit des alternatives étendues aux méthodes **AllocateForOutput** et **AllocateForStream** de l’interface **IWMReaderCallbackAdvanced** . |
| [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback)                 | Fournit des méthodes de rappel pour les méthodes **Start** et **Open** de **IWMReader**.                                                            |
| [**IWMReaderCallbackAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced) | Fournit des méthodes de rappel pour les méthodes de l’interface [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) .                                    |
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback)                 | Obligatoire lorsque les informations d’État doivent être communiquées à l’application hôte.                                                                |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Objets**](objects.md)
</dt> <dt>

[**Lecture des fichiers ASF**](reading-asf-files.md)
</dt> <dt>

[**Lecteur synchrone, objet**](synchronous-reader-object.md)
</dt> </dl>

 

 




