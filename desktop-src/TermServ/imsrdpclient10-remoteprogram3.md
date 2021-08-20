---
title: IMsRdpClient10 propriété RemoteProgram3
description: Objet qui prend en charge l’interface ITSRemoteProgram3.
ms.assetid: afb26152-32eb-45de-a228-a6f7ca7eea2b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RemoteProgram3
- Services Bureau à distance de la propriété RemoteProgram3, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, propriété RemoteProgram3
topic_type:
- apiref
api_name:
- IMsRdpClient10.RemoteProgram3
- IMsRdpClient10.get_RemoteProgram3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f332985777d6b83e04724e6bf0af65b06b3cac50d73ba437647dc93944f76e8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130282"
---
# <a name="imsrdpclient10remoteprogram3-property"></a>IMsRdpClient10 :: RemoteProgram3, propriété

Objet qui prend en charge l’interface [**ITSRemoteProgram3**](itsremoteprogram3.md) .

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_RemoteProgram3(
  [out, retval] ITSRemoteProgram3 **ppRemoteProgram
);
```



## <a name="property-value"></a>Valeur de la propriété

Retourne un pointeur d’interface [**ITSRemoteProgram3**](itsremoteprogram3.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





