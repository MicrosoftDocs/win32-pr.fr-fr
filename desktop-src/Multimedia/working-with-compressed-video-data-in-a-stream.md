---
title: Utilisation de données vidéo compressées dans un flux
description: Utilisation de données vidéo compressées dans un flux
ms.assetid: b701e072-f162-438f-b607-aea7491a02f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0587ee6c12a93eb014368642ba1605f546129e0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031134"
---
# <a name="working-with-compressed-video-data-in-a-stream"></a><span data-ttu-id="a2e30-103">Utilisation de données vidéo compressées dans un flux</span><span class="sxs-lookup"><span data-stu-id="a2e30-103">Working with Compressed Video Data in a Stream</span></span>

<span data-ttu-id="a2e30-104">AVIFile offre plusieurs moyens d’accéder à des flux vidéo compressés.</span><span class="sxs-lookup"><span data-stu-id="a2e30-104">AVIFile provides several ways for you to access compressed video streams.</span></span>

<span data-ttu-id="a2e30-105">Si vous souhaitez afficher une ou plusieurs images d’un flux vidéo compressé, vous pouvez récupérer les frames à l’aide de la fonction [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) et transférer les données de frame compressées aux fonctions DrawDib pour les afficher.</span><span class="sxs-lookup"><span data-stu-id="a2e30-105">If you want to display one or more frames of a compressed video stream, you can retrieve the frames by using the [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) function and forwarding the compressed frame data to DrawDib functions to display them.</span></span> <span data-ttu-id="a2e30-106">Les fonctions DrawDib peuvent afficher des images de plusieurs profondeurs d’images et détramer automatiquement les images pour les affichages qui ne peuvent pas gérer certains types de bitmaps indépendantes du périphérique (DIB).</span><span class="sxs-lookup"><span data-stu-id="a2e30-106">DrawDib functions can display images of several image depths and automatically dither images for displays that cannot handle certain types of device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="a2e30-107">Ces fonctions fonctionnent avec des images non compressées et compressées.</span><span class="sxs-lookup"><span data-stu-id="a2e30-107">These functions work with uncompressed and compressed images.</span></span> <span data-ttu-id="a2e30-108">Pour plus d’informations sur les fonctions DrawDib, consultez [fonctions DrawDib](drawdib-functions.md).</span><span class="sxs-lookup"><span data-stu-id="a2e30-108">For more information about DrawDib functions, see [DrawDib Functions](drawdib-functions.md).</span></span>

<span data-ttu-id="a2e30-109">AVIFile fournit des fonctions permettant de décompresser une image vidéo unique.</span><span class="sxs-lookup"><span data-stu-id="a2e30-109">AVIFile provides functions for decompressing a single video frame.</span></span> <span data-ttu-id="a2e30-110">Pour allouer des ressources, utilisez la fonction [**AVIStreamGetFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen) .</span><span class="sxs-lookup"><span data-stu-id="a2e30-110">To allocate resources, use the [**AVIStreamGetFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen) function.</span></span> <span data-ttu-id="a2e30-111">Cette fonction crée une mémoire tampon pour les données décompressées.</span><span class="sxs-lookup"><span data-stu-id="a2e30-111">This function creates a buffer for the decompressed data.</span></span>

<span data-ttu-id="a2e30-112">Vous pouvez décompresser une seule image vidéo à l’aide de la fonction [**AVIStreamGetFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe) .</span><span class="sxs-lookup"><span data-stu-id="a2e30-112">You can decompress a single video frame by using the [**AVIStreamGetFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe) function.</span></span> <span data-ttu-id="a2e30-113">Cette fonction décompresse le frame et récupère une image complète des données de l’image, en retournant l’adresse du DIB dans la structure [BITMAPINFOHEADER](/previous-versions//ms532290(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a2e30-113">This function decompresses the frame and retrieves a complete frame of image data, returning the address of the DIB in the [BITMAPINFOHEADER](/previous-versions//ms532290(v=vs.85)) structure.</span></span> <span data-ttu-id="a2e30-114">Votre application peut afficher le DIB à l’aide de fonctions de dessin standard ou à l’aide des fonctions DrawDib.</span><span class="sxs-lookup"><span data-stu-id="a2e30-114">Your application can display the DIB by using standard drawing functions or by using the DrawDib functions.</span></span>

<span data-ttu-id="a2e30-115">Si votre application effectue des appels successifs à **AVIStreamGetFrame**, la fonction remplace sa mémoire tampon par chaque frame récupéré.</span><span class="sxs-lookup"><span data-stu-id="a2e30-115">If your application makes successive calls to **AVIStreamGetFrame**, the function overwrites its buffer with each retrieved frame.</span></span>

<span data-ttu-id="a2e30-116">Lorsque vous avez fini d’utiliser **AVIStreamGetFrame** et que le DIB décompressé est dans sa mémoire tampon, vous pouvez libérer les ressources allouées à l’aide de la fonction [**AVIStreamGetFrameClose**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose) .</span><span class="sxs-lookup"><span data-stu-id="a2e30-116">When you finish using **AVIStreamGetFrame** and the decompressed DIB is in its buffer, you can release the allocated resources by using the [**AVIStreamGetFrameClose**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose) function.</span></span>

<span data-ttu-id="a2e30-117">Pour plus d’informations sur la décompression d’images, consultez [Gestionnaire de compression vidéo](video-compression-manager.md).</span><span class="sxs-lookup"><span data-stu-id="a2e30-117">For more information about decompressing images, see [Video Compression Manager](video-compression-manager.md).</span></span>

 

 