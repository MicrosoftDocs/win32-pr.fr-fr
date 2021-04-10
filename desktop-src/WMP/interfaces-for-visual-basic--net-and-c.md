---
title: Interfaces pour Visual Basic .NET et C
description: Interfaces pour Visual Basic .NET et C \
ms.assetid: c66f1e03-20eb-45b1-8710-be9eae63e7ad
keywords:
- Lecteur Windows Media, interfaces
- Windows Media Player Mobile, interfaces
- Modèle objet du lecteur Windows Media, interfaces
- modèle objet, interfaces
- Contrôle ActiveX, interfaces
- Contrôle ActiveX du lecteur Windows Media, interfaces
- Contrôle ActiveX Windows Media Player Mobile, interfaces
- informations de référence sur le modèle objet, les interfaces
- Référence du modèle objet d’interface
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a301cb075ccee049272f1db9b2582aeae6697fa3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197045"
---
# <a name="interfaces-for-visual-basic-net-and-c"></a>Interfaces pour Visual Basic .NET et C #

Cette section décrit les interfaces exposées par le contrôle ActiveX du lecteur Windows Media.

Plusieurs propriétés et méthodes de l' [objet AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) sont utilisées pour récupérer des interfaces spécifiques. Ces interfaces peuvent à leur tour avoir des propriétés et des méthodes d’accesseur pour récupérer d’autres interfaces.

Le contrôle du lecteur Windows Media expose les interfaces suivantes.



| Interface                                                      | Description                                                                                                                                                       |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IWMPCdrom](iwmpcdrom--vb-and-c.md)                           | Accède à un CD ou un DVD dans un lecteur.                                                                                                                                  |
| [IWMPCdromBurn](iwmpcdromburn--vb-and-c.md)                   | Fournit des propriétés et des méthodes pour gérer la création de CD audio.                                                                                                     |
| [IWMPCdromCollection](iwmpcdromcollection--vb-and-c.md)       | Accède à une collection de lecteurs de CD ou DVD.                                                                                                                        |
| [IWMPCdromRip](iwmpcdromrip--vb-and-c.md)                     | Fournit des propriétés et des méthodes pour gérer la copie, ou l' *extraction*, des pistes d’un CD audio.                                                                         |
| [IWMPClosedCaption](iwmpclosedcaption--vb-and-c.md)           | Offre un moyen d’inclure des sous-titres avec un fichier multimédia numérique.                                                                                                     |
| [IWMPClosedCaption2](iwmpclosedcaption2--vb-and-c.md)         | Fournit des propriétés et des méthodes de sous-titrage supplémentaires.                                                                                                     |
| [IWMPControls](iwmpcontrols--vb-and-c.md)                     | Représente les contrôles de transport du lecteur Windows Media, tels que lecture, arrêt et pause.                                                                         |
| [IWMPControls2](iwmpcontrols2--vb-and-c.md)                   | Fournit une méthode de contrôle supplémentaire pour geler la lecture sur le frame suivant ou précédent.                                                                           |
| [IWMPControls3](iwmpcontrols3--vb-and-c.md)                   | Fournit des propriétés et des méthodes de contrôle supplémentaires pour la sélection et la prise en charge de la langue audio.                                                                      |
| [IWMPDVD](iwmpdvd--vb-and-c.md)                               | Fournit des propriétés et des méthodes pour travailler avec des DVD.                                                                                                            |
| [IWMPError](iwmperror--vb-and-c.md)                           | Accède à une collection d’interfaces [IWMPErrorItem](iwmperroritem--vb-and-c.md) pour la récupération des informations d’erreur.                                                |
| [IWMPErrorItem](iwmperroritem--vb-and-c.md)                   | Fournit l’accès aux informations d’erreur.                                                                                                                             |
| [IWMPErrorItem2](iwmperroritem2--vb-and-c.md)                 | Fournit une propriété d’élément d’erreur supplémentaire pour obtenir un code de condition d’erreur.                                                                                   |
| **IWMPFolderMonitorServices**                                  | Non pris en charge pour la programmation .NET.                                                                                                                               |
| [IWMPLibrary](iwmplibrary--vb-and-c.md)                       | Représente une bibliothèque.                                                                                                                                             |
| [IWMPLibraryServices](iwmplibraryservices--vb-and-c.md)       | Fournit des méthodes pour énumérer des bibliothèques.                                                                                                                          |
| **IWMPLibrarySharingServices**                                 | Non pris en charge pour la programmation .NET.                                                                                                                               |
| [IWMPMedia](iwmpmedia--vb-and-c.md)                           | Fournit un moyen de définir et de récupérer les propriétés d’un élément multimédia.                                                                                                |
| [IWMPMedia2](iwmpmedia2--vb-and-c.md)                         | Fournit l’accès à une propriété d’élément multimédia supplémentaire.                                                                                                             |
| [IWMPMedia3](iwmpmedia3--vb-and-c.md)                         | Fournit des méthodes supplémentaires pour accéder aux propriétés d’un élément multimédia.                                                                                             |
| [IWMPMediaCollection](iwmpmediacollection--vb-and-c.md)       | Fournit des méthodes qui peuvent être utilisées pour organiser une grande collection d’éléments multimédias.                                                                                  |
| [IWMPMediaCollection2](iwmpmediacollection2--vb-and-c.md)     | Fournit des méthodes qui complètent l’interface **IWMPMediaCollection** .                                                                                           |
| [IWMPMetadataPicture](iwmpmetadatapicture--vb-and-c.md)       | Fournit des propriétés pour obtenir des informations sur l’image contenue dans un fichier multimédia numérique représenté par un attribut de métadonnées **WM/Picture** .         |
| [IWMPMetadataText](iwmpmetadatatext--vb-and-c.md)             | Fournit des propriétés pour obtenir des informations sur les attributs de métadonnées textuelles complexes.                                                                            |
| [IWMPNetwork](iwmpnetwork--vb-and-c.md)                       | Fournit des propriétés et des méthodes permettant d’accéder aux statistiques relatives à la qualité d’une connexion réseau, ainsi que de spécifier et de récupérer les paramètres du proxy réseau.     |
| **IWMPPlayerApplication**                                      | Non pris en charge pour la programmation .NET.                                                                                                                               |
| **IWMPPlayerServices**                                         | Non pris en charge pour la programmation .NET.                                                                                                                               |
| **IWMPPlayerServices2**                                        | Non pris en charge pour la programmation .NET.                                                                                                                               |
| [IWMPPlaylist](iwmpplaylist--vb-and-c.md)                     | Fournit des propriétés et des méthodes pour organiser, gérer et manipuler des éléments multimédias dans une sélection.                                                                    |
| [IWMPPlaylistArray](iwmpplaylistarray--vb-and-c.md)           | Accède à une collection d’interfaces [IWMPPlaylist](iwmpplaylist--vb-and-c.md) par numéro d’index.                                                                   |
| [IWMPPlaylistCollection](iwmpplaylistcollection--vb-and-c.md) | Fournit des méthodes pour manipuler des interfaces [IWMPPlaylist](iwmpplaylist--vb-and-c.md) et [IWMPPlaylistArray](iwmpplaylistarray--vb-and-c.md) dans une collection. |
| [IWMPQuery](iwmpquery--vb-and-c.md)                           | Représente une requête composée.                                                                                                                                      |
| [IWMPSettings](iwmpsettings--vb-and-c.md)                     | Fournit des propriétés et des méthodes qui obtiennent ou définissent les valeurs des paramètres du lecteur Windows Media.                                                                      |
| [IWMPSettings2](iwmpsettings2--vb-and-c.md)                   | Fournit des propriétés et une méthode qui complètent l’interface **IWMPSettings** .                                                                                  |
| [IWMPStringCollection](iwmpstringcollection--vb-and-c.md)     | Fournit une propriété et une méthode pour accéder à une collection de chaînes par numéro d’index.                                                                           |
| [IWMPStringCollection2](iwmpstringcollection2--vb-and-c.md)   | Fournit des méthodes qui complètent l’interface **IWMPStringCollection** .                                                                                          |
| **IWMPSyncDevice**                                             | Non pris en charge pour la programmation .NET.                                                                                                                               |
| **IWMPSyncDevice2**                                            | Non pris en charge pour la programmation .NET.                                                                                                                               |
| **IWMPSyncServices**                                           | Non pris en charge pour la programmation .NET.                                                                                                                               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence du modèle objet pour Visual Basic .NET et C #**](object-model-reference-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 




