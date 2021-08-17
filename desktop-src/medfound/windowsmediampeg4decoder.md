---
description: le décodeur mpeg4 v1/v2 Windows Media décode les flux vidéo mpeg4 v1/v2.
ms.assetid: 63b32972-1003-4291-bfdd-cc0cb8d65430
title: Windows Décodeur de média MPEG4 v1/v2 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c55d5c64cec2a0ad08978064d40c26267d7729adeee9a9f148c8e682ba168509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100931"
---
# <a name="windows-media-mpeg4-v1v2-decoder"></a>Windows Décodeur de média MPEG4 v1/v2

le décodeur mpeg4 v1/v2 Windows Media décode les flux vidéo mpeg4 v1/v2.

## <a name="class-identifier"></a>Identificateur de classe

l’identificateur de classe (CLSID) du décodeur MPEG4 V1/V2 Windows Media est représenté par la constante **CLSID \_ CMpeg4DecMediaObject**. Vous pouvez créer une instance du décodeur MPEG4 v1/v2 en appelant **CoCreateInstance**.

## <a name="formats"></a>Formats

le décodeur MPEG4 V1/V2 du média Windows prend en charge les types de média d’entrée suivants.

-   MEDIASUBTYPE \_ MPG4
-   MEDIASUBTYPE \_ MPG4
-   MEDIASUBTYPE \_ MP42
-   MEDIASUBTYPE \_ MP42

le décodeur MPEG4 V1/V2 du média Windows prend en charge les sous-types de médias de sortie suivants lorsqu’il agit comme un objet de média DirectX (DMO).

-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ Rgb24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB8
-   MEDIASUBTYPE \_ RGB555

le décodeur MPEG4 V1/V2 du média Windows prend en charge les sous-types de médias de sortie suivants lorsqu’il agit en tant que Media Foundation de transformation (MFT).

-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ Rgb24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB8
-   MFVideoFormat \_ RGB555

## <a name="remarks"></a>Remarques

l’objet décodeur MPEG4 V1/V2 Windows Media expose l’interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) afin que l’objet puisse être utilisé en tant qu’objet de média DirectX (DMO) et expose l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) afin que l’objet puisse être utilisé en tant que transformation de Media Foundation (MFT). l’objet a le même identificateur de classe (CLSID), qu’il agisse comme un DMO ou une table MFT.

un décodeur MPEG4 V1/V2 se comporte comme un DMO ou une table MFT selon les interfaces que vous obtenez et la version de Windows en cours d’exécution. le tableau suivant indique les conditions dans lesquelles un décodeur MPEG4 V1/V2 se comporte comme un DMO ou une table MFT.



| Système d’exploitation            | Comportement du décodeur                                                                                                                                                                |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Un décodeur MPEG4 v1/v2 se comporte toujours comme un DMO.                                                                                                                                 |
| Windows Vista et Windows 7 | Par défaut, un décodeur MPEG4 v1/v2 se comporte comme un DMO. Si vous obtenez une interface de GUID de sous- [type de vidéo](video-subtype-guids.md) sur un décodeur MPEG4 v1/v2, elle se comporte comme une table MFT. |



 

les identificateurs globaux uniques (guid) pour les sous-types de média rvb diffèrent selon qu’un décodeur joue le rôle d’un DMO ou d’une table MFT. les guid pour les sous-types de média non rvb sont les mêmes, qu’un décodeur agisse en tant que DMO ou MFT. Pour plus d’informations sur les GUID qui représentent des sous-types de vidéos, consultez [GUID de sous-type de vidéo](video-subtype-guids.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MPG4DECD.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets codec](codecobjects.md)
</dt> </dl>

 

 
