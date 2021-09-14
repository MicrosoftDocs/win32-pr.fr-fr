---
title: Nouveautés de Windows Media Player 12
description: cette rubrique répertorie les nouvelles fonctionnalités de Lecteur Windows Media 12.
ms.assetid: 17f76963-c96d-46c9-82c0-3ed2d8a4e892
keywords:
- Lecteur Windows Media, nouveautés
- Lecteur Windows Media, nouvelles fonctionnalités
- kit de développement logiciel (SDK), Lecteur Windows Media 12
- SDK (kit de développement logiciel), Lecteur Windows Media 12
- documentation, Lecteur Windows Media 12 SDK
- nouveautés, Lecteur Windows Media 12
- nouvelles fonctionnalités, Lecteur Windows Media 12
- interfaces, nouvelles fonctionnalités de Lecteur Windows Media 12
- attributs, nouvelles fonctionnalités dans Lecteur Windows Media 12
- métadonnées, nouvelles fonctionnalités de Lecteur Windows Media 12
- énumérations, nouvelles fonctionnalités de Lecteur Windows Media 12
- indicateurs, nouvelles fonctionnalités de Lecteur Windows Media 12
- interfaces, dépréciées dans Lecteur Windows Media 12
- méthodes, dépréciées dans Lecteur Windows Media 11 et non 12
- versions de Lecteur Windows Media, nouvelles fonctionnalités de la version 12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16b21077df1f4a9c11edbfa20032ed473f872a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193112"
---
# <a name="whats-new-in-windows-media-player-12"></a>Nouveautés de Windows Media Player 12

cette rubrique répertorie les nouvelles fonctionnalités de Lecteur Windows Media 12.

## <a name="new-interfaces"></a>Nouvelles interfaces

-   [**IWMPAudioRenderConfig**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [**IWMPEvents4**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [**IWMPLibrary2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [**IWMPSyncDevice3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="new-attributes"></a>Nouveaux attributs

Les nouveaux attributs suivants pour les éléments multimédias sont disponibles par le biais des interfaces [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) et [**IWMPMedia3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3) .

-   [**AlbumCoverURL**](wm-albumcoverurl-attribute.md)
-   [**AlternateSourceURL**](alternatesourceurl-attribute.md)
-   [**DLNASourceURI**](dlnasourceuri-attribute.md)
-   [**DLNAServerUDN**](dlnaserverudn-attribute.md)
-   [**DTCPIPHost**](dtcpiphost-attribute.md)
-   [**DTCPIPPort**](dtcpipport-attribute.md)
-   [**Id_bibliothèque**](libraryid-attribute.md)
-   [**LibraryName**](libraryname-attribute.md)

## <a name="new-device-metadata"></a>Nouvelles métadonnées de l’appareil

Les nouveaux éléments de métadonnées d’appareil suivants peuvent être récupérés en appelant [**IWMPSyncDevice :: getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-getiteminfo).

-   **BackgroundSyncState**
-   **SkippedFiles**
-   **SyncFilter**

Les nouveaux éléments de métadonnées d’appareil suivants peuvent être définis en appelant [**IWMPSyncDevice2 :: setItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo).

-   **AutoSyncDefaultRules**
-   **BackgroundSyncState**
-   **IncludeSkippedFiles**
-   **SyncFilter**
-   **SyncOnConnect**

## <a name="new-enumeration-member"></a>Nouveau membre de l’énumération

L’énumération [**WMPSyncState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate) a le nouveau membre suivant.

-   **wmpssEstimating**

## <a name="new-flag"></a>Nouvel indicateur

La méthode [**IWMPGraphCreation :: GetGraphCreationFlags**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-getgraphcreationflags) prend en charge le nouvel indicateur suivant.

-   **les \_ indicateurs WMPGC \_ utilisent un \_ \_ graphique personnalisé**

## <a name="deprecated-interface"></a>Interface dépréciée

L’interface suivante est déconseillée.

-   [**IWMPFolderMonitorServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)

## <a name="methods-that-are-no-longer-deprecated"></a>Méthodes qui ne sont plus dépréciées

les méthodes suivantes ont été dépréciées dans le kit de développement logiciel (SDK) Lecteur Windows Media 11, mais ne sont plus dépréciées.

-   [**IWMPGraphCreation::GraphCreationPreRender**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationprerender)
-   [**IWMPGraphCreation::GraphCreationPostRender**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationpostrender)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[à propos du kit de développement logiciel (SDK) Lecteur Windows Media](about-the-windows-media-player-sdk.md)
</dt> </dl>

 

 




