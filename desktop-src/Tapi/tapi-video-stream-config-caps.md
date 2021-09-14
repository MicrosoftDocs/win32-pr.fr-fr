---
description: La \_ \_ \_ structure d’embouts de la configuration du flux vidéo TAPI \_ est contenue dans la structure de la \_ configuration du flux TAPI \_ \_ lorsque le membre CapsType est défini sur le membre VideoCap de l’Union StreamConfigCapsType.
ms.assetid: 8812755a-50e8-4d8e-ab67-7a3a4b2a4a67
title: Structure TAPI_VIDEO_STREAM_CONFIG_CAPS (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 525a35cb7c7332aa4e80fe8d5e2436e75e2d5c08
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311154"
---
# <a name="tapi_video_stream_config_caps-structure"></a>\_Structure d' \_ \_ \_ embouts de la configuration du flux vidéo TAPI

\[cette structure n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La structure d' **\_ \_ \_ \_ embouts de la configuration du flux vidéo TAPI** est contenue dans la  structure de la [**\_ \_ configuration \_ du flux TAPI**](tapi-stream-config-caps.md) lorsque le membre CapsType est défini sur le membre **VideoCap** de l’Union [**StreamConfigCapsType**](streamconfigcapstype.md) .

## <a name="syntax"></a>Syntaxe


```C++
} TAPI_VIDEO_STREAM_CONFIG_CAPS;
```



## <a name="members"></a>Membres

<dl> <dt>

**Description**
</dt> <dd>

Description conviviale du type de configuration de flux audio à afficher aux utilisateurs de l’application.

</dd> <dt>

**VideoStandard**
</dt> <dd>

Standard vidéo en cours d’utilisation.

</dd> <dt>

**Inverser**
</dt> <dd>

Taille d’entrée du frame.

</dd> <dt>

**MinCroppingSize**
</dt> <dd>

Taille minimale du rognage.

</dd> <dt>

**MaxCroppingSize**
</dt> <dd>

Taille maximale du rognage.

</dd> <dt>

**CropGranularityX**
</dt> <dd>

Granularité du rognage autorisé le long de l’axe x.

</dd> <dt>

**CropGranularityY**
</dt> <dd>

Granularité du rognage autorisé le long de l’axe y.

</dd> <dt>

**CropAlignX**
</dt> <dd>

Alignement du rognage de l’axe x.

</dd> <dt>

**CropAlignY**
</dt> <dd>

Alignement du rognage de l’axe y.

</dd> <dt>

**MinOutputSize**
</dt> <dd>

Taille minimale résultante de la fenêtre vidéo.

</dd> <dt>

**MaxOutputSize**
</dt> <dd>

Taille maximale résultante de la fenêtre vidéo.

</dd> <dt>

**OutputGranularityX**
</dt> <dd>

Granularité de la taille de sortie le long de l’axe x.

</dd> <dt>

**OutputGranularityY**
</dt> <dd>

Granularité de la taille de sortie le long de l’axe y.

</dd> <dt>

**StretchTapsX**
</dt> <dd>

Étirer le long de l’axe x.

</dd> <dt>

**StretchTapsY**
</dt> <dd>

Étirement le long de l’axe y.

</dd> <dt>

**ShrinkTapsX**
</dt> <dd>

Rétrécir le long de l’axe x.

</dd> <dt>

**ShrinkTapsY**
</dt> <dd>

Rétrécir le long de l’axe y.

</dd> <dt>

**MinFrameInterval**
</dt> <dd>

Intervalle de trame vidéo minimal.

</dd> <dt>

**MaxFrameInterval**
</dt> <dd>

Intervalle de trame vidéo maximal.

</dd> <dt>

**MinBitsPerSecond**
</dt> <dd>

Nombre minimal de bits par seconde.

</dd> <dt>

**MaxBitsPerSecond**
</dt> <dd>

Nombre maximal de bits par seconde.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------|------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,1<br/>                                                       |
| En-tête<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_majuscules de la configuration de flux TAPI \_ \_**](tapi-stream-config-caps.md)
</dt> </dl>

 

 




