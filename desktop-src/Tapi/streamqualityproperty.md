---
description: 'Énumération StreamQualityProperty utilisée par les méthodes ITStreamQualityControl :: GetRange, ITStreamQualityControl :: obten et ITStreamQualityControl :: Set pour indiquer la propriété de qualité du flux qui est adressé.'
ms.assetid: 28c9257f-6fbb-440f-9b84-c15a74229b5b
title: Énumération StreamQualityProperty (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f552641cd0847bb3ff8eec9d528a03171a78c2e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324686"
---
# <a name="streamqualityproperty-enumeration"></a>Énumération StreamQualityProperty

\[cette énumération n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

Énumération **StreamQualityProperty** utilisée par les méthodes [**ITStreamQualityControl :: GetRange**](itstreamqualitycontrol-getrange.md), [**ITStreamQualityControl :: obten**](itstreamqualitycontrol-get.md)et [**ITStreamQualityControl :: Set**](itstreamqualitycontrol-set.md) pour indiquer la propriété de qualité du flux qui est adressé.

## <a name="syntax"></a>Syntaxe


```C++
} StreamQualityProperty;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="StreamQuality_MaxBitrate"></span><span id="streamquality_maxbitrate"></span><span id="STREAMQUALITY_MAXBITRATE"></span>**StreamQuality \_ MaxBitrate**
</dt> <dd>

Vitesse de transmission maximale.

</dd> <dt>

<span id="StreamQuality_CurrBitrate"></span><span id="streamquality_currbitrate"></span><span id="STREAMQUALITY_CURRBITRATE"></span>**StreamQuality \_ CurrBitrate**
</dt> <dd>

Vitesse de transmission minimale.

</dd> <dt>

<span id="StreamQuality_MinFrameInterval"></span><span id="streamquality_minframeinterval"></span><span id="STREAMQUALITY_MINFRAMEINTERVAL"></span>**StreamQuality \_ MinFrameInterval**
</dt> <dd>

Intervalle de trames maximal.

</dd> <dt>

<span id="StreamQuality_AvgFrameInterval"></span><span id="streamquality_avgframeinterval"></span><span id="STREAMQUALITY_AVGFRAMEINTERVAL"></span>**StreamQuality \_ AvgFrameInterval**
</dt> <dd>

Intervalle de frame minimal.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------|------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,1<br/>                                                       |
| En-tête<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITStreamQualityControl :: GetRange**](itstreamqualitycontrol-getrange.md)
</dt> <dt>

[**ITStreamQualityControl :: obtient**](itstreamqualitycontrol-get.md)
</dt> <dt>

[**ITStreamQualityControl :: Set**](itstreamqualitycontrol-set.md)
</dt> </dl>

 

 




