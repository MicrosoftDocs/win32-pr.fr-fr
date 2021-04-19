---
description: La table MFT de stabilisation vidéo est une Microsoft Media Foundation transformation (MFT) qui effectue une stabilisation d’image sur un flux vidéo.
ms.assetid: BBC42190-08E4-4C3B-972A-FD30621A6CC1
title: Stabilisation vidéo MFT (Camerauicontrol. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65eb64b05e41842b1f7b3ad2e49a6c064be08f0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523449"
---
# <a name="video-stabilization-mft"></a>Stabilisation vidéo MFT

La table MFT de stabilisation vidéo est une Microsoft Media Foundation transformation (MFT) qui effectue une stabilisation d’image sur un flux vidéo.

## <a name="clsid"></a>CLSID

CLSID \_ CMSVideoDSPMFT

## <a name="interfaces"></a>Interfaces

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMediaExtension**](/uwp/api/Windows.Media.IMediaExtension?view=winrt-19041)

## <a name="input-formats"></a>Formats d’entrée

Les combinaisons type de média et sous-type d’entrée acceptées par la MFT de stabilisation vidéo pour la vidéo non compressée sont :

-   **vidéo de MEDIATYPE \_**
-   **MEDIASUBTYPE \_ NV12**
-   **MEDIASUBTYPE \_ YUY2**

## <a name="output-formats"></a>Formats de sortie

Les combinaisons type de média de sortie et sous-type acceptées par la MFT de stabilisation vidéo sont les suivantes :

-   **vidéo de MEDIATYPE \_**
-   **MEDIASUBTYPE \_ NV12**

Le type de média d’entrée doit être défini avant le type de média de sortie. Dans la plupart des cas, la prise en charge du format limité n’est pas un problème, car le pipeline insère automatiquement les conversions de couleur nécessaires.

Le composant MFT de stabilisation vidéo est en capacité de modifier le format dynamique en cas de modification de l’entrée. Lorsque la taille de l’image d’entrée change ou que le sous-type change, une modification de format dynamique est déclenchée sur le flux de sortie.

La table MFT de stabilisation vidéo effectue une conversion des couleurs dans les cas suivants :

-   Lorsque le format d’entrée est **MEDIASUBTYPE \_ YUY2**.
-   Lorsque le mode de compatibilité de Microsoft DirectX 9,0 est utilisé.

### <a name="attributes"></a>Attributs

Les attributs suivants sont pris en charge par la table MFT de stabilisation vidéo par le biais de l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

-   L’attribut [ \_ \_ mode MF VIDEODSP](mf-videodsp-mode.md) place la table MFT de stabilisation vidéo en mode de stabilisation ou en mode pass-through. L’application doit appeler [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) sur le **\_ \_ type GUID MF VIDEODSP** avec un entier correspondant à l’une des valeurs valides suivantes : **MFVideoDSPMode \_ stabilisation** = 4, **MFVideoDSPMode \_ passthrough** = 1. Le \_ mode VIDEODSP MF \_ peut être modifié à tout moment pendant la lecture. Cela provoque une modification du mode dynamique. La sortie passera à la valeur stabilised ou passera après les 16 ou 2 images (selon le mode de latence) après la modification de l’attribut.
-   La [ \_ faible \_ latence MF](mf-low-latency.md) de l’attribut place la MFT de stabilisation vidéo en mode de latence faible ou en mode haute qualité. L’application doit appeler [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) sur la **\_ \_ latence faible** de GUID MF avec un entier correspondant à l’une des valeurs valides suivantes : faible latence = 1 haute qualité = 0
-   L’attribut [MF \_ sa \_ d3d11 \_ BINDFLAGS](mf-sa-d3d11-bindflags.md) est utilisé par le pipeline pour spécifier les indicateurs de liaison d3d11 à partir desquels créer les exemples de sortie. Toute combinaison de valeurs provenant de l’énumération de l' [**\_ \_ indicateur de liaison d3d11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) est valide.
-   Le nombre minimal d’échantillons de sortie de l’attribut **MF \_ sa \_ \_ \_ \_** est utilisé par le pipeline pour spécifier le nombre minimal d’exemples que ce composant doit prendre en charge lors de la sortie.
-   L’attribut [MFSampleExtension \_ VideoDSPMode](mfsampleextension-videodspmode.md) est défini sur chaque échantillon produit par la stabilisation pour indiquer que [le \_ \_ mode MF VIDEODSP](mf-videodsp-mode.md) effectif est appliqué à cet exemple (que l’exemple ait été stabilisé ou non). Dans certaines conditions, les échantillons peuvent ne pas être stabilisés (en raison d’une charge élevée du système, ou des demandes de l’utilisateur). Cet attribut a les mêmes valeurs que l' \_ attribut de \_ mode VIDEODSP MF **( \_ stabilisation MFVideoDSPMode** et **MFVideoDSPMode \_ passthrough**). Pour récupérer la valeur de cet attribut, les applications doivent appeler [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) sur le GUID **MFSampleExtension \_ VideoDSPMode**.

## <a name="remarks"></a>Notes

Une instance du DSP de stabilisation vidéo peut être créée de l’une des manières suivantes :

-   En appelant [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex). Le DSP de stabilisation vidéo est enregistré sous la catégorie d' **\_ \_ \_ effet vidéo de la catégorie MFT** .
-   En appelant la fonction COM **CoCreateInstance** en lui transmettant le CLSID CLSID **\_ CMSVideoDSPMFT**. Pour utiliser cette méthode, vous devez inclure wmcodecdsp. h et établir une liaison avec wmcodecdspuuid. lib.

En outre, le DSP de stabilisation vidéo prend en charge l’instanciation à l’aide de Windows Runtime en tant qu’extension Windows Media. Il est défini sur [**Windows. Media. VideoEffects**](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041)et son nom complet est « Windows. Media. VideoEffects. VideoStabilization ».

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Camerauicontrol. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Processeurs de signaux numériques](windowsmediadigitalsignalprocessors.md)
</dt> <dt>

[**Windows.Media.VideoEffects**](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041)
</dt> </dl>

 

 
