---
title: Compression Image-Data
description: Compression Image-Data
ms.assetid: 689cf403-cbb5-4ccb-a05b-0caa617430ed
keywords:
- Video Compression Manager (VCM), compression des données d’image
- VCM (gestionnaire de compression vidéo), compression des données d’image
- ICCompress fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8f59a163a9b5a74d2d2fe984417069985fa86a
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369007"
---
# <a name="image-data-compression"></a>Compression Image-Data

Votre application peut utiliser une série de fonctions et de macros [**ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) pour compresser les données. Les fonctions et les macros peuvent vous aider à effectuer les tâches suivantes :

-   Déterminez le format de compression à utiliser pour un format d’entrée spécifié.
-   Préparez le compresseur.
-   Compressez les données.
-   Fin de la compression.

Votre application peut augmenter le contrôle du processus de compression à l’aide des fonctions et macros [**ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) . Ce groupe de fonctions et de macros gère des frames individuels, plutôt que l’ensemble de la séquence. Par exemple, votre application peut identifier les frames à compresser en tant qu’images clés à l’aide de la fonction **ICCompress** .

Un compresseur reçoit des données dans un format, compresse les données et retourne une version compressée des données à l’aide d’un format spécifié. Le format d’entrée standard spécifie les DIB à l’aide de la structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) . Le format de sortie standard spécifie les DIB compressés, également à l’aide de la structure **BITMAPINFO,** .

> [!Note]  
> Pour réduire la dégradation de l’image et du son lors de la lecture, évitez de compresser un fichier AVI plusieurs fois. Combinez des éléments vidéo non compressés dans votre système de montage, puis compressez le produit final.

 

## <a name="compressor-and-compression-format-selection"></a>Sélection du format de compression et du compresseur

si vous souhaitez compresser des données et que votre application requiert un format de sortie spécifique, envoyez le message de [**ICM \_ compresser la \_ requête**](icm-compress-query.md) (ou utilisez la macro [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) ) pour interroger le compresseur et déterminer s’il prend en charge les formats d’entrée et de sortie.

Si le format de sortie n’est pas important pour votre application, il vous suffit de trouver un compresseur pouvant gérer le format d’entrée. pour déterminer si un compresseur peut gérer le format d’entrée, vous pouvez **envoyer \_ ICM \_ requête COMPRESS**, en spécifiant **NULL** pour le paramètre *lParam* . Ce message ne retourne pas le format de sortie de votre application. votre application peut déterminer la taille de mémoire tampon nécessaire pour les données qui spécifient le format de compression en envoyant le message [**ICM \_ compresser \_ obtenir le \_ format**](icm-compress-get-format.md) (ou en utilisant la macro [**ICCompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize) ). vous pouvez également récupérer les données de format en envoyant ICM \_ format d’extraction de compression \_ \_ (ou la macro [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) ).

si vous souhaitez déterminer la plus grande mémoire tampon que le compresseur peut nécessiter pour la compression, envoyez le message [**ICM \_ compression \_ obtenir la \_ taille**](icm-compress-get-size.md) (ou utilisez la macro [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) ). Vous pouvez utiliser le nombre d’octets retournés par la fonction [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) pour allouer une mémoire tampon pour les compressions d’image ultérieures.

## <a name="compressor-initialization"></a>Initialisation du compresseur

une fois que votre application a sélectionné un compresseur capable de gérer les formats d’entrée et de sortie dont elle a besoin, vous pouvez initialiser le compresseur à l’aide du message [**ICM \_ compresser \_ BEGIN**](icm-compress-begin.md) (ou utiliser la macro [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) ). Ce message requiert le descripteur de compresseur et les formats d’entrée et de sortie.

## <a name="data-compression"></a>Data Compression

Vous pouvez utiliser la fonction [**ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) pour compresser un frame. Votre application doit utiliser cette fonction à plusieurs reprises jusqu’à ce que tous les frames d’une séquence soient compressés. Votre application doit également suivre et incrémenter le nombre de chaque frame compressé avec **ICCompress**. Le compresseur utilise cette valeur pour vérifier si les trames sont envoyées dans le désordre pendant la compression temporelle rapide (stockage des différences entre les images consécutives). Si votre application recompresse un frame, elle doit utiliser le même numéro de frame que lorsque le frame a été compressé pour la première fois. Si votre application compresse une image de cadre continu, elle peut spécifier un nombre d’images égal à zéro.

Votre application peut utiliser l' **indicateur \_ KeyFrame ICCOMPRESS** pour que le frame compressé par [**ICCOMPRESS**](/windows/desktop/api/Vfw/nf-vfw-iccompress) une image clé.

Lorsque VCM renvoie le contrôle à votre application après la compression d’un frame, VCM stocke les données compressées dans les structures référencées par les paramètres *lpbiOutput* et *lpData* . Si votre application a besoin de déplacer les données compressées, elle peut trouver sa taille dans le membre *biSizeImage* de la structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) spécifiée dans *lpbiOutput*.

> [!Note]  
> Votre application doit allouer les structures et les tampons qui stockent les données non compressées et compressées. Si le compresseur prend en charge la compression temporelle, votre application doit également allouer une structure et une mémoire tampon pour stocker le format et les données de la trame d’informations précédente.

 

## <a name="ending-compression"></a>Compression de fin

Une fois que votre application a compressé les données, elle peut utiliser la macro [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) pour informer le compresseur qu’elle est terminée. si vous souhaitez redémarrer la compression après avoir utilisé cette fonction, votre application doit réinitialiser le compresseur en envoyant le message [**de \_ \_ début de la compression ICM**](icm-compress-begin.md) (ou en utilisant la macro [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) ).

 

 