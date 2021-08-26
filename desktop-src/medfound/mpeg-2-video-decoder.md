---
description: Le décodeur vidéo MPEG-2 est une transformation de Media Foundation qui décode la vidéo MPEG-1 et MPEG-2.
ms.assetid: 3E7FAE14-932D-44A3-997B-567C0D2EAE7B
title: Décodeur vidéo MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e2b270cadb114875fb63bc6c57ce2ddd63eecb2815b8fe3bcee175710d1771
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012589"
---
# <a name="mpeg-2-video-decoder"></a>Décodeur vidéo MPEG-2

Le décodeur vidéo MPEG-2 est une [transformation de Media Foundation](media-foundation-transforms.md) qui décode la vidéo MPEG-1 et MPEG-2. Le décodeur prend en charge la vidéo de profil simple et MPEG-2 (H. 262, ISO/IEC 13818-2) et MPEG-1 Video (ISO/IEC 11172-2).

## <a name="input-types"></a>Types d’entrée

Le décodeur prend en charge les types de média d’entrée suivants.

| Attribut                                                 | Description                                                             |
|-----------------------------------------------------------|-------------------------------------------------------------------------|
| [**\_type de \_ majeurese MF MT \_**](mf-mt-major-type-attribute.md) | **\_Vidéo MFMediaType**                                                  |
| [**\_sous- \_ type MF MT**](mf-mt-subtype-attribute.md)        | **MFVideoFormat \_ MPEG1**<br/> **MFVideoFormat \_ MPEG2**<br/> |



 

## <a name="output-types"></a>Types de sortie

Le décodeur prend en charge les types de sortie suivants.

| Attribut                                                 | Description                                                                                                                                                                    |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_type de \_ majeurese MF MT \_**](mf-mt-major-type-attribute.md) | **\_Vidéo MFMediaType**                                                                                                                                                         |
| [**\_sous- \_ type MF MT**](mf-mt-subtype-attribute.md)        | **MFVideoFormat \_ I420**<br/> **MFVideoFormat \_ IYUV**<br/> **MFVideoFormat \_ NV12**<br/> **MFVideoFormat \_ YUY2**<br/> **MFVideoFormat \_ YV12**<br/> |



 

## <a name="remarks"></a>Remarques

Le décodeur vidéo MPEG-2 expose les interfaces suivantes :

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

L’entrée du décodeur doit être un flux élémentaire. La résolution maximale prise en charge est de 1920 × 1088 pixels.

Le décodeur prend en charge l’accélération vidéo DirectX (DXVA) à l’aide de Microsoft Direct3D 9 ou Microsoft Direct3D 11.

### <a name="special-decoding-modes"></a>Modes de décodage spéciaux

-   **Mode de latence faible.** Ce mode est approprié pour des scénarios tels que les communications en temps réel. Cela réduit la latence de démarrage, de sorte que le décodeur produit le premier exemple de sortie plus tôt. Toutefois, le décodeur met en mémoire tampon moins d’échantillons dans ce mode, ce qui peut potentiellement entraîner des problèmes, car le décodeur ne décode pas autant de frames à l’avance. Pour activer le mode de faible latence, définissez l’attribut [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md) .
-   **Cherche.** Pour obtenir une recherche précise, appelez la méthode [**IMFTransform :: SetOutputBounds**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds) . Lorsque cette méthode est appelée, le décodeur génère uniquement les trames qui se trouvent dans la plage d’horodatage spécifiée par l’appelant.
-   **Mode de génération de miniatures**. Ce mode est conçu pour la génération rapide d’images miniatures. Dans ce mode, le décodeur décode initialement uniquement les images I. Si aucun frame I n’est trouvé dans un certain nombre de frames, le décodeur commence à décoder les frames P et sort les trames non-I à un intervalle fixe (un par *N* images) jusqu’à ce qu’une image i soit atteinte. Pour activer le mode de génération de miniatures, définissez la propriété [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md) .
-   **Astuce.** Le décodeur peut décoder à des vitesses plus rapides que le temps réel. À des vitesses de lecture plus élevées, le décodeur passe au décodage uniquement des trames. Pour la lecture inversée, seules les trames sont décodées.

### <a name="codec-properties"></a>Propriétés du codec

Le décodeur prend en charge les propriétés suivantes par le biais de la méthode [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .



| Propriété                                                                                                      | Description                                                                                                |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md)               | Active ou désactive le mode de génération de miniatures.                                                             |
| [CODECAPI \_ AVDecVideoAcceleration \_ MPEG2](../directshow/avdecvideoacceleration-mpeg2-property.md)                        | Active ou désactive le décodage à accélération matérielle.                                                         |
| [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)                                                   | Active ou désactive le mode faible latence.                                                                      |
| [le \_ DÉcodeur MFT \_ expose les \_ \_ types \_ de sortie dans l' \_ \_ ordre natif](mft-decoder-expose-output-types-in-native-order.md) | Spécifie si le décodeur expose des types de sortie qui conviennent au transcodage avant d’autres formats. |



 

Parmi ces propriétés, vous pouvez également définir les éléments suivants à l’aide de l’interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) :

-   [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [CODECAPI \_ AVDecVideoAcceleration \_ MPEG2](../directshow/avdecvideoacceleration-mpeg2-property.md)
-   [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)

### <a name="limitations"></a>Limites

-   Le décodeur n’est pas pris en charge sur les plateformes IA-64.
-   Le décodeur ne prend pas en charge le déchiffrement CSS ou la lecture des DVD chiffrés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                       |
| DLL<br/>                      | <dl> <dt>Msmpeg2vdec.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets codec](codecobjects.md)
</dt> </dl>

 

 
