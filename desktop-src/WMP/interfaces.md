---
title: Interfaces de SDK WMP
description: Interfaces de SDK WMP
ms.assetid: 68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd
keywords:
- Lecteur Windows Media, interfaces
- Lecteur Windows Media Mobile, interfaces
- Lecteur Windows Media modèle objet, interfaces
- modèle objet, interfaces
- contrôle ActiveX, interfaces
- contrôle ActiveX Lecteur Windows Media, interfaces
- Lecteur Windows Media contrôle Mobile ActiveX, interfaces
- informations de référence sur le modèle objet, les interfaces
- Référence du modèle objet d’interface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7db8e5ebe29e38da9f92370f60a622fad70f36395b271eb7bd86ef49f49a3d49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123499"
---
# <a name="wmp-sdk-interfaces"></a>Interfaces de SDK WMP

cette section documente les interfaces COM exposées par le contrôle Lecteur Windows Media ActiveX et le contrôle Lecteur Windows Media ActiveX Mobile.

Les méthodes d’accesseur de l’interface **IWMPCore** ou **IWMPPlayer** sont utilisées pour récupérer des interfaces spécifiques. Ces interfaces peuvent à leur tour avoir des méthodes d’accesseur pour récupérer d’autres interfaces. L’appel de **QueryInterface** sur l’une de ces interfaces est nécessaire uniquement lorsque vous récupérez la version de base d’une interface et que vous souhaitez appeler une méthode sur une version ultérieure de la même interface.

> [!Note]  
> toutes les méthodes et tous les événements sont entièrement pris en charge dans Lecteur Windows Media 10 Mobile et versions ultérieures, sauf indication contraire.

le contrôle Lecteur Windows Media expose les interfaces suivantes.

| Interface                                                    | Description                                                                                                                                                                               |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_WMPOCXEvents](-wmpocxevents-interface.md)                | fournit des événements provenant du contrôle Lecteur Windows Media auxquels un programme d’incorporation peut répondre.                                                                              |
| [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)                                   | Accède à un CD ou un DVD dans un lecteur.                                                                                                                                                          |
| [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)                           | Fournit des méthodes pour gérer la création de CD audio.                                                                                                                                            |
| [IWMPCdromCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)               | Accède à une collection de lecteurs de CD ou DVD.                                                                                                                                                |
| [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)                             | Fournit des méthodes pour gérer la copie des pistes à partir d’un CD audio.                                                                                                                               |
| [IWMPClosedCaption](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption)                   | Comprend des légendes avec un clip multimédia.                                                                                                                                                      |
| [IWMPClosedCaption2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption2)                 | Fournit des méthodes de sous-titrage supplémentaires.                                                                                                                                            |
| [IWMPControls](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)                             | représente les contrôles de transport de Lecteur Windows Media, tels que lecture, arrêt et Pause.                                                                                                 |
| [IWMPControls2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2)                           | Fournit des méthodes de contrôle supplémentaires.                                                                                                                                                      |
| [IWMPControls3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols3)                           | Fournit des méthodes de contrôle supplémentaires.                                                                                                                                                      |
| [IWMPCore](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore)                                     | Récupère des pointeurs vers d’autres interfaces et accède aux fonctionnalités de base du contrôle. il s’agit de l’interface racine pour le modèle objet Lecteur Windows Media.                                  |
| [IWMPCore2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore2)                                   | Fournit des méthodes de base supplémentaires.                                                                                                                                                         |
| [IWMPCore3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore3)                                   | Fournit des méthodes de base supplémentaires.                                                                                                                                                         |
| [IWMPDVD](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpdvd)                                       | Accède au menu contenu d’un DVD.                                                                                                                                                       |
| [IWMPError](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperror)                                   | Accède à une collection de pointeurs [IWMPErrorItem](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem) .                                                                                                                     |
| [IWMPErrorItem](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem)                           | Fournit des informations sur les erreurs.                                                                                                                                                        |
| [IWMPErrorItem2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem2)                         | Fournit des méthodes d’élément d’erreur supplémentaires.                                                                                                                                                   |
| [IWMPEvents](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)                       | expose les événements qui proviennent du contrôle Lecteur Windows Media auquel un programme d’incorporation peut répondre.                                                                            |
| [IWMPEvents2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)                     | expose les événements qui proviennent du contrôle Lecteur Windows Media 10 auquel un programme d’incorporation peut répondre. Ces événements sont utilisés spécifiquement pour les programmes de synchronisation d’appareil. |
| [IWMPEvents3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)                               | Fournit des événements liés à l’extraction de CD, à la gravure de CD, à la surveillance de dossiers et aux services de bibliothèque distants.                                                                                        |
| [IWMPFolderMonitorServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)   | fournit des méthodes pour énumérer, analyser et modifier des dossiers de fichiers qui Lecteur Windows Media analyse le contenu multimédia numérique.                                                                |
| [IWMPGraphCreation](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation)                   | gère le graphique DirectShow.                                                                                                                                                             |
| [IWMPLibrary](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)                               | Représente une bibliothèque.                                                                                                                                                                     |
| [IWMPLibraryServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)               | Fournit des méthodes pour énumérer des bibliothèques.                                                                                                                                                  |
| [IWMPLibrarySharingServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices) | Fournit des méthodes pour gérer le partage de bibliothèque.                                                                                                                                               |
| [IWMPMedia](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)                                   | Définit et récupère les propriétés d’un élément multimédia.                                                                                                                                        |
| [IWMPMedia2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia2)                                 | Fournit des méthodes supplémentaires pour définir et récupérer les propriétés d’un élément multimédia.                                                                                                           |
| [IWMPMedia3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3)                                 | Fournit des méthodes supplémentaires pour définir et récupérer les propriétés d’un élément multimédia.                                                                                                           |
| [IWMPMediaCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection)               | Accède à une collection de pointeurs [IWMPMedia](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) .                                                                                                                             |
| [IWMPMediaCollection2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)             | Fournit des méthodes qui complètent l’interface **IWMPMediaCollection** .                                                                                                                   |
| [IWMPMetadataPicture](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmetadatapicture)               | Récupère des informations sur l’attribut de métadonnées **WM/image** .                                                                                                                        |
| [IWMPMetadataText](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmetadatatext)                     | Récupère des informations sur les attributs de métadonnées textuelles complexes.                                                                                                                          |
| [IWMPNetwork](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpnetwork)                               | définit et récupère les propriétés de la connexion réseau utilisée par Lecteur Windows Media.                                                                                                 |
| [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer)                                 | contrôle le comportement de l’interface utilisateur du contrôle Lecteur Windows Media.                                                                                                                 |
| [IWMPPlayer2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer2)                               | fournit des méthodes supplémentaires pour le contrôle de Lecteur Windows Media.                                                                                                                         |
| [IWMPPlayer3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer3)                               | fournit des méthodes supplémentaires pour le contrôle de Lecteur Windows Media.                                                                                                                         |
| [IWMPPlayer4](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer4)                               | fournit des méthodes supplémentaires pour le contrôle de Lecteur Windows Media.                                                                                                                         |
| [IWMPPlayerApplication](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerapplication)           | bascule entre un contrôle de Lecteur Windows Media distant et le mode complet du lecteur. Conçu pour être utilisé par les programmes C++ qui incorporent le contrôle en mode distant.                          |
| [IWMPPlayerServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)                 | utilisé par l’hôte d’un contrôle distant pour manipuler le mode complet de Lecteur Windows Media. Conçu pour être utilisé avec C++.                                                                     |
| [IWMPPlayerServices2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2)               | Définit la priorité de traitement en arrière-plan.                                                                                                                                                  |
| [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)                             | Crée et gère des sélections.                                                                                                                                                            |
| [IWMPPlaylistArray](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistarray)                   | Accède à une collection de pointeurs [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) par numéro d’index.                                                                                                       |
| [IWMPPlaylistCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistcollection)         | Manipule les pointeurs [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) et [IWMPPlaylistArray](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistarray) .                                                                                     |
| [IWMPQuery](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)                                   | Représente une requête composée.                                                                                                                                                              |
| [IWMPRemoteMediaServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)       | fournit des services pour Lecteur Windows Media à partir d’un programme qui héberge le contrôle du lecteur. Conçu pour être utilisé avec C++.                                                                        |
| [IWMPRenderConfig](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig)                     | Fournit des méthodes pour spécifier ou récupérer une valeur indiquant si la lecture se produit uniquement dans le processus actuel.                                                                          |
| [IWMPSettings](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings)                             | définit ou récupère des paramètres de Lecteur Windows Media.                                                                                                                                          |
| [IWMPSettings2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2)                           | définit ou récupère des paramètres de Lecteur Windows Media.                                                                                                                                          |
| [IWMPSkinManager](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager)                       | spécifie l’apparence utilisée avec Lecteur Windows Media.                                                                                                                                        |
| [IWMPStringCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection)             | Accède à une collection de chaînes.                                                                                                                                                         |
| [IWMPStringCollection2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)           | Fournit des méthodes qui complètent l’interface **IWMPStringCollection** .                                                                                                                  |
| [IWMPSyncDevice](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)                         | représente un appareil qui peut synchroniser des fichiers multimédias numériques avec Lecteur Windows Media 10.                                                                                                |
| [IWMPSyncDevice2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)                       | Fournit une méthode qui complète l’interface **IWMPSyncDevice** .                                                                                                                      |
| [IWMPSyncServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)                     | énumère les appareils disponibles qui peuvent synchroniser des fichiers multimédias numériques avec Lecteur Windows Media 10.                                                                                       |
| [IWMPTranscodePolicy](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmptranscodepolicy)               | fournit une méthode implémentée par DirectShow filtres source pour gérer la modification du format des fichiers multimédias numériques.                                                                          |
| [IWMPVideoRenderConfig](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)           | fournit une méthode qui configure le convertisseur vidéo amélioré utilisé par Lecteur Windows Media.                                                                                               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence du modèle objet pour C++**](object-model-reference-for-c.md)
</dt> </dl>

 

 




