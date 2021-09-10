---
title: Utilisation de données vidéo compressées dans un flux
description: Utilisation de données vidéo compressées dans un flux
ms.assetid: b701e072-f162-438f-b607-aea7491a02f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0587ee6c12a93eb014368642ba1605f546129e0
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369300"
---
# <a name="working-with-compressed-video-data-in-a-stream"></a>Utilisation de données vidéo compressées dans un flux

AVIFile offre plusieurs moyens d’accéder à des flux vidéo compressés.

Si vous souhaitez afficher une ou plusieurs images d’un flux vidéo compressé, vous pouvez récupérer les frames à l’aide de la fonction [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) et transférer les données de frame compressées aux fonctions DrawDib pour les afficher. Les fonctions DrawDib peuvent afficher des images de plusieurs profondeurs d’images et détramer automatiquement les images pour les affichages qui ne peuvent pas gérer certains types de bitmaps indépendantes du périphérique (DIB). Ces fonctions fonctionnent avec des images non compressées et compressées. Pour plus d’informations sur les fonctions DrawDib, consultez [fonctions DrawDib](drawdib-functions.md).

AVIFile fournit des fonctions permettant de décompresser une image vidéo unique. Pour allouer des ressources, utilisez la fonction [**AVIStreamGetFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen) . Cette fonction crée une mémoire tampon pour les données décompressées.

Vous pouvez décompresser une seule image vidéo à l’aide de la fonction [**AVIStreamGetFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe) . Cette fonction décompresse le frame et récupère une image complète des données de l’image, en retournant l’adresse du DIB dans la structure [BITMAPINFOHEADER](/previous-versions//ms532290(v=vs.85)) . Votre application peut afficher le DIB à l’aide de fonctions de dessin standard ou à l’aide des fonctions DrawDib.

Si votre application effectue des appels successifs à **AVIStreamGetFrame**, la fonction remplace sa mémoire tampon par chaque frame récupéré.

Lorsque vous avez fini d’utiliser **AVIStreamGetFrame** et que le DIB décompressé est dans sa mémoire tampon, vous pouvez libérer les ressources allouées à l’aide de la fonction [**AVIStreamGetFrameClose**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose) .

Pour plus d’informations sur la décompression d’images, consultez [Gestionnaire de compression vidéo](video-compression-manager.md).

 

 