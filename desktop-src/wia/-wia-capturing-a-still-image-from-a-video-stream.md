---
description: 'Après avoir commencé l’aperçu d’un flux vidéo, appelez la méthode IWiaVideo :: TakePicture de l’interface IWiaVideo pour capturer une image continue à partir de la vidéo de diffusion en continu.'
ms.assetid: 2b8c465b-0dbf-4741-a701-200862cc3de3
title: Capture d’une image continue à partir d’un flux vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af98dc313ddde7f2da160515ab53d31357a6d9cc96e1737ed01767b40fb0e7c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814279"
---
# <a name="capturing-a-still-image-from-a-video-stream"></a>Capture d’une image continue à partir d’un flux vidéo

Après avoir commencé l’aperçu d’un flux vidéo, appelez la méthode [**IWiaVideo :: TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) de l’interface [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) pour capturer une image continue à partir de la vidéo de diffusion en continu. Pour obtenir des instructions sur la façon d’obtenir un pointeur **IWiaVideo** et de commencer l’aperçu de la vidéo en continu, consultez aperçu de la [vidéo](-wia-previewing-video.md).

Quand la méthode [**IWiaVideo :: TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) retourne, le paramètre *pbstrNewImageFilename* contient le chemin d’accès complet et le nom de fichier du fichier image résultant. Le fichier est au format JPEG. Le répertoire dans lequel le fichier est créé est spécifié par la valeur de la propriété [**IWiaVideo :: ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) de l’interface [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) .

> [!Note]  
> Windows l’Acquisition d’images (WIA) ne prend pas en charge les périphériques vidéo dans Windows Server 2003, Windows Vista ou version ultérieure. pour ces versions du Windows, utilisez [DirectShow](/previous-versions//ms783323(v=vs.85)) pour acquérir des images à partir d’une vidéo.

 

 

 
