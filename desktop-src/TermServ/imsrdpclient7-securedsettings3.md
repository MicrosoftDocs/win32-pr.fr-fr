---
title: IMsRdpClient7 propriété SecuredSettings3
description: Récupère un objet qui prend en charge l’interface IMsRdpClientSecuredSettings2.
ms.assetid: 500ce7ed-bd86-434c-baf8-f30dd667dca3
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété SecuredSettings3
- Services Bureau à distance de la propriété SecuredSettings3, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété SecuredSettings3
- Services Bureau à distance de la propriété SecuredSettings3, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété SecuredSettings3
- Services Bureau à distance de la propriété SecuredSettings3, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété SecuredSettings3
- Services Bureau à distance de la propriété SecuredSettings3, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, propriété SecuredSettings3
topic_type:
- apiref
api_name:
- IMsRdpClient7.SecuredSettings3
- IMsRdpClient7.get_SecuredSettings3
- IMsRdpClient8.SecuredSettings3
- IMsRdpClient8.get_SecuredSettings3
- IMsRdpClient9.SecuredSettings3
- IMsRdpClient9.get_SecuredSettings3
- IMsRdpClient10.SecuredSettings3
- IMsRdpClient10.get_SecuredSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 219e3373a6ecb2f5b963a82800f4415f7de64534
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384191"
---
# <a name="imsrdpclient7securedsettings3-property"></a>IMsRdpClient7 :: SecuredSettings3, propriété

Récupère un objet qui prend en charge l’interface [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) .

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_SecuredSettings3(
  [out] IMsRdpClientSecuredSettings2 **ppSecuredSettings
);
```



## <a name="property-value"></a>Valeur de la propriété

Adresse d’un pointeur d’interface [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) qui reçoit l’objet.

## <a name="requirements"></a>Configuration requise



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

 

 





