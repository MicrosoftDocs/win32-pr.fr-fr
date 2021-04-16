---
title: Plateforme multimédia
description: Media Foundation et DirectShow fournissent la base de la prise en charge des médias dans Windows.
ms.assetid: 020f009c-7432-432b-a39b-9295dd784d2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f756112384451ac3f5b4055d73a60a170b2e29
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508094"
---
# <a name="media-platform"></a>Plateforme multimédia

[Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) et [DirectShow](/windows/desktop/DirectShow/directshow) fournissent la base de la prise en charge des médias dans Windows. Media Foundation a été introduit dans Windows Vista comme remplacement de DirectShow. Dans Windows 7, Media Foundation a été amélioré pour fournir une meilleure prise en charge du format, notamment *MPEG-4*, ainsi que la prise en charge des périphériques de capture vidéo et des codecs matériels.

## <a name="format-support"></a>Prise en charge du format

Dans Windows 7, [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) fournit une prise en charge complète du format qui inclut les codecs pour les vidéos *H. 264* , *MJPEG* et *mp3*. nouvelles sources pour *MP4*, *3GP*, audio *AAC* et *AVI*; et nouveaux récepteurs de fichiers pour *MP4*, *3GP* et *mp3*. (Consultez [formats multimédias pris en charge dans Media Foundation](../medfound/supported-media-formats-in-media-foundation.md).)

## <a name="hardware-devices"></a>Périphériques matériels

[Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) prend désormais en charge les types suivants de périphériques matériels dans le pipeline audio/vidéo :

-   Appareils de capture vidéo *UVC 1,1* , tels que les webcams
-   Périphériques de capture audio
-   Encodeurs et décodeurs matériels
-   Processeurs vidéo matériels, tels que les convertisseurs d’espace colorimétrique

Les codecs matériels peuvent effectuer un transcodage vidéo très rapide. Supposons, par exemple, que vous souhaitiez transférer un fichier *Windows Media Video (WMV)* sur un téléphone portable qui prend uniquement en charge les fichiers *3GP* . Avec un encodeur matériel, le fichier peut être transcodé « en fonction des besoins » immédiatement avant d’être transféré vers l’appareil.

Les périphériques matériels sont représentés en [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) par un objet proxy et sont utilisés dans le pipeline, comme les composants logiciels. (Voir [Nouveautés de Media Foundation](../medfound/whats-new-for-media-foundation.md).)

## <a name="simplified-programming-model"></a>Modèle de programmation simplifié

Dans Windows Vista, [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) exposé un ensemble relativement bas d’API. Ces API sont flexibles, mais elles peuvent ne pas convenir à l’exécution de tâches. Windows 7 ajoute de nouvelles API de haut niveau qui simplifient l’écriture d’applications multimédias en *C++*. Ces nouvelles API de haut niveau sont les suivantes :

-   **MFPlay**. Ces API sont conçues pour la lecture audio et vidéo. Ils prennent en charge les opérations de lecture classiques (arrêter, suspendre, lire, Rechercher, contrôle de débit, volume audio, etc.), tout en masquant les détails des API de bas niveau (couches de session et de topologie).
-   **Lecteur source**. Vous pouvez utiliser ces API pour extraire des données brutes ou décodées d’un fichier multimédia, sans connaître le format sous-jacent. Par exemple, vous pouvez obtenir une image bitmap à partir d’un fichier vidéo ou obtenir des images vidéo en direct à partir d’une webcam.
-   **Enregistreur du récepteur**. Vous pouvez utiliser ces API pour créer des fichiers multimédias en passant des données non compressées ou encodées. Par exemple, vous pouvez recoder ou remixer un fichier vidéo.
-   **Transcodage**. Ces API ciblent les scénarios d’encodage audio et vidéo les plus courants.

## <a name="platform-improvements"></a>Améliorations de la plateforme

Windows 7 comprend de nombreuses améliorations des API de plateforme de [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) sous-jacentes. Les applications avancées peuvent utiliser ces API directement. les autres applications bénéficieront des avantages indirects. Les avantages sont les suivants :

-   Améliorations du pipeline vidéo pour réduire la consommation d’énergie et l’utilisation de la mémoire vidéo.
-   Les nouvelles API de traitement vidéo *DVXA* , qui utilisent un modèle de composition plus souple et sont mieux adaptées aux formats vidéo *HD* .
-   Améliorations apportées à la façon dont les plug-ins (sources et décodeurs) sont énumérés et gérés.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Nouveautés de Media Foundation](../medfound/whats-new-for-media-foundation.md)
</dt> </dl>

 

 