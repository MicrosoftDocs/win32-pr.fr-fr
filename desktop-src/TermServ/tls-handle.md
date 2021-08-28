---
title: TLS_HANDLE
description: Représente un handle vers un serveur de licences Bureau à distance.
ms.assetid: 6da51660-a9fd-4e49-97e3-ba0829b1bbbf
ms.tgt_platform: multiple
keywords:
- TLS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04daf14429a5b400267e664a615739fd14e8306e987f50726cfdb341522870a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869449"
---
# <a name="tls_handle"></a>\_handle TLS

Représente un handle vers un serveur de licences Bureau à distance. Ce descripteur est retourné par la fonction [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .

> [!Note]  
> Ce type de données n’a aucun fichier d’en-tête associé. Pour l’utiliser, vous devez le définir vous-même comme indiqué dans cette rubrique.

 


```C++
typedef HANDLE TLS_HANDLE;
```



## <a name="requirements"></a>Configuration requise



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

 

 





