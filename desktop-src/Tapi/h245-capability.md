---
description: L' \_ énumération des capacités h245 décrit la prise en charge des formats audio et vidéo.
ms.assetid: 76aeb3a1-3233-4425-b9db-efacbedc309e
title: Énumération H245_CAPABILITY (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae7a6f81f87480f221f87680d9cf086120deb2de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526662"
---
# <a name="h245_capability-enumeration"></a>\_Énumération des fonctionnalités h245

\[**H245 \_ La fonctionnalité** n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’énumération des **\_ capacités h245** décrit la prise en charge des formats audio et vidéo.

## <a name="syntax"></a>Syntaxe


```C++
} H245_CAPABILITY;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="HC_G711"></span><span id="hc_g711"></span>**\_G711 hc**
</dt> <dd>

Le protocole audio G. 711 est pris en charge.

</dd> <dt>

<span id="HC_G723"></span><span id="hc_g723"></span>**\_G723 hc**
</dt> <dd>

Le protocole audio G. 723 est pris en charge.

</dd> <dt>

<span id="HC_H263QCIF"></span><span id="hc_h263qcif"></span>**\_H263QCIF hc**
</dt> <dd>

Le protocole vidéo H. 263 est pris en charge.

</dd> <dt>

<span id="HC_H261QCIF"></span><span id="hc_h261qcif"></span>**\_H261QCIF hc**
</dt> <dd>

Le protocole vidéo H. 263 est pris en charge.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>H323priv. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IH323LineEx::SetDefaultCapabilityPreferrence**](ih323lineex-setdefaultcapabilitypreferrence.md)
</dt> </dl>

 

 




