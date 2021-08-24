---
description: Définit un type de réseau BSS (Service Set) de base.
ms.assetid: 13d57339-655e-4978-974e-e7b12a83d18a
title: Énumération DOT11_BSS_TYPE (Wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_BSS_TYPE
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: 2d1c83ced842dbb876fea89271a160df2ca07fb9f02f415b13f8f1a46bc8dc79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780319"
---
# <a name="dot11_bss_type-enumeration"></a>\_ \_ Énumération des types BSS DOT11

Le type d’énumération de **\_ \_ type BSS DOT11** définit un type de réseau BSS (Basic Service Set).

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _DOT11_BSS_TYPE { 
  dot11_BSS_type_infrastructure  = 1,
  dot11_BSS_type_independent     = 2,
  dot11_BSS_type_any             = 3
} DOT11_BSS_TYPE, *PDOT11_BSS_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="dot11_BSS_type_infrastructure"></span><span id="dot11_bss_type_infrastructure"></span><span id="DOT11_BSS_TYPE_INFRASTRUCTURE"></span>**\_infrastructure de \_ type \_ BSS dot11**
</dt> <dd>

Spécifie un réseau BSS d’infrastructure.

</dd> <dt>

<span id="dot11_BSS_type_independent"></span><span id="dot11_bss_type_independent"></span><span id="DOT11_BSS_TYPE_INDEPENDENT"></span>**\_type BSS \_ dot11 \_ indépendant**
</dt> <dd>

Spécifie un réseau indépendant BSS (IBSS).

</dd> <dt>

<span id="dot11_BSS_type_any"></span><span id="dot11_bss_type_any"></span><span id="DOT11_BSS_TYPE_ANY"></span>**\_types BSS \_ dot11 \_ any**
</dt> <dd>

Spécifie l’infrastructure ou le réseau IBSS.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                        |
| Composant redistribuable<br/>          | API de réseau local sans fil pour Windows XP avec SP2<br/>                                                         |
| En-tête<br/>                   | <dl> <dt>Wlantypes. h (inclure Windot11. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**entrée réseau local sans fil \_ \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry)
</dt> <dt>

[**\_paramètres de connexion WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> <dt>

[**WlanGetNetworkBssList**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlangetnetworkbsslist)
</dt> </dl>

 

 




