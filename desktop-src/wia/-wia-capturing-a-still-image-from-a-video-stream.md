---
description: 'Après avoir commencé l’aperçu d’un flux vidéo, appelez la méthode IWiaVideo :: TakePicture de l’interface IWiaVideo pour capturer une image continue à partir de la vidéo de diffusion en continu.'
ms.assetid: 2b8c465b-0dbf-4741-a701-200862cc3de3
title: Capture d’une image continue à partir d’un flux vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be475405f4aa9719514a531a6af0105d7a786f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202894"
---
# <a name="capturing-a-still-image-from-a-video-stream"></a><span data-ttu-id="1fe03-103">Capture d’une image continue à partir d’un flux vidéo</span><span class="sxs-lookup"><span data-stu-id="1fe03-103">Capturing a Still Image from a Video Stream</span></span>

<span data-ttu-id="1fe03-104">Après avoir commencé l’aperçu d’un flux vidéo, appelez la méthode [**IWiaVideo :: TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) de l’interface [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) pour capturer une image continue à partir de la vidéo de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="1fe03-104">After beginning preview of a video stream, call the [**IWiaVideo::TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) method of the [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) interface to capture a still image from the streaming video.</span></span> <span data-ttu-id="1fe03-105">Pour obtenir des instructions sur la façon d’obtenir un pointeur **IWiaVideo** et de commencer l’aperçu de la vidéo en continu, consultez aperçu de la [vidéo](-wia-previewing-video.md).</span><span class="sxs-lookup"><span data-stu-id="1fe03-105">For instructions on how to get an **IWiaVideo** pointer and begin previewing streaming video, see [Previewing Video](-wia-previewing-video.md).</span></span>

<span data-ttu-id="1fe03-106">Quand la méthode [**IWiaVideo :: TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) retourne, le paramètre *pbstrNewImageFilename* contient le chemin d’accès complet et le nom de fichier du fichier image résultant.</span><span class="sxs-lookup"><span data-stu-id="1fe03-106">When the [**IWiaVideo::TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) method returns, the *pbstrNewImageFilename* parameter contains the full path and filename of the resulting image file.</span></span> <span data-ttu-id="1fe03-107">Le fichier est au format JPEG.</span><span class="sxs-lookup"><span data-stu-id="1fe03-107">The file is in JPEG format.</span></span> <span data-ttu-id="1fe03-108">Le répertoire dans lequel le fichier est créé est spécifié par la valeur de la propriété [**IWiaVideo :: ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) de l’interface [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) .</span><span class="sxs-lookup"><span data-stu-id="1fe03-108">The directory in which the file is created is specified by the value of the [**IWiaVideo::ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) property of the [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) interface.</span></span>

> [!Note]  
> <span data-ttu-id="1fe03-109">L’acquisition d’images Windows (WIA) ne prend pas en charge les périphériques vidéo dans Windows Server 2003, Windows Vista ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="1fe03-109">Windows Image Acquisition (WIA) does not support video devices in Windows Server 2003, Windows Vista, or later.</span></span> <span data-ttu-id="1fe03-110">Pour ces versions de Windows, utilisez [DirectShow](/previous-versions//ms783323(v=vs.85)) pour acquérir des images à partir d’une vidéo.</span><span class="sxs-lookup"><span data-stu-id="1fe03-110">For those versions of the Windows, use [DirectShow](/previous-versions//ms783323(v=vs.85)) to acquire images from video.</span></span>

 

 

 
