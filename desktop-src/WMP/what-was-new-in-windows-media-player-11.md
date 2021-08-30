---
title: Nouveautés de Windows Media Player 11
description: cette rubrique répertorie les nouvelles fonctionnalités de Lecteur Windows Media 11 et du kit de développement logiciel (SDK) Lecteur Windows Media 11.
ms.assetid: d2a6b6ce-a924-4b55-9dc7-68cc57e5651f
keywords:
- Lecteur Windows Media, nouveautés
- Lecteur Windows Media, nouvelles fonctionnalités
- kit de développement logiciel (SDK), Lecteur Windows Media 11
- SDK (kit de développement logiciel), Lecteur Windows Media 11
- documentation, Lecteur Windows Media 11 SDK
- nouveautés, Lecteur Windows Media 11
- nouvelles fonctionnalités, Lecteur Windows Media 11
- interfaces, nouvelles fonctionnalités de Lecteur Windows Media 11
- attributs, nouvelles fonctionnalités de Lecteur Windows Media 11
- Lecteur Windows Media ActiveX contrôle, nouvelles fonctionnalités de la version 11
- contrôle de ActiveX, nouvelles fonctionnalités de la version 11
- apparences, nouvelles fonctionnalités de Lecteur Windows Media 11
- Lecteur Windows Media skins, nouvelles fonctionnalités de la version 11
- plug-ins, nouvelles fonctionnalités de Lecteur Windows Media 11
- plug-ins Lecteur Windows Media, nouvelles fonctionnalités de la version 11
- magasins en ligne, nouvelles fonctionnalités de Lecteur Windows Media 11
- Lecteur Windows Media des magasins en ligne, nouvelles fonctionnalités de la version 11
- exemples, nouvelles fonctionnalités de Lecteur Windows Media 11
- versions de Lecteur Windows Media, nouvelles fonctionnalités de la version 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b69f9ffdeb3325b7b993e3c2a1826567ebd5507f4d0290248ad4c570b788e137
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001269"
---
# <a name="what-was-new-in-windows-media-player-11"></a>Nouveautés de Windows Media Player 11

cette rubrique répertorie les nouvelles fonctionnalités de Lecteur Windows Media 11 et du kit de développement logiciel (SDK) Lecteur Windows Media 11.

## <a name="windows-media-player-control"></a>Lecteur Windows Media Régulation

les interfaces suivantes ont été introduites dans le contrôle Lecteur Windows Media 11 ActiveX.

-   [**Interface IWMPLibrary**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
-   [**Interface IWMPLibraryServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
-   [**Interface IWMPLibrarySharingServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices)
-   [**Interface IWMPMediaCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)
-   [**Interface IWMPQuery**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
-   [**Interface IWMPStringCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)
-   [**Objet MediaCollection**](mediacollection-object.md)
-   [**Objet Query**](query-object.md)
-   [**StringCollection, objet**](stringcollection-object.md)
-   [**Interface IWMPCdromRip**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)
-   [**Interface IWMPCdromBurn**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
-   [**Interface IWMPFolderMonitorServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
-   [**Interface IWMPSyncDevice2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)
-   [**Interface IWMPVideoRenderConfig**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)
-   [**IWMPUserEventSink**](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpusereventsink)
-   [**Interface IWMPEvents3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)

## <a name="windows-media-player-skins"></a>Lecteur Windows Media Apparences

les fonctionnalités d’apparence suivantes ont été introduites dans Lecteur Windows Media 11.

-   Nouveaux attributs pour positionner les contrôles. Consultez [**AmbientAttributes. Right**](ambientattributes-right.md) et [**AmbientAttributes. Bottom**](ambientattributes-bottom.md).
-   Nouveaux attributs pour le déplacement et le redimensionnement des contrôles. Consultez [**AmbientAttributes. moveSizeTo**](ambientattributes-movesizeto.md) et [**AmbientAttributes. slideTo**](ambientattributes-slideto.md).
-   Nouvel attribut permettant de spécifier le comportement de redimensionnement d’image. Consultez [**AmbientAttributes. resizeImages**](ambientattributes-resizeimages.md).
-   Nouvel attribut permettant de spécifier la mise à l’échelle non uniforme d’un élément d’apparence. Consultez [**AmbientAttributes. nineGridMargins**](ambientattributes-ninegridmargins.md).

## <a name="windows-media-player-plug-ins"></a>Lecteur Windows Media Plug-ins

le kit de développement logiciel (SDK) Lecteur Windows Media 11 a introduit un nouveau type de plug-in pour la conversion des formats de fichiers multimédias numériques. consultez [Lecteur Windows Media les Plug-ins de Conversion](windows-media-player-conversion-plug-ins.md).

les Plug-ins DSP créés avant la publication du kit de développement logiciel (SDK) Lecteur Windows Media 11 doivent être mis à jour pour fonctionner avec Lecteur Windows Media 11. Consultez [mise à jour des plug-ins DSP existants](updating-existing-dsp-plug-ins.md).

l’assistant de plug-in Lecteur Windows Media a été mis à jour pour créer des plug-ins DSP qui fonctionnent dans Lecteur Windows Media 11. pour plus d’informations, consultez [mises à jour de l’assistant de Plug-in DSP pour Lecteur Windows Media 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).

## <a name="windows-media-player-online-stores"></a>Lecteur Windows Media Magasins en ligne

Lecteur Windows Media 11 a introduit un nouveau modèle d’intégration des catalogues de magasin en ligne dans la fonctionnalité de bibliothèque Lecteur Windows Media. Consultez [types 1 magasins en ligne](type-1-online-stores.md).

## <a name="windows-media-player"></a>Lecteur Windows Media

les fonctionnalités suivantes ont été introduites dans Lecteur Windows Media 11.

-   [Extensions d’appareil pour la création de rapports sur le contenu acquis](device-extensions-for-reporting-acquired-content.md)
-   [Extensions d’appareil pour les préférences de l’objet playlist](device-extensions-for-playlist-object-preferences.md)

## <a name="windows-media-player-sdk-samples"></a>Lecteur Windows Media Exemples du kit de développement logiciel

l’exemple C# nommé SchemaReader a été nouveau dans le kit de développement logiciel (SDK) Lecteur Windows Media 11. l’exemple crée un outil qui utilise le modèle objet Lecteur Windows Media pour récupérer et afficher des informations sur les métadonnées dans la bibliothèque Lecteur Windows Media ou dans un fichier multimédia numérique. L’outil peut enregistrer les résultats dans un fichier texte. L’outil énumère les noms d’attributs de métadonnées stockés dans la bibliothèque pour chaque schéma pris en charge (audio, vidéo, sélection, photo, etc.). L’outil peut également fournir des informations sur les attributs disponibles pour les sélections dans la collection de sélections, les pistes de CD, les sommaires de CD, les titres de DVD, les chapitres DVD, la table des matières DVD et les fichiers multimédias individuels.

l’exemple C++ nommé WMPML a été mis à jour dans le kit de développement logiciel (SDK) Lecteur Windows Media 11 pour illustrer les fonctionnalités suivantes :

-   utilisation de la nouvelle interface [**IWMPStringCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2) pour créer une interface utilisateur similaire à la fonctionnalité de bibliothèque Lecteur Windows Media.
-   Utilisation des interfaces [**IWMPQuery**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery) et [**IWMPMediaCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2) pour créer des requêtes composées et afficher les résultats.

 

 




