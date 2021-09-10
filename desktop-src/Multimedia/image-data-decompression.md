---
title: Décompression Image-Data
description: Décompression Image-Data
ms.assetid: 4bff02be-dac8-41f4-a3af-2da6a2693ffe
keywords:
- Video Compression Manager (VCM), décompression des données d’image
- VCM (gestionnaire de compression vidéo), décompression des données d’image
- ICDecompressEx, fonctions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25614f157436056f7f24c340f6cc6f4dbc62d9ae
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369023"
---
# <a name="image-data-decompression"></a>Décompression Image-Data

Votre application utilise une série de fonctions [**ICDecompressEx**](/windows/desktop/api/Vfw/nf-vfw-icdecompressex) pour contrôler le décompresseur. Les fonctions peuvent vous aider à effectuer les tâches suivantes :

-   Sélectionnez un décompresseur.
-   Préparez le décompresseur.
-   Décompressez les données.
-   Fin de la décompression.

Votre application gère la décompression de la même manière qu’elle gère la compression, à la différence près que le format d’entrée est un format compressé et que le format de sortie est affichable. Le format d’entrée de la décompression est généralement obtenu à partir de l’en-tête de flux. Après avoir déterminé le format d’entrée, votre application peut utiliser les fonctions [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) ou [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) pour trouver un décompresseur qui peut le gérer.

Les fonctions et macros [**ICDecompressEx**](/windows/desktop/api/Vfw/nf-vfw-icdecompressex) sont un sur-ensemble du groupe de fonctions [**ICDecompress**](/windows/desktop/api/Vfw/nf-vfw-icdecompress) et fournissent davantage de fonctionnalités. Les fonctionnalités de **ICDecompressEx**, [**ICDecompressExBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin), [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend)et [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery) remplacent celles des fonctions **ICDecompress**, [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin), [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend)et [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) . Utilisez les fonctions et macros **ICDecompressEx** à la place des équivalents **ICDecompress** .

## <a name="decompressor-and-decompression-format-selection"></a>Sélection du format décompresseur et décompression

Si vous souhaitez décompresser des données et que votre application requiert un format de sortie spécifique, vous pouvez utiliser la fonction [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery) pour interroger le décompresseur afin de déterminer s’il prend en charge les formats d’entrée et de sortie.

Si le format de sortie n’est pas important dans votre application, il vous suffit de trouver un décompresseur pouvant gérer le format d’entrée. Pour déterminer si un décompresseur peut gérer le format d’entrée, utilisez [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery) et spécifiez **null** pour le paramètre *lpbiDst* . votre application peut déterminer la taille de mémoire tampon nécessaire pour les données qui spécifient le format de décompression en envoyant le message de [**format d’extraction de ICM \_ décompresser \_ \_**](icm-decompress-get-format.md) (ou en utilisant la macro [**ICDecompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) ). vous pouvez également envoyer des **ICM \_ décompressez le \_ \_ format d’extraction** (ou la macro [**ICDecompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) ) pour récupérer les données de format. Le décompresseur retourne son format suggéré dans une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) . Ce format préserve généralement le plus d’informations lors de la décompression. Votre application doit s’assurer que le décompresseur est correctement retourné avant de décompresser les informations.

Étant donné que votre application alloue la mémoire requise pour la décompression, elle doit déterminer la mémoire maximale que le décompresseur peut exiger pour le format de sortie. le message de **\_ format d' \_ obtention \_ de décompression ICM** obtient le nombre d’octets que le décompresseur utilise pour le format par défaut.

Si votre application définit son propre format à l’aide de [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery), elle doit également obtenir une palette pour l’image bitmap. **ICDecompressExQuery** ne fournit pas de définitions de palette. (La plupart des applications utilisent des formats standard et n’ont pas besoin d’obtenir une palette.) votre application peut obtenir la palette en envoyant le message [**ICM \_ décompresser \_ obtenir la \_ palette**](icm-decompress-get-palette.md) (ou utiliser la macro [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) ).

## <a name="decompressor-initialization"></a>Initialisation du décompresseur

Une fois que votre application a sélectionné un décompresseur qui peut gérer les formats d’entrée et de sortie dont elle a besoin, vous pouvez initialiser le décompresseur à l’aide de la fonction [**ICDecompressExBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin) . Cette fonction requiert le handle de décompresseur et les formats d’entrée et de sortie.

## <a name="data-decompression"></a>Décompression des données

Vous pouvez utiliser la fonction [**ICDecompressEx**](/windows/desktop/api/Vfw/nf-vfw-icdecompressex) pour décompresser un frame. Votre application doit utiliser cette fonction à plusieurs reprises jusqu’à ce que tous les frames d’une séquence soient décompressés.

Si votre flux vidéo est en retard par rapport à d’autres composants (tels que l’audio) pendant la lecture, votre application peut spécifier l’indicateur **ICDECOMPRESS \_ HURRYUP** pour accélérer la décompression. Pour ce faire, un décompresseur peut extraire uniquement les informations dont il a besoin pour décompresser le frame suivant et ne pas décompresser complètement le frame actuel. Par conséquent, votre application ne doit pas essayer de dessiner les données décompressées lorsqu’elle utilise cet indicateur.

une fois que votre application a décompressé les données, elle peut envoyer le message [**ICM \_ DECOMPRESSEX \_ END**](icm-decompressex-end.md) (ou utiliser la macro [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend) ) pour notifier le décompresseur qu’il est terminé. Si vous souhaitez redémarrer la décompression après avoir utilisé cette fonction, votre application doit réinitialiser le décompresseur à l’aide de [**ICDecompressExBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Services VCM](vcm-services.md)
</dt> </dl>

 

 