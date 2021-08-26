---
title: Types de données du service d’accès à distance (RAS. h)
description: Les types de données suivants sont utilisés par l’API du service d’accès à distance.
ms.assetid: aaa7f971-9c23-4738-a386-9b7db859f6be
keywords:
- RASIPV4ADDR
- RASIPV6ADDR
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26df8b8336b9b96ec338a79ed846519fb8a0ca019e6dd5996b9ac17087faa371
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028249"
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
> pris en charge dans Windows Vista ou les versions ultérieures de Windows.

 

</dd> <dt>

**RASIPV6ADDR**
</dt> <dd>

[**In6 \_ addr**](/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)) qui contient une adresse IPv6.

> [!Note]  
> pris en charge dans Windows Vista ou les versions ultérieures de Windows.

 

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>RAS. h</dt> </dl> |



 

