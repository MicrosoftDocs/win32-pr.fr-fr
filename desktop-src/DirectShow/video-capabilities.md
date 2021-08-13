---
description: Fonctionnalités vidéo
ms.assetid: 305bd009-f58e-4dcc-9b70-252de87dc86d
title: Fonctionnalités vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4841f5f33b39adc6bd12775e07085e14886d250cd59c988884ae7ca8a6a21b80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290841"
---
# <a name="video-capabilities"></a>Fonctionnalités vidéo

La méthode [**IAMStreamConfig :: GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) présente des fonctionnalités vidéo dans un tableau de paires de structures d' [**\_ \_ \_ embouts de configuration de flux vidéo**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) et de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Vous pouvez l’utiliser pour exposer tous les formats et résolutions pris en charge sur un code confidentiel, comme indiqué ci-dessous.

Pour obtenir des exemples liés à l’audio de **GetStreamCaps**, consultez [fonctionnalités audio](audio-capabilities.md).

Supposons que votre carte de capture prend en charge le format JPEG à toutes les résolutions entre 160 x 120 pixels et 320 x 240 pixels, inclus. Dans ce cas, la différence entre les résolutions prises en charge est le suivant : vous pouvez ajouter ou soustraire un pixel de chaque résolution prise en charge pour bénéficier de la résolution prise en charge suivante. Cette différence dans les résolutions prises en charge est appelée granularité.

Supposons que votre carte prenne également en charge la taille 640 x 480. L’exemple suivant illustre cette résolution unique et la plage de résolutions ci-dessus (toutes les tailles comprises entre 160 x 120 pixels et 320 x 240 pixels).

![résolution de 160 x 120 à 320 x 240 pixels, plus 640 x 480](images/strmcap1.png)

Par ailleurs, supposez qu’il prend en charge le format RVB de couleur 24 bits à des résolutions comprises entre 160 x 120 et 320 x 240, mais avec une granularité de 8. L’illustration suivante montre certaines des tailles valides dans ce cas.

![résolution de 160 x 120 à 320 à 240, avec une granularité égale à 8](images/strmcap3.png)

Pour en faire une autre façon et en répertoriant davantage de résolutions, les éléments suivants se trouvent dans la liste des résolutions valides.

-   160 x 120
-   168 x 120
-   168 x 128
-   176 x 128
-   176 x 136
-   ... résolutions supplémentaires...
-   312 x 232
-   320 x 240

Utilisez **GetStreamCaps** pour exposer ces fonctionnalités de format et de dimension en offrant un type de média 320 x 240 JPEG (s’il s’agit de votre taille par défaut ou par défaut) associé aux fonctionnalités minimales de 160 x 120, aux capacités maximales de 320 x 240 et à une granularité de 1. La paire suivante que vous exposez à l’aide de **GetStreamCaps** est un type de média 640 x 480 JPEG couplé avec au minimum 640 x 480 et un maximum de 640 x 480 et une granularité de 0. La troisième paire comprend un type de support 320 x 240, RGB 24 bits avec des fonctionnalités minimales de 160 x 120, des capacités maximales de 320 x 240 et une granularité de 8. De cette façon, vous pouvez publier presque tout le format et les capacités que votre carte peut prendre en charge. Une application qui doit connaître les formats de compression que vous fournissez peut obtenir toutes les paires et dresser la liste de tous les sous-types uniques des types de médias.

Un filtre obtient ses rectangles source de type de média et cible à partir des membres **rcSource** et **rcTarget** de la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , respectivement. Les filtres n’ont pas besoin de prendre en charge les rectangles source et cible.

Le rectangle de rognage décrit dans la documentation [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) est le même que le rectangle **rcSource** de la structure **VIDEOINFOHEADER** pour la broche de sortie.

Le rectangle de sortie décrit dans la documentation **IAMStreamConfig** est le même que celui des membres **bilargeur** et **biheight** de la structure **BITMAPINFOHEADER** du code confidentiel de sortie (consultez [données DV dans le format de fichier AVI](dv-data-in-the-avi-file-format.md)).

Si la broche de sortie d’un filtre est connectée à un type de média avec des rectangles sources et cibles non vides, votre filtre est requis pour étirer le sous-rectangle source du format d’entrée dans le sous-rectangle cible du format de sortie. Le sous-rectangle source est stocké dans le membre **Inputs** de la structure de [**\_ configuration de flux \_ \_ vidéo**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) .

Par exemple, considérez le scénario de compresseur vidéo suivant : l’image d’entrée est au format RVB et a une taille de 160 x 120 pixels. L’angle supérieur gauche du rectangle source est à la coordonnée (20, 20) et son coin inférieur droit est à (30, 30). L’image de sortie est au format MPEG avec une taille de 320 x 240. L’angle supérieur gauche du rectangle cible se trouve à (0,0) et son coin inférieur droit est à (100 100). Dans ce cas, le filtre doit prendre une partie de 10 x 10 de l’image bitmap source RVB 160 x 120, et le faire remplir la première zone de 100 x 100 d’une image bitmap 320 x 240, laissant le reste de la bitmap 320 x 240 intact. L’illustration suivante montre ce scénario.

![étirement de sous-rectangles](images/strmcap4.png)

Un filtre ne prend peut-être pas en charge cette opération et peut échouer pour se connecter à un type de média où **rcSource** et **rcTarget** ne sont pas vides.

La structure **VIDEOINFOHEADER** expose des informations sur les capacités de débit de données d’un filtre. Par exemple, supposons que vous avez connecté votre broche de sortie au filtre suivant avec un certain type de média (soit directement, soit à l’aide du type de support passé par la fonction [**CMediaType :: SetFormat**](cmediatype-setformat.md) ). Examinez le membre **dwBitRate** de la structure de format **VIDEOINFOHEADER** de ce type de média pour déterminer le débit de données à partir duquel vous souhaitez compresser la vidéo. Si vous multipliez le nombre d’unités de temps par Frame dans le membre **AvgTimePerFrame** de la structure **VIDEOINFOHEADER** par le débit de données dans le membre **dwBitRate** et divisez par 10 millions (nombre d’unités par seconde), vous pouvez déterminer le nombre d’octets de chaque trame. Vous pouvez produire un cadre de taille inférieure, mais jamais un plus grand. Pour déterminer la fréquence d’images d’un compresseur vidéo ou d’un filtre de capture, utilisez **AvgTimePerFrame** à partir du type de média de votre broche de sortie.

 

 



