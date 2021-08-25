---
description: Utilisation du récepteur multimédia EVR
ms.assetid: cd98266a-bc62-43da-b4d7-3561447d634f
title: Utilisation du récepteur multimédia EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ced80b4f9ee17093a00436a26f3f142281907597191791712fd6900520926ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826289"
---
# <a name="using-the-evr-media-sink"></a>Utilisation du récepteur multimédia EVR

Le récepteur multimédia EVR (Enhanced Video Renderer) peut être utilisé en tant que composant autonome. Toutefois, plus souvent, une application crée le récepteur multimédia EVR à l’intérieur d’une topologie, puis utilise la session multimédia pour contrôler la lecture.

Il existe deux façons de créer le récepteur multimédia EVR :

-   La fonction [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) crée le récepteur multimédia.

-   La fonction [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) crée un objet d’activation pour le récepteur multimédia.

Le récepteur multimédia EVR a initialement un récepteur de flux, qui correspond au flux de référence. Pour ajouter de nouveaux récepteurs de flux, appelez [**IMFMediaSink :: AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Convertisseur vidéo amélioré](enhanced-video-renderer.md)
</dt> <dt>

[Récepteurs de médias](media-sinks.md)
</dt> </dl>

 

 



