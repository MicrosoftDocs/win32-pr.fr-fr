---
description: L’énumération du mode de bouclage de multidiffusion \_ \_ décrit le mode de bouclage de multidiffusion.
ms.assetid: bf9c3665-71cc-4cde-9ad4-1a8b62eddf9f
title: Énumération MULTICAST_LOOPBACK_MODE (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f322f723d6e1dfa7a0819c661b13d02fdfda753738f7cdb9c304c394bffc2a40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002837"
---
# <a name="multicast_loopback_mode-enumeration"></a>\_Énumération du mode de bouclage multicast \_

\[**Multidiffusion \_ le \_ MODE de bouclage** n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

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

 

 




