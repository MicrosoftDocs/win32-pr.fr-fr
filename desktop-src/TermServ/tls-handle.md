---
title: TLS_HANDLE
description: Représente un handle vers un serveur de licences Bureau à distance.
ms.assetid: 6da51660-a9fd-4e49-97e3-ba0829b1bbbf
ms.tgt_platform: multiple
keywords:
- TLS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09764072b42e14aea2d1b8242dbc3cbb044442b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120570"
---
# <a name="tls_handle"></a>\_handle TLS

Représente un handle vers un serveur de licences Bureau à distance. Ce descripteur est retourné par la fonction [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .

> [!Note]  
> Ce type de données n’a aucun fichier d’en-tête associé. Pour l’utiliser, vous devez le définir vous-même comme indiqué dans cette rubrique.

 


```C++
typedef HANDLE TLS_HANDLE;
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dt>

[**TLSDisconnectFromServer**](tlsdisconnectfromserver.md)
</dt> </dl>

 

 





