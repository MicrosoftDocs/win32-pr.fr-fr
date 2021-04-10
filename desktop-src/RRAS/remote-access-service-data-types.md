---
title: Types de données du service d’accès à distance (RAS. h)
description: Les types de données suivants sont utilisés par l’API du service d’accès à distance.
ms.assetid: aaa7f971-9c23-4738-a386-9b7db859f6be
keywords:
- RASIPV4ADDR
- RASIPV6ADDR
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c8aa2fdae531c5aae0986d3289802565c6914fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942094"
---
# <a name="remote-access-service-data-types"></a>Types de données du service d’accès à distance

Les types de données suivants sont utilisés par l’API du service d’accès à distance.


```C++
typedef in_addr RASIPV4ADDR;
typedef in6_addr RASIPV6ADDR;
```



<dl> <dt>

**RASIPV4ADDR**
</dt> <dd>

[**Dans \_ addr**](/windows/desktop/api/winsock2/ns-winsock2-in_addr) qui contient une adresse IPv4.

> [!Note]  
> Pris en charge dans Windows Vista ou les versions ultérieures de Windows.

 

</dd> <dt>

**RASIPV6ADDR**
</dt> <dd>

[**In6 \_ addr**](/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)) qui contient une adresse IPv6.

> [!Note]  
> Pris en charge dans Windows Vista ou les versions ultérieures de Windows.

 

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>RAS. h</dt> </dl> |



 

