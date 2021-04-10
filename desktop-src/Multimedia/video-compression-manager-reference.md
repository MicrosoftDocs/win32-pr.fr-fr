---
title: Référence du gestionnaire de compression vidéo
description: Référence du gestionnaire de compression vidéo
ms.assetid: dd678b24-62af-495f-bdd6-3082c1a753dd
keywords:
- Video for Windows (VFW), Video Compression Manager (VCM)
- VFW (vidéo pour Windows), gestionnaire de compression vidéo (VCM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c801df7ecdf0f6468762c2742235d4ef627f5aee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190947"
---
# <a name="video-compression-manager-reference"></a>Référence du gestionnaire de compression vidéo

Cette section décrit les fonctions, structures, messages et macros associés à VCM. Ces éléments sont regroupés comme suit.

## <a name="compressor-installation-and-removal"></a>Installation et suppression du compresseur

-   [**ICInstall**](/windows/desktop/api/Vfw/nf-vfw-icinstall)
-   [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [**ICOPEN**](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose)
-   [**ICRemove**](/windows/desktop/api/Vfw/nf-vfw-icremove)
-   [**ICOpenFunction**](/windows/desktop/api/Vfw/nf-vfw-icopenfunction)

## <a name="locating-and-opening-a-compressor"></a>Localisation et ouverture d’un compresseur

-   [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [**ICOPEN**](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [**ICDecompressOpen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen)
-   [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose)

## <a name="selecting-compressors"></a>Sélection de compresseurs

-   [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)
-   [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree)
-   [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars)

## <a name="configuring-compressors"></a>Configuration des compresseurs

-   [**\_configuration ICM**](icm-configure.md)
-   [**\_GETSTATE ICM**](icm-getstate.md)
-   [**de \_ la CCI.**](icm-setstate.md)
-   [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage)

## <a name="compressor-information"></a>Informations sur le compresseur

-   [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [**\_GETDEFAULTKEYFRAMERATE ICM**](icm-getdefaultkeyframerate.md)
-   [**ICGetDisplayFormat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat)
-   [**\_GETDEFAULTQUALITY ICM**](icm-getdefaultquality.md)
-   [**ICM \_ à propos de**](icm-about.md)

## <a name="single-image-compression"></a>Compression d’image unique

-   [**ICImageCompress**](/windows/desktop/api/Vfw/nf-vfw-icimagecompress)

## <a name="sequence-compression"></a>Compression de séquence

-   [**ICSeqCompressFrame**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe)
-   [**ICSeqCompressFrameStart**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart)
-   [**ICSeqCompressFrameEnd**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend)

## <a name="compvars"></a>COMPVARS

-   [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)

## <a name="image-data-compression"></a>Compression des données d’image

-   [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress)
-   [**FORMAT d’extraction de la \_ compression ICM \_ \_**](icm-compress-get-format.md)
-   [**\_requête de compression ICM \_**](icm-compress-query.md)
-   [**taille d’extraction de la \_ compression ICM \_ \_**](icm-compress-get-size.md)
-   [**début de la \_ compression ICM \_**](icm-compress-begin.md)
-   [**fin de la \_ compression ICM \_**](icm-compress-end.md)

## <a name="compressor-monitoring"></a>Analyse du compresseur

-   [**ICSETSTATUSPROC**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc)

## <a name="decompressing-single-images"></a>Décompression d’images uniques

-   [**ICImageDecompress**](/windows/desktop/api/Vfw/nf-vfw-icimagedecompress)

## <a name="decompressing-image-data"></a>Décompression des données d’image

-   [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)
-   [**ICDecompressExBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin)
-   [**\_fin de DECOMPRESSEX ICM \_**](icm-decompressex-end.md)
-   [**FORMAT d’extraction de la \_ décompression ICM \_ \_**](icm-decompress-get-format.md)
-   [**\_DÉcompresser \_ la \_ palette ICM**](icm-decompress-get-palette.md)
-   [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery)
-   [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress)
-   [**début de la \_ décompression ICM \_**](icm-decompress-begin.md)
-   [**\_fin de décompression ICM \_**](icm-decompress-end.md)
-   [**\_requête de décompression ICM \_**](icm-decompress-query.md)

## <a name="using-hardware-drawing-capabilities"></a>Utilisation des fonctionnalités de Hardware-Drawing

-   [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin)
-   [**\_fin de dessin ICM \_**](icm-draw-end.md)
-   [**\_vidage de dessin ICM \_**](icm-draw-flush.md)
-   [**requête ICM de \_ dessin \_**](icm-draw-query.md)
-   [**ICDrawSuggestFormat**](/windows/desktop/api/Vfw/nf-vfw-icdrawsuggestformat)
-   [**\_début de dessin ICM \_**](icm-draw-start.md)
-   [**\_arrêter le dessin ICM \_**](icm-draw-stop.md)
-   [**\_GETBUFFERSWANTED ICM**](icm-getbufferswanted.md)
-   [**ICM- \_ créer \_**](icm-draw-realize.md)
-   [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw)
-   [**ICM de \_ dessin ICM \_**](icm-draw-gettime.md)
-   [**ICM \_ dessin \_ setTime**](icm-draw-settime.md)
-   [**\_fenêtre de dessin ICM \_**](icm-draw-window.md)
-   [**ICM- \_ créer \_**](icm-draw-realize.md)
-   [**\_CHANGEPALETTE de dessin ICM \_**](icm-draw-changepalette.md)
-   [**\_RENDERBUFFER de dessin ICM \_**](icm-draw-renderbuffer.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestionnaire de compression vidéo](video-compression-manager.md)
</dt> </dl>

 

 




