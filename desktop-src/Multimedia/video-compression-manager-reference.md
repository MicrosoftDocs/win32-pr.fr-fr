---
title: Référence du gestionnaire de compression vidéo
description: Référence du gestionnaire de compression vidéo
ms.assetid: dd678b24-62af-495f-bdd6-3082c1a753dd
keywords:
- video for Windows (VFW), video compression manager (VCM)
- VFW (vidéo pour Windows), gestionnaire de compression vidéo (VCM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c801df7ecdf0f6468762c2742235d4ef627f5aee
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364099"
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

-   [**ICM \_ CONFIGURER**](icm-configure.md)
-   [**ICM \_ GETSTATE**](icm-getstate.md)
-   [**ICM \_ SETSTATE**](icm-setstate.md)
-   [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage)

## <a name="compressor-information"></a>Informations sur le compresseur

-   [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [**ICM \_ GETDEFAULTKEYFRAMERATE**](icm-getdefaultkeyframerate.md)
-   [**ICGetDisplayFormat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat)
-   [**ICM \_ GETDEFAULTQUALITY**](icm-getdefaultquality.md)
-   [**ICM \_ OBTENIR**](icm-about.md)

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
-   [**ICM \_ \_format d’extraction de compression \_**](icm-compress-get-format.md)
-   [**ICM \_ compresser la \_ requête**](icm-compress-query.md)
-   [**ICM \_ COMPRESSION de la \_ taille d’extraction \_**](icm-compress-get-size.md)
-   [**ICM \_ début de la compression \_**](icm-compress-begin.md)
-   [**ICM \_ compresser la \_ fin**](icm-compress-end.md)

## <a name="compressor-monitoring"></a>Analyse du compresseur

-   [**ICSETSTATUSPROC**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc)

## <a name="decompressing-single-images"></a>Décompression d’images uniques

-   [**ICImageDecompress**](/windows/desktop/api/Vfw/nf-vfw-icimagedecompress)

## <a name="decompressing-image-data"></a>Décompression des données d’image

-   [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)
-   [**ICDecompressExBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin)
-   [**ICM \_ fin de DECOMPRESSEX \_**](icm-decompressex-end.md)
-   [**ICM \_ FORMAT d’extraction de décompression \_ \_**](icm-decompress-get-format.md)
-   [**ICM \_ décompresser l’extraction de la \_ \_ palette**](icm-decompress-get-palette.md)
-   [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery)
-   [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress)
-   [**ICM \_ début de la décompression \_**](icm-decompress-begin.md)
-   [**ICM \_ fin de décompression \_**](icm-decompress-end.md)
-   [**ICM \_ décompresser la \_ requête**](icm-decompress-query.md)

## <a name="using-hardware-drawing-capabilities"></a>Utilisation des fonctionnalités de Hardware-Drawing

-   [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin)
-   [**ICM \_ DESSINER la \_ fin**](icm-draw-end.md)
-   [**ICM \_ DESSINER le \_ vidage**](icm-draw-flush.md)
-   [**ICM \_ CRÉER une \_ requête**](icm-draw-query.md)
-   [**ICDrawSuggestFormat**](/windows/desktop/api/Vfw/nf-vfw-icdrawsuggestformat)
-   [**ICM \_ démarrer le dessin \_**](icm-draw-start.md)
-   [**ICM \_ DESSINER \_ arrêter**](icm-draw-stop.md)
-   [**ICM \_ GETBUFFERSWANTED**](icm-getbufferswanted.md)
-   [**ICM \_ DESSINER \_**](icm-draw-realize.md)
-   [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw)
-   [**ICM \_ DESSINER \_ GETTIME**](icm-draw-gettime.md)
-   [**ICM \_ DESSINER \_ setTime**](icm-draw-settime.md)
-   [**ICM \_ \_fenêtre dessin**](icm-draw-window.md)
-   [**ICM \_ DESSINER \_**](icm-draw-realize.md)
-   [**ICM \_ DESSIN \_ CHANGEPALETTE**](icm-draw-changepalette.md)
-   [**ICM \_ DESSIN \_ RENDERBUFFER**](icm-draw-renderbuffer.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestionnaire de compression vidéo](video-compression-manager.md)
</dt> </dl>

 

 




