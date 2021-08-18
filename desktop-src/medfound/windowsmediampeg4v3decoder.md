---
description: le décodeur mpeg-4 v3 Windows Media décode les flux vidéo mpeg-4 v3.
ms.assetid: 5143b0cc-c171-46af-8d7f-4d029af71fb4
title: Windows Décodeur Media MPEG-4 v3 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 975351d04b0876b5f1793d442e41d54a585062bd1fed778902fee5c4c83dcd6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100914"
---
# <a name="windows-media-mpeg-4-v3-decoder"></a>Windows Décodeur Media MPEG-4 v3

le décodeur mpeg-4 v3 Windows Media décode les flux vidéo mpeg-4 v3.

## <a name="class-identifier"></a>Identificateur de classe

l’identificateur de classe (CLSID) du décodeur Windows MPEG-4 V3 est représenté par la constante **CLSID \_ CMpeg43DecMediaObject**. Vous pouvez créer une instance du décodeur MPEG-4 v3 en appelant **CoCreateInstance**.

## <a name="formats"></a>Formats

le décodeur MPEG-4 V3 Windows media prend en charge les types de média d’entrée suivants.

-   MEDIASUBTYPE \_ mp43
-   MEDIASUBTYPE \_ mp43

le décodeur MPEG-4 V3 Windows media prend en charge les sous-types de médias de sortie suivants lorsqu’il agit comme un objet de média DirectX (DMO).

-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ Rgb24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB8
-   MEDIASUBTYPE \_ RGB555

le décodeur MPEG-4 V3 Windows media prend en charge les sous-types de médias de sortie suivants lorsqu’il agit comme une transformation de Media Foundation (MFT).

-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ Rgb24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB8
-   MFVideoFormat \_ RGB555

## <a name="remarks"></a>Remarques

l’objet décodeur Windows Media MPEG-4 V3 expose l’interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) de sorte que l’objet puisse être utilisé comme objet de média DirectX (DMO) et expose l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) afin que l’objet puisse être utilisé comme une transformation de Media Foundation (MFT). l’objet a le même identificateur de classe (CLSID), qu’il agisse comme un DMO ou une table MFT.

le décodeur MPEG-4 V3 se comporte comme un DMO ou une table MFT selon les interfaces que vous obtenez et la version de Windows en cours d’exécution. le tableau suivant indique les conditions dans lesquelles un décodeur MPEG-4 V3 se comporte comme un DMO ou une table MFT.



| Système d’exploitation            | Comportement du décodeur                                                                                                                                                    |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Le décodeur MPEG-4 v3 se comporte toujours comme un DMO.                                                                                                                      |
| Windows Vista et Windows 7 | Par défaut, le décodeur MPEG-4 v3 se comporte comme un DMO. Si vous obtenez une interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) sur le décodeur MPEG-4 v3, elle se comporte comme une table MFT. |



 

les identificateurs globaux uniques (guid) pour les sous-types de média rvb diffèrent selon qu’un décodeur joue le rôle d’un DMO ou d’une table MFT. les guid pour les sous-types de média non rvb sont les mêmes, qu’un décodeur agisse en tant que DMO ou MFT. Pour plus d’informations sur les GUID qui représentent des sous-types de médias, consultez [GUID de sous-type de vidéo](video-subtype-guids.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MP43DECD.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets codec](codecobjects.md)
</dt> </dl>

 

 
