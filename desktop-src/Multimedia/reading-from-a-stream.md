---
title: Lire à partir d’un flux
description: Lire à partir d’un flux
ms.assetid: be961f06-cf5f-4093-9b31-7d1d69e62fec
keywords:
- AVIStreamInfo fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cc7ecd606a33503557e7c7209bff68015756523
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940988"
---
# <a name="reading-from-a-stream"></a>Lire à partir d’un flux

Vous pouvez récupérer des informations sur un flux ouvert à l’aide de la fonction [**AVIStreamInfo**](/windows/desktop/api/Vfw/nf-vfw-avistreaminfoa) . Cette fonction remplit la structure [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) avec des informations telles que le type de données dans le flux, la méthode de compression utilisée lors de l’écriture de données de flux, la taille de mémoire tampon suggérée, la vitesse de lecture et une description textuelle du flux.

Certains membres de la structure [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) sont également présents dans la structure [**AVIFILEINFO**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) . Les informations de la structure **AVIFILEINFO** s’appliquent à l’ensemble du fichier. Les informations contenues dans la structure **AVISTREAMINFO** sont spécifiques au flux d’accès et ont la priorité sur les informations de la structure **AVIFILEINFO** .

Si un flux contient des informations supplémentaires qui lui sont associées, vous pouvez récupérer ces informations à l’aide de la fonction [**AVIStreamReadData**](/windows/desktop/api/Vfw/nf-vfw-avistreamreaddata) . Cette fonction retourne les informations dans une mémoire tampon fournie par l’application. Les informations de flux supplémentaires peuvent inclure des paramètres de configuration pour les méthodes de compression et de décompression utilisées sur un flux. Vous pouvez obtenir la taille de mémoire tampon requise à l’aide de la macro [**AVIStreamDataSize**](/windows/desktop/api/Vfw/nf-vfw-avistreamdatasize) .

Vous pouvez récupérer les informations de mise en forme d’un flux à l’aide de la fonction [**AVIStreamReadFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamreadformat) . Cette fonction retourne une structure spécifique au flux dans une mémoire tampon fournie par l’application. Pour un flux vidéo, la mémoire tampon contient des informations de mise en forme dans une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) . Pour un flux audio, la mémoire tampon contient des informations de mise en forme dans une structure [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) ou [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) . Pour les autres types de flux, le gestionnaire de flux retourne des informations spécifiques au flux. Vous pouvez déterminer la taille de mémoire tampon requise en utilisant **AVIStreamReadFormat** et en spécifiant une adresse de mémoire tampon **null** ou à l’aide de la macro [**AVIStreamFormatSize**](/windows/desktop/api/Vfw/nf-vfw-avistreamformatsize) .

Vous pouvez récupérer le contenu multimédia dans un flux à l’aide de la fonction [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) . Cette fonction copie les données brutes du flux dans une mémoire tampon fournie par l’application. Pour les flux vidéo, cette fonction récupère les images bitmap qui composent le contenu du cadre. Pour les flux audio, cette fonction récupère les exemples Waveform Audio qui composent le contenu du son. Vous pouvez déterminer la taille de mémoire tampon requise en utilisant **AVIStreamRead** et en spécifiant une adresse de mémoire tampon **null** ou à l’aide de la macro [**AVIStreamSampleSize**](/windows/desktop/api/Vfw/nf-vfw-avistreamsamplesize) .

Certains gestionnaires de flux AVI présentent des retards associés à l’initialisation ou à la coordination des logiciels et du matériel. Vous pouvez informer ces gestionnaires pour préparer la diffusion de données en continu à l’aide de la fonction [**AVIStreamBeginStreaming**](/windows/desktop/api/Vfw/nf-vfw-avistreambeginstreaming) . Cette fonction permet au gestionnaire de flux d’allouer et d’initialiser les ressources dont il a besoin. Pour informer ces gestionnaires lorsque la diffusion en continu est terminée, utilisez la fonction [**AVIStreamEndStreaming**](/windows/desktop/api/Vfw/nf-vfw-avistreamendstreaming) . Cette fonction permet au gestionnaire de flux de libérer les ressources qu’il a allouées pour **AVIStreamBeginStreaming**.

La fonction [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) ne fournit pas de services de décompression. Pour plus d’informations sur la compression et la décompression des flux audio, consultez [Gestionnaire de compression audio](audio-compression-manager.md). Pour plus d’informations sur la compression et la décompression des flux vidéo, consultez [Gestionnaire de compression vidéo](video-compression-manager.md). Pour plus d’informations sur la compression et la décompression des frames individuels dans un flux vidéo, consultez [utilisation de données vidéo compressées dans un flux](working-with-compressed-video-data-in-a-stream.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Opérations de flux](stream-operations.md)
</dt> </dl>

 

 