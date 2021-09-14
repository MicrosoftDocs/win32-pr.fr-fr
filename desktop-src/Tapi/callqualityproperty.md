---
description: 'L’énumération CallQualityProperty est utilisée par les méthodes ITCallQualityControl :: GetRange, ITCallQualityControl :: obten et ITCallQualityControl :: Set pour indiquer que la propriété de qualité d’appel est traitée.'
ms.assetid: d9a04cc4-9b7d-4b01-918f-e4938c172b8e
title: Énumération CallQualityProperty (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2ca3af31e0b85a443bb34ac1992b3d3b5c89bfa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008779"
---
# <a name="callqualityproperty-enumeration"></a>Énumération CallQualityProperty

\[cette énumération n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’énumération **CallQualityProperty** est utilisée par les méthodes [**ITCallQualityControl :: GetRange**](itcallqualitycontrol-getrange.md), [**ITCallQualityControl :: obten**](itcallqualitycontrol-get.md)et [**ITCallQualityControl :: Set**](itcallqualitycontrol-set.md) pour indiquer que la propriété de qualité d’appel est traitée.

## <a name="syntax"></a>Syntaxe


```C++
} CallQualityProperty;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="CallQuality_ControlInterval"></span><span id="callquality_controlinterval"></span><span id="CALLQUALITY_CONTROLINTERVAL"></span>**CallQuality \_ ControlInterval**
</dt> <dd>

Intervalle de contrôle.

</dd> <dt>

<span id="CallQuality_ConfBitrate"></span><span id="callquality_confbitrate"></span><span id="CALLQUALITY_CONFBITRATE"></span>**CallQuality \_ ConfBitrate**
</dt> <dd>

Vitesse de transmission de la Conférence.

</dd> <dt>

<span id="CallQuality_MaxInputBitrate"></span><span id="callquality_maxinputbitrate"></span><span id="CALLQUALITY_MAXINPUTBITRATE"></span>**CallQuality \_ MaxInputBitrate**
</dt> <dd>

Débit d’entrée maximal.

</dd> <dt>

<span id="CallQuality_CurrInputBitrate"></span><span id="callquality_currinputbitrate"></span><span id="CALLQUALITY_CURRINPUTBITRATE"></span>**CallQuality \_ CurrInputBitrate**
</dt> <dd>

Vitesse d’entrée actuelle.

</dd> <dt>

<span id="CallQuality_MaxOutputBitrate"></span><span id="callquality_maxoutputbitrate"></span><span id="CALLQUALITY_MAXOUTPUTBITRATE"></span>**CallQuality \_ MaxOutputBitrate**
</dt> <dd>

Vitesse de transmission maximale.

</dd> <dt>

<span id="CallQuality_CurrOutputBitrate"></span><span id="callquality_curroutputbitrate"></span><span id="CALLQUALITY_CURROUTPUTBITRATE"></span>**CallQuality \_ CurrOutputBitrate**
</dt> <dd>

Vitesse de transmission en sortie actuelle.

</dd> <dt>

<span id="CallQuality_MaxCPULoad"></span><span id="callquality_maxcpuload"></span><span id="CALLQUALITY_MAXCPULOAD"></span>**CallQuality \_ MaxCPULoad**
</dt> <dd>

Charge de l’UC maximale.

</dd> <dt>

<span id="CallQuality_CurrCPULoad"></span><span id="callquality_currcpuload"></span><span id="CALLQUALITY_CURRCPULOAD"></span>**CallQuality \_ CurrCPULoad**
</dt> <dd>

Charge de l’UC actuelle.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,1<br/>                                                       |
| En-tête<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITCallQualityControl :: GetRange**](itcallqualitycontrol-getrange.md)
</dt> <dt>

[**ITCallQualityControl :: obtient**](itcallqualitycontrol-get.md)
</dt> <dt>

[**ITCallQualityControl :: Set**](itcallqualitycontrol-set.md)
</dt> </dl>

 

 




