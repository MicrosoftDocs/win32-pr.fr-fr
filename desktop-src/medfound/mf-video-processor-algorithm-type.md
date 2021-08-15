---
description: Définit des algorithmes pour le processeur vidéo qui est utilisé par \_ l' \_ algorithme de processeur vidéo MF \_ .
ms.assetid: 3BB0836E-39E6-40FA-9BA0-C986EB587CF1
title: Énumération MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
api_type:
- HeaderDef
api_location:
- mfidl.h
ms.openlocfilehash: 885c3e9c34fa787a6877fd37eef81f470be395225594b90b2f5516a8e773eb88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244137"
---
# <a name="mf_video_processor_algorithm_type-enumeration"></a>\_ \_ \_ Énumération des types d’algorithmes de processeur vidéo MF \_

Définit des algorithmes pour le processeur vidéo qui est utilisé par l' [ \_ \_ \_ algorithme de processeur vidéo MF](mf-video-processor-algorithm.md).

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _MF_VIDEO_PROCESSOR_ALGORITHM_TYPE { 
  MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT      = 0,
  MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444  = 1
} MF_VIDEO_PROCESSOR_ALGORITHM_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT"></span><span id="mf_video_processor_algorithm_default"></span>**\_ \_ algorithme de processeur vidéo MF \_ \_ par défaut**
</dt> <dd>

le mode par défaut favorise un équilibre entre qualité et vitesse

</dd> <dt>

<span id="MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444"></span><span id="mf_video_processor_algorithm_mrf_crf_444"></span>**\_ \_ Algorithme de processeur vidéo MF \_ \_ MRF \_ CRF \_ 444**
</dt> <dd>

Le processeur vidéo est toujours traité en interne dans AYUV et utilise des filtres de haute qualité.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                              |
| MIDL<br/>                      | <dl> <dt>Mfidl. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations de Media Foundation](media-foundation-enumerations.md)
</dt> </dl>

 

 




