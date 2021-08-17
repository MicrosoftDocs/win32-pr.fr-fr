---
description: Le décodeur vidéo Media Foundation DV est une Media Foundation transformation qui décode la vidéo DV.
ms.assetid: 97e5ba52-92fc-49e4-9c22-6f61bfda2003
title: Décodeur vidéo DV
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd91cf325d9ba715d75aae884e29665d05d449ca39f01c195f9b13e2e1f8c1fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118064092"
---
# <a name="dv-video-decoder"></a>Décodeur vidéo DV

Le décodeur vidéo Media Foundation DV est une [Media Foundation transformation](media-foundation-transforms.md) qui décode la vidéo DV.

Le décodeur vidéo DV prend en charge les types d’entrée suivants :



| Subtype                 | Description                  |
|-------------------------|------------------------------|
| **\_DVC MFVideoFormat**  | Vidéo DVC/DV                 |
| **MFVideoFormat \_ DVHD** | HD-magnétoscope numérique (1125-60 ou 1250-50) |
| **MFVideoFormat \_ DVSD** | SDL-magnétoscope numérique (525-60 ou 625-50)  |
| **MFVideoFormat \_ DVSL** | SD-magnétoscope numérique (525-60 ou 625-50)   |



 

Il prend en charge un seul type de sortie :



| Subtype             | Description |
|---------------------|-------------|
| MFVideoFormat \_ YUY2 | Vidéo YUY2  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                |
| DLL<br/>                      | <dl> <dt>Mfdvdec.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets codec](codecobjects.md)
</dt> <dt>

[Formats multimédias pris en charge dans Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[Types de média vidéo](video-media-types.md)
</dt> </dl>

 

 




