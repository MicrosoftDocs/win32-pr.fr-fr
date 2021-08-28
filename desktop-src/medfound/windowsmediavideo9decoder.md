---
description: le décodeur Windows Media Video 9 décode les flux vidéo qui ont été encodés par l’encodeur Windows Media Video.
ms.assetid: 08f68d1c-c226-4bf6-abd0-fce0f9ddbc05
title: Windows Décodeur Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df973e78f69e1f1ff0e649b2c4f5637380be9f27
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474305"
---
# <a name="windows-media-video-9-decoder"></a>Windows Décodeur Media Video 9

le décodeur Windows Media Video 9 décode les flux vidéo qui ont été encodés par l’encodeur [**Windows Media Video**](windowsmediavideo9encoder.md). L’encodeur et le décodeur prennent en charge les quatre catégories de vidéo encodées suivantes.

-   Windows Profil simple Media Video 9
-   Windows Profil principal Media Video 9
-   Windows Profil Media Video 9 Advanced
-   Windows Image Media Video 9,1

## <a name="class-identifier"></a>Identificateur de classe

l’identificateur de classe (CLSID) du décodeur de Windows Media Video est représenté par la constante **clsid \_ CWMVDecMediaObject**. Vous pouvez créer une instance du décodeur vidéo en appelant **CoCreateInstance**.

## <a name="interfaces"></a>Interfaces

un objet décodeur vidéo expose l’interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) afin que l’objet puisse être utilisé en tant qu’objet DirectX Media (DMO) et expose l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) afin que l’objet puisse être utilisé en tant que transformation de Media Foundation (MFT).

un décodeur vidéo se comporte comme un DMO ou une table MFT selon les interfaces que vous obtenez et la version de Windows en cours d’exécution. le tableau suivant indique les conditions sous lesquelles un décodeur vidéo se comporte comme un DMO ou une table MFT.



| Système d’exploitation            | Comportement du décodeur                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | un décodeur vidéo de média Windows se comporte toujours comme une DMO.                                                                                                                |
| Windows Vista et Windows 7 | par défaut, un décodeur vidéo de média Windows se comporte comme un DMO. Si vous obtenez une interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) sur un décodeur vidéo, il se comporte comme une table MFT. |



 

à partir de Windows 7, le décodeur Windows Media Video implémente l’interface [**IDMOQualityControl**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol) .

## <a name="input-formats"></a>Formats d’entrée

le tableau suivant présente les codes à quatre caractères (FOURCCs) qui correspondent aux catégories d’entrées encodées prises en charge par le décodeur Windows Media Video.



| Category                               | FOURCC                                   |
|----------------------------------------|------------------------------------------|
| Windows Profil simple Media Video 9   | "WMV3"                                   |
| Windows Profil principal Media Video 9     | "WMV3"                                   |
| Windows Profil Media Video 9 Advanced | "WVC1"                                   |
| Windows Image Media Video 9,1          | « WMVP » pour 9,1, « WVP2 » pour 9,1 version 2 |



 

## <a name="output-formats"></a>Formats de sortie

le décodeur Windows Media Video prend en charge les sous-types de médias de sortie suivants lorsqu’il agit en tant que DMO.

-   MEDIASUBTYPE \_ NV12
-   MEDIASUBTYPE \_ YV12
-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ YVYU
-   MEDIASUBTYPE \_ NV11
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ Rgb24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8

le décodeur Windows Media Video prend en charge les sous-types de médias de sortie suivants lorsqu’il joue le rôle de MFT.

-   MFVideoFormat \_ NV12
-   MFVideoFormat \_ YV12
-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ YVYU
-   MFVideoFormat \_ NV11
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ Rgb24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ RGB8

## <a name="properties"></a>Propriétés

le décodeur Windows Media Video prend en charge les propriétés suivantes.




| Propriété | Description | 
|----------|-------------|
| <a href="mfpkey-decoder-deinterlacingproperty.md">MFPKEY_DECODER_DEINTERLACING</a> | Spécifie si le codec décode les images vidéo entrelacées du flux compressé en tant que trames progressives.<br /><dl> Windows XP et versions ultérieures.<br />Profil simple, profil principal, profil avancé.<br />En lecture/écriture.<br /></dl> | 
| <a href="mfpkey-dxva-enabledproperty.md">MFPKEY_DXVA_ENABLED</a> | Spécifie si le décodeur utilise le matériel d’accélération vidéo DirectX, s’il est disponible.<br /><dl> Windows XP et versions ultérieures.<br />Profil simple, profil principal, profil avancé.<br />En écriture seule.<br /></dl> | 
| <a href="mfpkey-avdecvideoswpowerlevelproperty.md">MFPKEY_AVDecVideoSWPowerLevel</a> | Spécifie le niveau de puissance pour le décodeur.<br /><dl> Windows 7<br />Profil simple, profil principal, profil avancé, image.<br />En lecture/écriture.<br /></dl> | 
| <a href="mfpkey-fi-enabledproperty.md">MFPKEY_FI_ENABLED</a> | Spécifie si le décodeur doit utiliser l’interpolation de frame.<br /><dl> Windows XP et versions ultérieures.<br />Profil simple, profil principal, profil avancé, image.<br />En écriture seule.<br /></dl> | 
| <a href="mfpkey-fi-supportedproperty.md">MFPKEY_FI_SUPPORTED</a> | Spécifie si le décodeur prend en charge l’interpolation de frame.<br /><dl> Windows XP et versions ultérieures.<br />Profil simple, profil principal, profil avancé, image<br />Lecture seule.<br /></dl> | 
| <a href="mfpkey-numthreadsdecproperty.md">MFPKEY_NUMTHREADSDEC</a> | Spécifie le nombre de threads que le décodeur utilisera.<br /><dl> Windows Vista et versions ultérieures.<br />Profil simple, profil principal, profil avancé, image.<br />En lecture/écriture.<br /></dl> | 
| <a href="mfpkey-postprocessmodeproperty.md">MFPKEY_POSTPROCESSMODE</a> | Spécifie le mode de traitement de la publication pour le décodeur.<br /><dl> Windows Vista et versions ultérieures.<br />Profil simple, profil principal, profil avancé, image.<br />En écriture seule.<br /></dl> | 
| <strong>g_wszWMVCNeedsDrain</strong> | Spécifie si le décodeur doit être vidé.<br /><dl> Windows 8<br />Lecture seule.<br /></dl> cette propriété est utilisée par le runtime de Format multimédia Windows. Le type de propriété est <strong>VARIANT_BOOL</strong>. Si la valeur est <strong>VARIANT_TRUE</strong>, le décodeur doit être vidé après une discontinuation. Pour plus d’informations sur la vidange d’une table MFT, consultez <a href="basic-mft-processing-model.md">modèle de traitement MFT de base</a>.<br /><blockquote>[!Note]<br />Pour interroger cette propriété, utilisez l’interface <a href="/windows/desktop/com/ipropertybag-and-ipersistpropertybag"><strong>IPropertyBag</strong></a> .</blockquote><br /> | 




 

## <a name="remarks"></a>Remarques

la résolution maximale autorisée par le décodeur Windows Media Video 9 est 4096x4096.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista ou Windows 7<br/>                                       |
| En-tête<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvdecod.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets codec](codecobjects.md)
</dt> <dt>

[Implémentation du codec](codecimplementation.md)
</dt> </dl>

 

 
