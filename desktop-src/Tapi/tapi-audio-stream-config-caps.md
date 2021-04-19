---
description: La \_ \_ \_ structure d’embouts de la configuration du flux audio TAPI \_ est contenue dans la structure de la \_ configuration du flux TAPI \_ \_ lorsque le membre CapsType est défini sur le membre AudioCap de l’Union StreamConfigCapsType.
ms.assetid: 61575839-4604-4c8b-ae4d-fe796c3c5314
title: Structure TAPI_AUDIO_STREAM_CONFIG_CAPS (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daec587a8e760bedd3ab9c6b3469ef8f70b72383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541330"
---
# <a name="tapi_audio_stream_config_caps-structure"></a>\_Structure d' \_ \_ \_ embouts de la configuration du flux audio TAPI

\[ Cette structure n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La structure d' **\_ \_ \_ \_ embouts de la configuration du flux audio TAPI** est contenue dans la  structure de la [**\_ \_ configuration \_ du flux TAPI**](tapi-stream-config-caps.md) lorsque le membre CapsType est défini sur le membre **AudioCap** de l’Union [**StreamConfigCapsType**](streamconfigcapstype.md) .

## <a name="syntax"></a>Syntaxe


```C++
} TAPI_AUDIO_STREAM_CONFIG_CAPS;
```



## <a name="members"></a>Membres

<dl> <dt>

**Description**
</dt> <dd>

Description conviviale du type de configuration de flux audio à afficher aux utilisateurs de l’application.

</dd> <dt>

**MinimumChannels**
</dt> <dd>

Nombre minimal de canaux associés au flux.

</dd> <dt>

**MaximumChannels**
</dt> <dd>

Nombre maximal de canaux associés au flux.

</dd> <dt>

**ChannelsGranularity**
</dt> <dd>

Granularité du nombre de canaux.

</dd> <dt>

**MinimumBitsPerSample**
</dt> <dd>

Nombre minimal de bits par échantillon.

</dd> <dt>

**MaximumBitsPerSample**
</dt> <dd>

Nombre maximal de bits par échantillon.

</dd> <dt>

**BitsPerSampleGranularity**
</dt> <dd>

Granularité des bits par valeurs d’échantillon.

</dd> <dt>

**MinimumSampleFrequency**
</dt> <dd>

Fréquence d’échantillonnage minimale.

</dd> <dt>

**MaximumSampleFrequency**
</dt> <dd>

Fréquence d’échantillonnage maximale.

</dd> <dt>

**SampleFrequencyGranularity**
</dt> <dd>

Granularité des valeurs de fréquence d’échantillonnage.

</dd> <dt>

**MinimumAvgBytesPerSec**
</dt> <dd>

Nombre moyen d’octets par seconde.

</dd> <dt>

**MaximumAvgBytesPerSec**
</dt> <dd>

Nombre moyen d’octets par seconde.

</dd> <dt>

**AvgBytesPerSecGranularity**
</dt> <dd>

Granularité des valeurs d’octets par seconde.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,1<br/>                                                       |
| En-tête<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_majuscules de la configuration de flux TAPI \_ \_**](tapi-stream-config-caps.md)
</dt> </dl>

 

 




