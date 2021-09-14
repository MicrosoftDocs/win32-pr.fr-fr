---
title: Types de données DNS (windns. h)
ms.assetid: 652012a5-e45d-4ea6-896a-17e8b1ed4a05
description: En savoir plus sur les types de données DNS
keywords:
- IP4_ADDRESS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2caa113670a749029b70df9772d6e2707684b7c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114693"
---
# <a name="dns-data-types"></a>Types de données DNS

Les types de données suivants sont définis pour DNS :


```C++
typedef DWORD IP4_ADDRESS;
```



<dl> <dt>

**\_Adresse adresse IP4**
</dt> <dd>

Valeur qui représente une adresse IPv4 (Internet Protocol version 4). Par exemple, l’adresse IPv4 décimale séparée par des points, **127.0.0.1**, est représentée dans l’ordre d’octet de l’hôte en tant que **0x7F000001**.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Windns. h</dt> </dl> |



 

 





