---
description: La MFT du processeur vidéo est une Microsoft Media Foundation transformation (MFT) qui effectue la conversion colorspace, le redimensionnement vidéo, le désentrelacement, la conversion de la fréquence d’images, la rotation, le rognage, la décompression et la mise en miroir de la vue spatiale gauche et droite.
ms.assetid: 1476995A-9692-4B08-8EF7-7DB6321BEC24
title: MFT du processeur vidéo (Camerauicontrol. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53783b42073414e4dc440546698bf295b404dcc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535383"
---
# <a name="video-processor-mft"></a>MFT du processeur vidéo

La MFT du processeur vidéo est une Microsoft Media Foundation transformation (MFT) qui effectue la conversion colorspace, le redimensionnement vidéo, le désentrelacement, la conversion de la fréquence d’images, la rotation, le rognage, la décompression et la mise en miroir de la vue spatiale gauche et droite.

## <a name="clsid"></a>CLSID

CLSID \_ VideoProcessorMFT

## <a name="interfaces"></a>Interfaces

-   [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IMFVideoProcessorControl**](/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol)

## <a name="input-formats"></a>Formats d’entrée

-   **MFVideoFormat \_ ARGB32**
-   **MFVideoFormat \_ AYUV**
-   **MFVideoFormat \_ I420**
-   **MFVideoFormat \_ IYUV**
-   **MFVideoFormat \_ NV11**
-   **MFVideoFormat \_ NV12**
-   **MFVideoFormat \_ Rgb24**
-   **MFVideoFormat \_ RGB32**
-   **MFVideoFormat \_ RGB555**
-   **MFVideoFormat \_ RGB565**
-   **MFVideoFormat \_ RGB8**
-   **MFVideoFormat \_ UYVY**
-   **MFVideoFormat \_ V410**
-   **MFVideoFormat \_ Y216**
-   **MFVideoFormat \_ Y41P**
-   **MFVideoFormat \_ Y41T**
-   **MFVideoFormat \_ Y42T**
-   **MFVideoFormat \_ YUY2**
-   **MFVideoFormat \_ YV12**
-   **MFVideoFormat \_ YVYU**

## <a name="output-formats"></a>Formats de sortie

-   **MFVideoFormat \_ ARGB32**
-   **MFVideoFormat \_ AYUV**
-   **MFVideoFormat \_ I420**
-   **MFVideoFormat \_ IYUV**
-   **MFVideoFormat \_ NV12**
-   **MFVideoFormat \_ Rgb24**
-   **MFVideoFormat \_ RGB32**
-   **MFVideoFormat \_ RGB555**
-   **MFVideoFormat \_ RGB565**
-   **MFVideoFormat \_ UYVY**
-   **MFVideoFormat \_ Y216**
-   **MFVideoFormat \_ YUY2**
-   **MFVideoFormat \_ YV12**

Toutes les combinaisons de formats d’entrée et de sortie ne sont pas prises en charge. Pour vérifier si une conversion est prise en charge, définissez le type d’entrée, puis appelez [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).

Pour plus d’informations sur ces formats, consultez [GUID sous-type de vidéo](video-subtype-guids.md).

## <a name="remarks"></a>Notes

Une instance du processeur vidéo peut être créée de l’une des manières suivantes :

-   En appelant [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex). Le processeur vidéo est inscrit sous la catégorie de **\_ \_ \_ processeur vidéo de catégorie MFT** .
-   En appelant la fonction COM **CoCreateInstance** en lui transmettant le CLSID CLSID **\_ VideoProcessorMFT**.

Les remarques suivantes concernent l’utilisation des rectangles sources et des rectangles de destination dans la **MFT du processeur vidéo**. Les rectangles source et de destination sont définis avec [**IMFVideoProcessorControl :: SetDestinationRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setdestinationrectangle) et [**SetSourceRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setsourcerectangle) et parfois avec [**IMFMediaEngineEx :: UpdateVideoStream**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-updatevideostream).

-   Le rectangle source doit être aligné et arrondi pour correspondre aux exigences du format de couleur du cadre entré sur le processeur vidéo. Cela est important, car les formats comme 420 et 422 ont des exigences relatives aux dimensions et aux décalages qui peuvent être créés et accessibles. Par exemple, un rectangle source de {1, 0, 319, 240} (gauche, haut, droite, bas) sera arrondi à {2, 0, 320, 240} lorsque le format d’entrée est 420.
-   Les rectangles de destination et source sont toujours fixés pour s’ajuster à l’intérieur de leurs images respectives : le rectangle source dans le frame source et le rectangle de destination dans le frame de destination. Cela signifie que les valeurs négatives ne sont pas significatives, elles sont toujours ancrées à 0.
-   Le rectangle source est dans le système de coordonnées du frame de destination, moins tout rectangle de destination. Cela signifie que les transformations telles que la rotation sont « annulées » sur le rectangle source. Par conséquent, vous n’avez pas besoin de savoir si la vidéo a pivoté ou a été décompressée en 3D. Par exemple, vous pouvez dessiner un rectangle en haut de la balise vidéo, prendre les coordonnées relatives (par rapport à la balise vidéo), les normaliser (plage 0 à 1) et les transmettre en tant que rectangle source et les faire fonctionner comme prévu, même si la vidéo est pivotée.

Le processeur vidéo prend en charge le traitement vidéo accéléré par GPU à l’aide de Microsoft Direct3D 11. Pour plus d’informations, voir [MF \_ sa \_ d3d11 \_ Aware](mf-sa-d3d11-aware.md).

### <a name="stereoscopic-video"></a>Vidéo stéréoscopique

Le processeur vidéo prend en charge l’opération de décompression de vue sur les images vidéo 3D :

Si le frame d’entrée contient deux vues compressées dans le même frame, le processeur vidéo peut fractionner les vues en mémoires tampons distinctes, ou extraire la vue de base et ignorer la deuxième vue. Pour activer la décompression de la vue, définissez l’attribut de [ \_ \_ \_ sortie 3DVIDEO MF Enable](mf-enable-3dvideo-output.md) sur **MF3DVideoOutputType \_ stéréo** ou **MF3DVideoOutputType \_ BaseView**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Camerauicontrol. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Processeurs de signaux numériques](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




