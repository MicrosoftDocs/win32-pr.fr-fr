---
description: 'L’énumération AudioSettingsProperty est utilisée par les méthodes ITAudioSettings :: GetRange, ITAudioSettings :: obten et ITAudioSettings :: Set pour indiquer que la propriété de paramètre audio est traitée.'
ms.assetid: b91c8213-f102-4ebb-ad8a-e43709b3daad
title: Énumération AudioSettingsProperty (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b15cfb5a0211f02ac333ba75e47b5e4cbd5c44865b4a18c2f19ea3a8769dde3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118871529"
---
# <a name="audiosettingsproperty-enumeration"></a>Énumération AudioSettingsProperty

\[cette énumération n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’énumération **AudioSettingsProperty** est utilisée par les méthodes [**ITAudioSettings :: GetRange**](itaudiosettings-getrange.md), [**ITAudioSettings :: obten**](itaudiosettings-get.md)et [**ITAudioSettings :: Set**](itaudiosettings-set.md) pour indiquer que la propriété de paramètre audio est traitée.

## <a name="syntax"></a>Syntaxe


```C++
} AudioSettingsProperty;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="AudioSettings_SignalLevel"></span><span id="audiosettings_signallevel"></span><span id="AUDIOSETTINGS_SIGNALLEVEL"></span>**AudioSettings \_ SignalLevel**
</dt> <dd>

Propriété des paramètres de signal.

</dd> <dt>

<span id="AudioSettings_SilenceThreshold"></span><span id="audiosettings_silencethreshold"></span><span id="AUDIOSETTINGS_SILENCETHRESHOLD"></span>**AudioSettings \_ SilenceThreshold**
</dt> <dd>

Propriété de seuil de silence.

</dd> <dt>

<span id="AudioSettings_Volume"></span><span id="audiosettings_volume"></span><span id="AUDIOSETTINGS_VOLUME"></span>**\_Volume AudioSettings**
</dt> <dd>

Propriété de volume.

</dd> <dt>

<span id="AudioSettings_Balance"></span><span id="audiosettings_balance"></span><span id="AUDIOSETTINGS_BALANCE"></span>**AudioSettings \_ solde**
</dt> <dd>

Propriété balance.

</dd> <dt>

<span id="AudioSettings_Loudness"></span><span id="audiosettings_loudness"></span><span id="AUDIOSETTINGS_LOUDNESS"></span>**AudioSettings \_**
</dt> <dd>

Propriété intensité.

</dd> <dt>

<span id="AudioSettings_Treble"></span><span id="audiosettings_treble"></span><span id="AUDIOSETTINGS_TREBLE"></span>**\_Aigus AudioSettings**
</dt> <dd>

Propriété aigus.

</dd> <dt>

<span id="AudioSettings_Bass"></span><span id="audiosettings_bass"></span><span id="AUDIOSETTINGS_BASS"></span>**\_Basses AudioSettings**
</dt> <dd>

Propriété Bass.

</dd> <dt>

<span id="AudioSettings_Mono"></span><span id="audiosettings_mono"></span><span id="AUDIOSETTINGS_MONO"></span>**\_Mono AudioSettings**
</dt> <dd>

Propriété mono.

</dd> </dl>

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------|------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,1<br/>                                                       |
| En-tête<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITAudioSettings :: GetRange**](itaudiosettings-getrange.md)
</dt> <dt>

[**ITAudioSettings :: obtient**](itaudiosettings-get.md)
</dt> <dt>

[**ITAudioSettings :: Set**](itaudiosettings-set.md)
</dt> </dl>

 

 




