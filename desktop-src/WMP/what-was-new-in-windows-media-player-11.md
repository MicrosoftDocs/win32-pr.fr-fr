---
title: Nouveautés de Windows Media Player 11
description: Cette rubrique répertorie les fonctionnalités qui ont été introduites dans le lecteur Windows Media 11 et le kit de développement logiciel (SDK) du lecteur Windows Media 11.
ms.assetid: d2a6b6ce-a924-4b55-9dc7-68cc57e5651f
keywords:
- Windows Media Player, nouveautés
- Windows Media Player, nouvelles fonctionnalités
- Kit de développement logiciel (SDK), lecteur Windows Media 11
- SDK (kit de développement logiciel), lecteur Windows Media 11
- documentation, Windows Media Player 11 SDK
- nouveautés, lecteur Windows Media 11
- nouvelles fonctionnalités, lecteur Windows Media 11
- interfaces, nouvelles fonctionnalités dans le lecteur Windows Media 11
- attributs, nouvelles fonctionnalités dans le lecteur Windows Media 11
- Contrôle ActiveX du lecteur Windows Media, nouvelles fonctionnalités de la version 11
- Contrôle ActiveX, nouvelles fonctionnalités de la version 11
- apparences, nouvelles fonctionnalités dans le lecteur Windows Media 11
- Apparences du lecteur Windows Media, nouvelles fonctionnalités de la version 11
- plug-ins, nouvelles fonctionnalités dans le lecteur Windows Media 11
- Plug-ins du lecteur Windows Media, nouvelles fonctionnalités de la version 11
- magasins en ligne, nouvelles fonctionnalités dans le lecteur Windows Media 11
- Windows Media Player Online stores, nouvelles fonctionnalités de la version 11
- exemples, nouvelles fonctionnalités du lecteur Windows Media 11
- versions du lecteur Windows Media, nouvelles fonctionnalités de la version 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12aa728aa1552ac0e65f5825cad62d8e9e0c7300
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104030933"
---
# <a name="what-was-new-in-windows-media-player-11"></a>Nouveautés de Windows Media Player 11

Cette rubrique répertorie les fonctionnalités qui ont été introduites dans le lecteur Windows Media 11 et le kit de développement logiciel (SDK) du lecteur Windows Media 11.

## <a name="windows-media-player-control"></a>Contrôle du lecteur Windows Media

Les interfaces suivantes ont été introduites dans le contrôle ActiveX du lecteur Windows Media 11.

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

## <a name="windows-media-player-skins"></a>Apparences du lecteur Windows Media

Les fonctionnalités d’apparence suivantes ont été introduites dans le lecteur Windows Media 11.

-   Nouveaux attributs pour positionner les contrôles. Consultez [**AmbientAttributes. Right**](ambientattributes-right.md) et [**AmbientAttributes. Bottom**](ambientattributes-bottom.md).
-   Nouveaux attributs pour le déplacement et le redimensionnement des contrôles. Consultez [**AmbientAttributes. moveSizeTo**](ambientattributes-movesizeto.md) et [**AmbientAttributes. slideTo**](ambientattributes-slideto.md).
-   Nouvel attribut permettant de spécifier le comportement de redimensionnement d’image. Consultez [**AmbientAttributes. resizeImages**](ambientattributes-resizeimages.md).
-   Nouvel attribut permettant de spécifier la mise à l’échelle non uniforme d’un élément d’apparence. Consultez [**AmbientAttributes. nineGridMargins**](ambientattributes-ninegridmargins.md).

## <a name="windows-media-player-plug-ins"></a>Plug-ins du lecteur Windows Media

Le kit de développement logiciel (SDK) du lecteur Windows Media 11 a introduit un nouveau type de plug-in pour la conversion des formats de fichiers multimédias numériques. Consultez [plug-ins de conversion du lecteur Windows Media](windows-media-player-conversion-plug-ins.md).

Les plug-ins DSP créés avant le lancement du kit de développement logiciel (SDK) du lecteur Windows Media 11 doivent être mis à jour pour fonctionner avec le lecteur Windows Media 11. Consultez [mise à jour des plug-ins DSP existants](updating-existing-dsp-plug-ins.md).

L’Assistant de plug-in du lecteur Windows Media a été mis à jour pour créer des plug-ins DSP qui fonctionnent dans le lecteur Windows Media 11. Pour plus d’informations, consultez [mises à jour de l’Assistant de plug-in DSP pour le lecteur Windows Media 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).

## <a name="windows-media-player-online-stores"></a>Windows Media Player Online stores

Le lecteur Windows Media 11 a introduit un nouveau modèle d’intégration des catalogues de magasin en ligne dans la fonctionnalité de la bibliothèque du lecteur Windows Media. Consultez [types 1 magasins en ligne](type-1-online-stores.md).

## <a name="windows-media-player"></a>Lecteur Windows Media

Les fonctionnalités suivantes ont été introduites dans le lecteur Windows Media 11.

-   [Extensions d’appareil pour la création de rapports sur le contenu acquis](device-extensions-for-reporting-acquired-content.md)
-   [Extensions d’appareil pour les préférences de l’objet playlist](device-extensions-for-playlist-object-preferences.md)

## <a name="windows-media-player-sdk-samples"></a>Exemples du kit de développement logiciel (SDK) Windows Media Player

L’exemple C# nommé SchemaReader a été nouveau dans le kit de développement logiciel (SDK) du lecteur Windows Media 11. L’exemple crée un outil qui utilise le modèle objet du lecteur Windows Media pour récupérer et afficher des informations sur les métadonnées dans la bibliothèque du lecteur Windows Media ou dans un fichier multimédia numérique. L’outil peut enregistrer les résultats dans un fichier texte. L’outil énumère les noms d’attributs de métadonnées stockés dans la bibliothèque pour chaque schéma pris en charge (audio, vidéo, sélection, photo, etc.). L’outil peut également fournir des informations sur les attributs disponibles pour les sélections dans la collection de sélections, les pistes de CD, les sommaires de CD, les titres de DVD, les chapitres DVD, la table des matières DVD et les fichiers multimédias individuels.

L’exemple C++ nommé WMPML a été mis à jour dans le kit de développement logiciel (SDK) lecteur Windows Media 11 pour illustrer les fonctionnalités suivantes :

-   À l’aide de la nouvelle interface [**IWMPStringCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2) pour créer une interface utilisateur similaire à la fonctionnalité de la bibliothèque du lecteur Windows Media.
-   Utilisation des interfaces [**IWMPQuery**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery) et [**IWMPMediaCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2) pour créer des requêtes composées et afficher les résultats.

 

 




