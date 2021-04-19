---
description: L’énumération du mode de bouclage de multidiffusion \_ \_ décrit le mode de bouclage de multidiffusion.
ms.assetid: bf9c3665-71cc-4cde-9ad4-1a8b62eddf9f
title: Énumération MULTICAST_LOOPBACK_MODE (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a15505efcd1a9e399866b104da0582ccf846689
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531157"
---
# <a name="multicast_loopback_mode-enumeration"></a>\_Énumération du mode de bouclage multicast \_

\[**Multidiffusion \_ Le \_ mode de bouclage** n’est pas disponible pour une utilisation dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’énumération du **\_ \_ mode de bouclage de multidiffusion** décrit le mode de bouclage de multidiffusion.

## <a name="syntax"></a>Syntaxe


```C++
} MULTICAST_LOOPBACK_MODE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MM_NO_LOOPBACK"></span><span id="mm_no_loopback"></span>**MM \_ pas de \_ bouclage**
</dt> <dd>

Le bouclage de multidiffusion est désactivé. Cela signifie que deux applications sur le même ordinateur qui rejoignent le même groupe de multidiffusion peuvent se procurer les paquets de chacun d’eux.

</dd> <dt>

<span id="MM_FULL_LOOPBACK"></span><span id="mm_full_loopback"></span>**MM \_ de \_ boucle complète**
</dt> <dd>

Tous les paquets envoyés sont également renvoyés en boucle. Ce mode est utile uniquement pour les tests.

</dd> <dt>

<span id="MM_SELECTIVE_LOOPBACK"></span><span id="mm_selective_loopback"></span>**\_boucle mm sélective \_**
</dt> <dd>

Le bouclage sélectif est activé. Cela signifie que l’activation de plusieurs applications sur un même ordinateur peut joindre le même groupe de multidiffusion sans confusion. Les paquets sont rebouclés de la pile et chaque session RTP est chargée de filtrer les paquets indésirables.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMulticastControl :: obtient \_ LoopbackMode**](imulticastcontrol-get-loopbackmode.md)
</dt> <dt>

[**IMulticastControl ::p ut \_ LoopbackMode**](imulticastcontrol-put-loopbackmode.md)
</dt> </dl>

 

 




