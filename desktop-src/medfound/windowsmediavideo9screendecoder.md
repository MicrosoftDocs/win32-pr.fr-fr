---
description: Le décodeur d’écran Windows Media Video 9 décode les flux qui ont été encodés par l’encodeur d’écran Windows Media Video 9.
ms.assetid: 6688a830-7a54-4f58-947e-26013e191b5f
title: Décodeur d’écran Windows Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9dcdce920fa39437edb769fd575a7d7a0d68fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524008"
---
# <a name="windows-media-video-9-screen-decoder"></a>Décodeur d’écran Windows Media Video 9

Le décodeur d’écran Windows Media Video 9 décode les flux qui ont été encodés par l’encodeur d' [**écran Windows Media Video 9**](windowsmediavideo9screenencoder.md).

## <a name="class-identifier"></a>Identificateur de classe

L’identificateur de classe (CLSID) du décodeur d’écran Windows Media Video 9 est représenté par la constante **CLSID \_ CMSSCDecMediaObject**. Vous pouvez créer une instance du décodeur en appelant **CoCreateInstance**.

## <a name="input-types"></a>Types d’entrée

Le code à quatre caractères (FOURCC) pour Windows Media Video contenu encodé à l’écran version 9 est « MSS2 ».

Les types d’entrée suivants sont pris en charge par le décodeur d’écran version 9.

-   MEDIASUBTYPE \_ MSS2

## <a name="output-types"></a>Types de sortie

Les types de sortie suivants sont pris en charge par le décodeur d’écran version 9 lorsqu’il est utilisé en tant qu’objet de média DirectX (DMO).

-   MEDIASUBTYPE \_ Rgb24
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ ARGB32
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8

Les types de sortie suivants sont pris en charge par le décodeur d’écran version 9 lorsqu’il est utilisé en tant que transformation de Media Foundation (MFT).

-   MFVideoFormat \_ Rgb24
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ ARGB32
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ RGB8

## <a name="remarks"></a>Notes

Un objet décodeur d’écran expose l’interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) afin que l’objet puisse être utilisé en tant qu’objet de média DirectX (DMO) et expose l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) afin que l’objet puisse être utilisé en tant que transformation de Media Foundation (MFT).

Un décodeur d’écran se comporte comme un DMO ou une table MFT selon les interfaces que vous obtenez et la version de Windows en cours d’exécution. Le tableau suivant indique les conditions sous lesquelles un décodeur d’écran se comporte comme un DMO ou une table MFT.



| Système d’exploitation            | Comportement du décodeur                                                                                                                                                        |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Un décodeur d’écran Windows Media se comporte toujours comme un DMO.                                                                                                                 |
| Windows Vista et Windows 7 | Par défaut, un décodeur d’écran Windows Media se comporte comme un DMO. Si vous obtenez une interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) sur un décodeur d’écran, celui-ci se comporte comme une table MFT. |



 

Vous pouvez utiliser le même CLSID (CLSID \_ CMSSCDecMediaObject) pour créer le décodeur d’écran de la version 7 et le décodeur d’écran de la version 9. Le contenu encodé FOURCC pour Windows Media Video écran version 7 est « MSS1 ». Le décodeur d’écran de la version 7 prend en charge le \_ type d’entrée MEDIASUBTYPE MSS1.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista ou Windows 7<br/>                                       |
| En-tête<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvsdecd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets codec](codecobjects.md)
</dt> <dt>

[Implémentation du codec](codecimplementation.md)
</dt> <dt>

[Utilisation du codec d’écran Windows Media Video 9](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[Encodeur d’écran Windows Media Video 9](windowsmediavideo9screenencoder.md)
</dt> </dl>

 

 
