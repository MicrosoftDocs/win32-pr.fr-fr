---
description: Le décodeur Windows Media MPEG-4 v3 décode les flux vidéo MPEG-4 v3.
ms.assetid: 5143b0cc-c171-46af-8d7f-4d029af71fb4
title: Décodeur Windows Media MPEG-4 v3 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ee98a0a3c4b221da6f2000e32d4c75bc3e3a93b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106539790"
---
# <a name="windows-media-mpeg-4-v3-decoder"></a>Décodeur Windows Media MPEG-4 v3

Le décodeur Windows Media MPEG-4 v3 décode les flux vidéo MPEG-4 v3.

## <a name="class-identifier"></a>Identificateur de classe

L’identificateur de classe (CLSID) du décodeur Windows MPEG-4 v3 est représenté par la constante **CLSID \_ CMpeg43DecMediaObject**. Vous pouvez créer une instance du décodeur MPEG-4 v3 en appelant **CoCreateInstance**.

## <a name="formats"></a>Formats

Le décodeur Windows Media MPEG-4 v3 prend en charge les types de média d’entrée suivants.

-   MEDIASUBTYPE \_ mp43
-   MEDIASUBTYPE \_ mp43

Le décodeur Windows Media MPEG-4 v3 prend en charge les sous-types de médias de sortie suivants lorsqu’il agit comme un objet de média DirectX (DMO).

-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ Rgb24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB8
-   MEDIASUBTYPE \_ RGB555

Le décodeur Windows Media MPEG-4 v3 prend en charge les sous-types de médias de sortie suivants lorsqu’il agit comme une Media Foundation transformation (MFT).

-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ Rgb24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB8
-   MFVideoFormat \_ RGB555

## <a name="remarks"></a>Notes

L’objet décodeur Windows Media MPEG-4 v3 expose l’interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) de sorte que l’objet puisse être utilisé en tant qu’objet de média DirectX (DMO) et expose l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) afin que l’objet puisse être utilisé en tant que transformation de Media Foundation (MFT). L’objet a le même identificateur de classe (CLSID), qu’il agisse comme DMO ou MFT.

Le décodeur MPEG-4 v3 se comporte comme un DMO ou une table MFT en fonction des interfaces que vous obtenez et de la version de Windows en cours d’exécution. Le tableau suivant répertorie les conditions dans lesquelles un décodeur MPEG-4 v3 se comporte comme une table DMO ou une table MFT.



| Système d’exploitation            | Comportement du décodeur                                                                                                                                                    |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Le décodeur MPEG-4 v3 se comporte toujours comme un DMO.                                                                                                                      |
| Windows Vista et Windows 7 | Par défaut, le décodeur MPEG-4 v3 se comporte comme un DMO. Si vous obtenez une interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) sur le décodeur MPEG-4 v3, elle se comporte comme une table MFT. |



 

Les identificateurs globaux uniques (GUID) pour les sous-types de média RVB diffèrent selon qu’un décodeur agit comme DMO ou MFT. Les GUID pour les sous-types de média non RVB sont les mêmes, qu’un décodeur agisse comme DMO ou MFT. Pour plus d’informations sur les GUID qui représentent des sous-types de médias, consultez [GUID de sous-type de vidéo](video-subtype-guids.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MP43DECD.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets codec](codecobjects.md)
</dt> </dl>

 

 
