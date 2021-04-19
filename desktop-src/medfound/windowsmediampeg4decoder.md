---
description: Le décodeur MPEG4 v1/v2 Windows Media décode les flux vidéo MPEG4 v1/v2.
ms.assetid: 63b32972-1003-4291-bfdd-cc0cb8d65430
title: Décodeur Windows Media MPEG4 v1/v2 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b14cf22e29c1266ac9bb3593375ee4485d79df2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106537163"
---
# <a name="windows-media-mpeg4-v1v2-decoder"></a>Décodeur Windows Media MPEG4 v1/v2

Le décodeur MPEG4 v1/v2 Windows Media décode les flux vidéo MPEG4 v1/v2.

## <a name="class-identifier"></a>Identificateur de classe

L’identificateur de classe (CLSID) du décodeur MPEG4 v1/v2 Windows Media est représenté par la constante **CLSID \_ CMpeg4DecMediaObject**. Vous pouvez créer une instance du décodeur MPEG4 v1/v2 en appelant **CoCreateInstance**.

## <a name="formats"></a>Formats

Le décodeur MPEG4 v1/v2 Windows Media prend en charge les types de média d’entrée suivants.

-   MEDIASUBTYPE \_ MPG4
-   MEDIASUBTYPE \_ MPG4
-   MEDIASUBTYPE \_ MP42
-   MEDIASUBTYPE \_ MP42

Le décodeur MPEG4 Windows Media MPEG4/v2 prend en charge les sous-types de médias de sortie suivants lorsqu’il agit comme un objet de média DirectX (DMO).

-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ Rgb24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB8
-   MEDIASUBTYPE \_ RGB555

Le décodeur MPEG4 Windows Media MPEG4/v2 prend en charge les sous-types de médias de sortie suivants lorsqu’il agit comme une Media Foundation transformation (MFT).

-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ Rgb24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB8
-   MFVideoFormat \_ RGB555

## <a name="remarks"></a>Notes

L’objet décodeur Windows Media MPEG4 v1/v2 expose l’interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) afin que l’objet puisse être utilisé en tant qu’objet de média DirectX (DMO) et expose l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) afin que l’objet puisse être utilisé en tant que transformation de Media Foundation (MFT). L’objet a le même identificateur de classe (CLSID), qu’il agisse comme DMO ou MFT.

Un décodeur MPEG4 v1/v2 se comporte comme un DMO ou une table MFT en fonction des interfaces que vous obtenez et de la version de Windows en cours d’exécution. Le tableau suivant indique les conditions dans lesquelles un décodeur MPEG4 v1/v2 se comporte comme une version DMO ou une table MFT.



| Système d’exploitation            | Comportement du décodeur                                                                                                                                                                |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Un décodeur MPEG4 v1/v2 se comporte toujours comme un DMO.                                                                                                                                 |
| Windows Vista et Windows 7 | Par défaut, un décodeur MPEG4 v1/v2 se comporte comme un DMO. Si vous obtenez une interface de GUID de sous- [type de vidéo](video-subtype-guids.md) sur un décodeur MPEG4 v1/v2, elle se comporte comme une table MFT. |



 

Les identificateurs globaux uniques (GUID) pour les sous-types de média RVB diffèrent selon qu’un décodeur agit comme DMO ou MFT. Les GUID pour les sous-types de média non RVB sont les mêmes, qu’un décodeur agisse comme DMO ou MFT. Pour plus d’informations sur les GUID qui représentent des sous-types de vidéos, consultez [GUID de sous-type de vidéo](video-subtype-guids.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MPG4DECD.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets codec](codecobjects.md)
</dt> </dl>

 

 
