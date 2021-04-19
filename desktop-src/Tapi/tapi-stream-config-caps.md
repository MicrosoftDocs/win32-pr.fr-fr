---
description: La structure d’embouts de la configuration de \_ flux TAPI contient des \_ \_ informations de configuration de flux vidéo ou audio.
ms.assetid: 83b39751-b00f-4762-830b-13cafbcb1cfd
title: Structure TAPI_STREAM_CONFIG_CAPS (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379ca481d3bebaf8ceb11bfc2dbdab6642ca20b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530970"
---
# <a name="tapi_stream_config_caps-structure"></a>\_Structure d' \_ \_ embouts de la configuration de flux TAPI

\[ Cette structure n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La structure d' **\_ \_ \_ embouts** de la configuration de flux TAPI contient des informations de configuration de flux vidéo ou audio.

## <a name="syntax"></a>Syntaxe


```C++
} TAPI_STREAM_CONFIG_CAPS, *PTAPI_STREAM_CONFIG_CAPS;
```



## <a name="members"></a>Membres

<dl> <dt>

**CapsType**
</dt> <dd>

Définit si le membre d’Union contient des informations vidéo ou audio.

</dd> <dt>

**VideoCap**
</dt> <dd>

Structure de la [**\_ \_ \_ configuration \_ de flux vidéo TAPI**](tapi-video-stream-config-caps.md) contenant les fonctionnalités du flux vidéo.

</dd> <dt>

**AudioCap**
</dt> <dd>

Structure [**d' \_ \_ \_ \_ embouts de configuration de flux audio TAPI**](tapi-audio-stream-config-caps.md) contenant les fonctionnalités de flux audio.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,1<br/>                                                       |
| En-tête<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITFormatControl::GetStreamCaps**](itformatcontrol-getstreamcaps.md)
</dt> <dt>

[**StreamConfigCapsType**](streamconfigcapstype.md)
</dt> <dt>

[**extrémités de la \_ \_ configuration du flux vidéo \_ TAPI \_**](tapi-video-stream-config-caps.md)
</dt> <dt>

[**extrémités de la \_ \_ configuration du flux audio \_ TAPI \_**](tapi-audio-stream-config-caps.md)
</dt> </dl>

 

 




