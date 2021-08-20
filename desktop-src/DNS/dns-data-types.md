---
title: Types de données DNS (windns. h)
ms.assetid: 652012a5-e45d-4ea6-896a-17e8b1ed4a05
description: En savoir plus sur les types de données DNS
keywords:
- IP4_ADDRESS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81756daaff73e7d5afc1b7c749cd976a9ede09d74ae70eb7db05d9e5d12f2f62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076863"
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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Windns. h</dt> </dl> |



 

 





