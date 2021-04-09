---
description: Le décodeur vidéo Media Foundation DV est une Media Foundation transformation qui décode la vidéo DV.
ms.assetid: 97e5ba52-92fc-49e4-9c22-6f61bfda2003
title: Décodeur vidéo DV
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed277c3e4dd1aaa031d4dcf4694c7c3051fe37ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749260"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                |
| DLL<br/>                      | <dl> <dt>Mfdvdec.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets codec](codecobjects.md)
</dt> <dt>

[Formats multimédias pris en charge dans Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[Types de média vidéo](video-media-types.md)
</dt> </dl>

 

 




