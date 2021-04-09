---
description: Sont utilisées pour définir une adresse MAC (Media Access Control).
ms.assetid: c1335127-a2d2-4f44-a895-1abbc5eaf98d
title: DOT11_MAC_ADDRESS (Windot11. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77b43635462c4b48890599512cc1a413461de72e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866041"
---
# <a name="dot11_mac_address"></a>\_Adresse Mac \_ DOT11

Les types d' **\_ \_ adresses Mac DOT11** sont utilisés pour définir une adresse Mac (Media Access Control).


```C++
typedef UCHAR DOT11_MAC_ADDRESS[6];
typedef DOT11_MAC_ADDRESS* PDOT11_MAC_ADDRESS;
```



<dl> <dt>

**\_Adresse Mac \_ DOT11 \[ 6\]**
</dt> <dd>

Adresse MAC dans un format de monodiffusion, de multidiffusion ou de diffusion.

</dd> <dt>

**\_Adresse Mac \_ PDOT11**
</dt> <dd>

Pointeur vers une adresse MAC dans un format de monodiffusion, de multidiffusion ou de diffusion.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                       |
| Composant redistribuable<br/>          | API de réseau local sans fil pour Windows XP avec SP2<br/>                                                        |
| En-tête<br/>                   | <dl> <dt>Windot11. h (inclure Windot11. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Liste des BSSID DOT11 \_**](dot11-bssid-list.md)
</dt> <dt>

[**\_attributs d’association WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_association_attributes)
</dt> <dt>

[**entrée réseau local sans fil \_ \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry)
</dt> </dl>

 

 




