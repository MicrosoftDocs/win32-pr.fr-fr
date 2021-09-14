---
title: IMsRdpClient7 propriété TransportSettings3
description: Récupère un objet qui prend en charge l’interface IMsRdpClientTransportSettings3.
ms.assetid: d11f0943-241e-44cd-a98c-595916ab0718
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété TransportSettings3
- Services Bureau à distance de la propriété TransportSettings3, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété TransportSettings3
- Services Bureau à distance de la propriété TransportSettings3, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété TransportSettings3
- Services Bureau à distance de la propriété TransportSettings3, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété TransportSettings3
- Services Bureau à distance de la propriété TransportSettings3, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, propriété TransportSettings3
topic_type:
- apiref
api_name:
- IMsRdpClient7.TransportSettings3
- IMsRdpClient7.get_TransportSettings3
- IMsRdpClient8.TransportSettings3
- IMsRdpClient8.get_TransportSettings3
- IMsRdpClient9.TransportSettings3
- IMsRdpClient9.get_TransportSettings3
- IMsRdpClient10.TransportSettings3
- IMsRdpClient10.get_TransportSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c60b58f8f2438de0d43f69ce0b3bb73607e7551
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126920060"
---
# <a name="imsrdpclient7transportsettings3-property"></a>IMsRdpClient7 :: TransportSettings3, propriété

Récupère un objet qui prend en charge l’interface [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) .

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_TransportSettings3(
  [out, retval] IMsRdpClientTransportSettings3 **ppXportSet3
);
```



## <a name="property-value"></a>Valeur de la propriété

Adresse d’un pointeur d’interface [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) qui reçoit l’objet.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                      |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient7 est défini en tant que b2a5b5ce-3461-444A-91D4-add26d070638<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





