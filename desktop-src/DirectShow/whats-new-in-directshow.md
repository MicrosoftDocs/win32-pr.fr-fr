---
description: Nouveautés de DirectShow
ms.assetid: 675a34d4-7a33-4125-86af-cd4ed73ad430
title: Nouveautés de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74747349848a7b370cd4766113085c84d0c7a1d5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238835"
---
# <a name="whats-new-in-directshow"></a>Nouveautés de DirectShow

## <a name="whats-new-for-directshow-in-windows-7"></a>nouveautés de DirectShow dans Windows 7

Nouvelles interfaces :

-   [**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling)
-   [**IAMPluginControl**](/windows/desktop/api/Strmif/nn-strmif-iamplugincontrol)

Filtres nouveaux ou mis à jour :

-   [**Décodeur audio Microsoft MPEG-1/DD/AAC**](microsoft-mpeg-1-dd-audio-decoder.md)
-   [**Décodeur vidéo Microsoft MPEG-2**](microsoft-mpeg-2-video-decoder.md)

Les algorithmes « intelligent Connect » ont été modifiés pour prendre en charge les filtres préférés et bloqués. Pour plus d’informations, consultez [Intelligent connecter](intelligent-connect.md).

Lecture de DVD : nouvelles options pour la méthode [**IDvdControl2 :: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) .

## <a name="whats-new-for-directshow-in-windows-vista"></a>nouveautés de DirectShow dans Windows Vista

-   DirectShow fait maintenant partie du SDK Windows. les en-têtes DirectShow, les bibliothèques, les exemples et les outils ne sont plus inclus dans le kit de développement logiciel (SDK) DirectX.
-   DirectX Video Acceleration (DXVA) 2,0 contient de nombreuses améliorations par rapport à DXVA 1,0.

    -   Le pipeline vidéo matériel a été considérablement amélioré.
    -   Les composants tels que les décodeurs peuvent accéder à la carte DXVA 2,0 directement sans communiquer via le convertisseur vidéo.
    -   Le Gestionnaire de périphériques Direct3D permet aux composants de partager le même appareil Direct3D.

    Pour plus d’informations sur DXVA 2,0, consultez la documentation [DirectX Video Acceleration 2,0](../medfound/directx-video-acceleration-2-0.md) , qui fait partie de la documentation [Microsoft Media Foundation](../medfound/microsoft-media-foundation-sdk.md) .

-   Le [**convertisseur vidéo amélioré**](enhanced-video-renderer-filter.md) (EVR) est un nouveau convertisseur vidéo puissant, qui partage le même modèle de plug-in que la version Media Foundation du EVR. Pour plus d’informations sur EVR, consultez la documentation [Microsoft Media Foundation](../medfound/microsoft-media-foundation-sdk.md) .
-   prise en charge de la capture du modèle WDDM (Windows Vista Display Driver Model). Cette fonctionnalité permet aux filtres de tirer pleinement parti des cartes vidéo avec capture vidéo intégrée, afin de réduire les copies inutiles entre la mémoire vidéo et la mémoire système. Pour plus d’informations, consultez [utilisation de la capture WDDM dans DirectShow](using-wddm-capture-in-directshow.md).
-   Le décodeur audio MPEG-1 Layer II utilise désormais l’arithmétique à virgule flottante pour améliorer la qualité du décodage.
-   Améliorations de la lecture des DVD. pour plus d’informations, consultez [améliorations de la lecture de DVD dans Windows Vista](dvd-playback-enhancements-in-windows-vista.md).
    -   Meilleure prise en charge du mode Astuce : transitions en douceur entre les tarifs ; transitions entre la lecture vers l’avant et vers l’arrière ; prise en charge de la lecture audio pendant l’avance rapide et l’inversion.
    -   Mise en cache améliorée. Les applications peuvent définir la quantité de données que le navigateur DVD lit à l’avance. La définition d’un cache plus large peut prolonger la durée de vie de la batterie et activer la lecture silencieuse (une fois que le lecteur est en mode de rotation). Pour plus d’informations, [**consultez \_ \_ indicateur**](/windows/win32/api/strmif/ne-strmif-dvd_option_flag)de l’option de DVD.
-   Périphériques de point de terminaison audio : les applications peuvent associer le [filtre de convertisseur DirectSound](directsound-renderer-filter.md) à un périphérique de point d’arrêt audio particulier. Les applications peuvent utiliser l’API MMDevice (Media Device) pour énumérer et sélectionner l’appareil de point de terminaison. pour plus d’informations, consultez la documentation de l’API Audio principale dans le SDK Windows.
-   les filtres suivants ont été supprimés de Windows Vista :
    -   [Filtre de récepteur IP BDA](/previous-versions/windows/desktop/mstv/bda-ip-sink-filter)
    -   [Filtre de détourage du bordereau BDA](/previous-versions/windows/desktop/mstv/bda-slip-deframer-filter)
    -   [Filtre de décodeur CC](cc-decoder-filter.md)
    -   [Filtre de codec VBI NABTS/FEC](/previous-versions/windows/desktop/mstv/nabts-fec-vbi-codec-filter)
    -   [Filtre de décompresseur QT](qt-decompressor-filter.md)
    -   [Filtre de l’analyseur de film QuickTime](quicktime-movie-parser-filter.md)
    -   [Filtre de codec WST](wst-codec-filter.md)
    -   [Filtre de décodage WST](wst-decoder-filter.md)
-   le code proxy/stub pour la plupart des interfaces de DirectShow a été déplacé de quartz.dll à proppage.dll. Ce code a été supprimé de quartz.dll, car il n’était pas destiné à être utilisé par des applications. toutefois, il est utile pour le débogage, car il permet à une application de test de se connecter à distance à un graphique de filtre DirectShow dans un autre processus. pour utiliser cette fonctionnalité dans Windows Vista, vous devez d’abord inscrire proppage.dll. cette DLL est disponible dans le répertoire des outils de SDK Windows. (pour plus d’informations, consultez [chargement d’un Graph à partir d’un processus externe](loading-a-graph-from-an-external-process.md).)

 

 
