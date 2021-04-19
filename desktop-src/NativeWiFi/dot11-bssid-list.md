---
description: Contient une liste d’identificateurs BSS (Service Set) de base.
ms.assetid: 22907f94-1ae8-4938-a816-b406656256c0
title: Structure DOT11_BSSID_LIST (Windot11. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_BSSID_LIST
api_type:
- HeaderDef
api_location:
- windot11.h
ms.openlocfilehash: 345053a8d39ea37bea2fa2350dcc426420aed422
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518745"
---
# <a name="dot11_bssid_list-structure"></a>Structure de liste des \_ BSSID DOT11 \_

La structure de **\_ \_ liste des BSSID DOT11** contient une liste d’identificateurs BSS (Basic Service Set).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _DOT11_BSSID_LIST {
  NDIS_OBJECT_HEADER Header;
  ULONG              uNumOfEntries;
  ULONG              uTotalNumOfEntries;
  DOT11_MAC_ADDRESS  BSSIDs[1];
} DOT11_BSSID_LIST, *PDOT11_BSSID_LIST;
```



## <a name="members"></a>Membres

<dl> <dt>

**En-tête**
</dt> <dd>

Structure [**d' \_ \_ en-tête d’objet NDIS**](ndis-object-header.md) qui contient le type, la version et les informations de taille d’une structure NDIS. Pour la plupart des structures de **\_ \_ liste des BSSID dot11** , définissez **le type de membre sur** **NDIS \_ \_ \_ par défaut**, définissez le membre de **révision** sur **DOT11 \_ BSSID \_ List \_ révision \_ 1**, puis définissez le membre **Size** sur **sizeof ( \_ liste des BSSID dot11 \_ )**.

</dd> <dt>

**uNumOfEntries**
</dt> <dd>

Nombre d’entrées dans cette structure.

</dd> <dt>

**uTotalNumOfEntries**
</dt> <dd>

Nombre total d’entrées prises en charge.

</dd> <dt>

**BSSIDs**
</dt> <dd>

Liste d’identificateurs BSS. Un identificateur BSS est stocké en tant que type d' [**\_ \_ adresse Mac DOT11**](dot11-mac-address-type.md) .

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

[**\_paramètres de connexion WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> </dl>

 

 




