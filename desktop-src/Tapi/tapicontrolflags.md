---
description: L’énumération TAPIControlFlags est utilisée par un certain nombre de méthodes pour indiquer si une propriété donnée est contrôlée automatiquement ou manuellement.
ms.assetid: 48259444-bf7b-4f0e-9068-2bdf89dde694
title: Énumération TAPIControlFlags (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 278cc2328335409d4ffcc95ea136826d121acd57776f98aaad947c8fb9ee5d93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139802"
---
# <a name="tapicontrolflags-enumeration"></a>Énumération TAPIControlFlags

\[cette énumération n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’énumération **TAPIControlFlags** est utilisée par un certain nombre de méthodes pour indiquer si une propriété donnée est contrôlée automatiquement ou manuellement.

## <a name="syntax"></a>Syntaxe


```C++
} TAPIControlFlags;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="TAPIControl_Flags_None"></span><span id="tapicontrol_flags_none"></span><span id="TAPICONTROL_FLAGS_NONE"></span>**\_Indicateurs TAPIControl \_ aucun**
</dt> <dd>

L’interface TAPI n’a aucun indicateur de contrôle pour la propriété.

</dd> <dt>

<span id="TAPIControl_Flags_Auto"></span><span id="tapicontrol_flags_auto"></span><span id="TAPICONTROL_FLAGS_AUTO"></span>**TAPIControl les \_ indicateurs \_ automatiquement**
</dt> <dd>

La propriété est contrôlée automatiquement.

</dd> <dt>

<span id="TAPIControl_Flags_Manual"></span><span id="tapicontrol_flags_manual"></span><span id="TAPICONTROL_FLAGS_MANUAL"></span>**\_Manuel des indicateurs TAPIControl \_**
</dt> <dd>

La propriété est contrôlée manuellement.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,1<br/>                                                       |
| En-tête<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITAudioDeviceControl :: GetRange**](itaudiodevicecontrol-getrange.md)
</dt> <dt>

[**ITAudioDeviceControl :: obtient**](itaudiodevicecontrol-get.md)
</dt> <dt>

[**ITAudioDeviceControl :: Set**](itaudiodevicecontrol-set.md)
</dt> <dt>

[**ITAudioSettings :: GetRange**](itaudiosettings-getrange.md)
</dt> <dt>

[**ITAudioSettings :: obtient**](itaudiosettings-get.md)
</dt> <dt>

[**ITAudioSettings :: Set**](itaudiosettings-set.md)
</dt> <dt>

[**ITCallQualityControl :: GetRange**](itcallqualitycontrol-getrange.md)
</dt> <dt>

[**ITCallQualityControl :: obtient**](itcallqualitycontrol-get.md)
</dt> <dt>

[**ITCallQualityControl :: Set**](itcallqualitycontrol-set.md)
</dt> <dt>

[**ITStreamQualityControl :: GetRange**](itstreamqualitycontrol-getrange.md)
</dt> <dt>

[**ITStreamQualityControl :: obtient**](itstreamqualitycontrol-get.md)
</dt> <dt>

[**ITStreamQualityControl :: Set**](itstreamqualitycontrol-set.md)
</dt> </dl>

 

 




