---
description: Le décodeur Windows Media Video 9 décode les flux vidéo qui ont été encodés par l’encodeur Windows Media Video.
ms.assetid: 08f68d1c-c226-4bf6-abd0-fce0f9ddbc05
title: Décodeur Windows Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96d89e05f82ce503016a10d5591a23bc673d0db5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539949"
---
# <a name="windows-media-video-9-decoder"></a>Décodeur Windows Media Video 9

Le décodeur Windows Media Video 9 décode les flux vidéo qui ont été encodés par l’encodeur [**Windows Media Video**](windowsmediavideo9encoder.md). L’encodeur et le décodeur prennent en charge les quatre catégories de vidéo encodées suivantes.

-   Profil simple Windows Media Video 9
-   Profil principal du Windows Media Video 9
-   Profil avancé Windows Media Video 9
-   Image Windows Media Video 9,1

## <a name="class-identifier"></a>Identificateur de classe

L’identificateur de classe (CLSID) du décodeur de Windows Media Video est représenté par la constante **CLSID \_ CWMVDecMediaObject**. Vous pouvez créer une instance du décodeur vidéo en appelant **CoCreateInstance**.

## <a name="interfaces"></a>Interfaces

Un objet décodeur vidéo expose l’interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) afin que l’objet puisse être utilisé en tant qu’objet de média DirectX (DMO) et expose l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) afin que l’objet puisse être utilisé en tant que transformation de Media Foundation (MFT).

Un décodeur vidéo se comporte comme un DMO ou une table MFT en fonction des interfaces que vous obtenez et de la version de Windows en cours d’exécution. Le tableau suivant indique les conditions sous lesquelles un décodeur vidéo se comporte comme un DMO ou une table MFT.



| Système d’exploitation            | Comportement du décodeur                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Un décodeur vidéo Windows Media se comporte toujours comme un DMO.                                                                                                                |
| Windows Vista et Windows 7 | Par défaut, un décodeur vidéo Windows Media se comporte comme un DMO. Si vous obtenez une interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) sur un décodeur vidéo, il se comporte comme une table MFT. |



 

À partir de Windows 7, le décodeur Windows Media Video implémente l’interface [**IDMOQualityControl**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol) .

## <a name="input-formats"></a>Formats d’entrée

Le tableau suivant présente les codes à quatre caractères (FOURCCs) qui correspondent aux catégories d’entrées encodées prises en charge par le décodeur Windows Media Video.



| Category                               | FOURCC                                   |
|----------------------------------------|------------------------------------------|
| Profil simple Windows Media Video 9   | "WMV3"                                   |
| Profil principal du Windows Media Video 9     | "WMV3"                                   |
| Profil avancé Windows Media Video 9 | "WVC1"                                   |
| Image Windows Media Video 9,1          | « WMVP » pour 9,1, « WVP2 » pour 9,1 version 2 |



 

## <a name="output-formats"></a>Formats de sortie

Le décodeur Windows Media Video prend en charge les sous-types de médias de sortie suivants lorsqu’il agit en tant que DMO.

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

Le décodeur Windows Media Video prend en charge les sous-types de médias de sortie suivants lorsqu’il joue le rôle de MFT.

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

Le décodeur Windows Media Video prend en charge les propriétés suivantes.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Propriété</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-decoder-deinterlacingproperty.md">MFPKEY_DECODER_DEINTERLACING</a></td>
<td>Spécifie si le codec décode les images vidéo entrelacées du flux compressé en tant que trames progressives.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dxva-enabledproperty.md">MFPKEY_DXVA_ENABLED</a></td>
<td>Spécifie si le décodeur utilise le matériel d’accélération vidéo DirectX, s’il est disponible.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-avdecvideoswpowerlevelproperty.md">MFPKEY_AVDecVideoSWPowerLevel</a></td>
<td>Spécifie le niveau de puissance pour le décodeur.<br/> <dl> Windows 7<br />
Profil simple, profil principal, profil avancé, image.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-fi-enabledproperty.md">MFPKEY_FI_ENABLED</a></td>
<td>Spécifie si le décodeur doit utiliser l’interpolation de frame.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé, image.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fi-supportedproperty.md">MFPKEY_FI_SUPPORTED</a></td>
<td>Spécifie si le décodeur prend en charge l’interpolation de frame.<br/> <dl> Windows XP et versions ultérieures.<br />
Profil simple, profil principal, profil avancé, image<br />
Lecture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-numthreadsdecproperty.md">MFPKEY_NUMTHREADSDEC</a></td>
<td>Spécifie le nombre de threads que le décodeur utilisera.<br/> <dl> Windows Vista et versions ultérieures.<br />
Profil simple, profil principal, profil avancé, image.<br />
En lecture/écriture.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-postprocessmodeproperty.md">MFPKEY_POSTPROCESSMODE</a></td>
<td>Spécifie le mode de traitement de la publication pour le décodeur.<br/> <dl> Windows Vista et versions ultérieures.<br />
Profil simple, profil principal, profil avancé, image.<br />
En écriture seule.<br />
</dl></td>
</tr>
<tr class="even">
<td><strong>g_wszWMVCNeedsDrain</strong></td>
<td>Spécifie si le décodeur doit être vidé.<br/> <dl> Windows 8<br />
Lecture seule.<br />
</dl> Cette propriété est utilisée par l’exécution du format Windows Media. Le type de propriété est <strong>VARIANT_BOOL</strong>. Si la valeur est <strong>VARIANT_TRUE</strong>, le décodeur doit être vidé après une discontinuation. Pour plus d’informations sur la vidange d’une table MFT, consultez <a href="basic-mft-processing-model.md">modèle de traitement MFT de base</a>.<br/>
<blockquote>
[!Note]<br />
Pour interroger cette propriété, utilisez l’interface <a href="/windows/desktop/com/ipropertybag-and-ipersistpropertybag"><strong>IPropertyBag</strong></a> .
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Notes

La résolution maximale autorisée par le décodeur Windows Media Video 9 est 4096x4096.

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

 

 
