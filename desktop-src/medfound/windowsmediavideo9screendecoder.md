---
description: le décodeur d’écran Windows Media Video 9 décode les flux qui ont été encodés par l’encodeur d’écran Windows Media Video 9.
ms.assetid: 6688a830-7a54-4f58-947e-26013e191b5f
title: Windows Décodeur d’écran Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9dcdce920fa39437edb769fd575a7d7a0d68fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313578"
---
# <a name="windows-media-video-9-screen-decoder"></a>Windows Décodeur d’écran Media Video 9

le décodeur d’écran Windows Media Video 9 décode les flux qui ont été encodés par l’encodeur d' [**écran Windows Media Video 9**](windowsmediavideo9screenencoder.md).

## <a name="class-identifier"></a>Identificateur de classe

l’identificateur de classe (CLSID) du décodeur d’écran Windows Media Video 9 est représenté par la constante **clsid \_ CMSSCDecMediaObject**. Vous pouvez créer une instance du décodeur en appelant **CoCreateInstance**.

## <a name="input-types"></a>Types d’entrée

le code à quatre caractères (FOURCC) pour Windows Media Video contenu encodé à l’écran Version 9 est « MSS2 ».

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

un objet décodeur d’écran expose l’interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) afin que l’objet puisse être utilisé en tant qu’objet DirectX Media (DMO) et expose l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) afin que l’objet puisse être utilisé en tant que Media Foundation Transform (MFT).

un décodeur d’écran se comporte comme un DMO ou une table MFT en fonction des interfaces que vous obtenez et de la version de Windows en cours d’exécution. le tableau suivant indique les conditions sous lesquelles un décodeur d’écran se comporte comme un DMO ou une table MFT.



| Système d'exploitation            | Comportement du décodeur                                                                                                                                                        |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | un décodeur d’écran de média Windows se comporte toujours comme DMO.                                                                                                                 |
| Windows Vista et Windows 7 | par défaut, un décodeur d’écran de média Windows se comporte comme un DMO. Si vous obtenez une interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) sur un décodeur d’écran, celui-ci se comporte comme une table MFT. |



 

Vous pouvez utiliser le même CLSID (CLSID \_ CMSSCDecMediaObject) pour créer le décodeur d’écran de la version 7 et le décodeur d’écran de la version 9. le contenu encodé FOURCC pour Windows Media Video écran Version 7 est « MSS1 ». Le décodeur d’écran de la version 7 prend en charge le \_ type d’entrée MEDIASUBTYPE MSS1.

## <a name="requirements"></a>Spécifications



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

[utilisation du Codec d’écran Windows Media Video 9](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[Windows Encodeur d’écran Media Video 9](windowsmediavideo9screenencoder.md)
</dt> </dl>

 

 
