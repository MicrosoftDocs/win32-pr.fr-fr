---
title: Méthode IMsRdpDeviceCollection2 RedirectNow
description: Force la redirection ou la suppression des appareils qui ont été sélectionnés ou désélectionnés dans la collection.
ms.assetid: 9cd5849d-a589-43f3-b904-6b2e15ca033d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RedirectNow
- Méthode RedirectNow Services Bureau à distance, interface IMsRdpDeviceCollection2
- Services Bureau à distance de l’interface IMsRdpDeviceCollection2, méthode RedirectNow
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2.RedirectNow
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 893d1e26f504d5aeb45f795ea7425eeefc3a6232
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941681"
---
# <a name="imsrdpdevicecollection2redirectnow-method"></a>IMsRdpDeviceCollection2 :: RedirectNow, méthode

Force la redirection ou la suppression des appareils qui ont été sélectionnés ou désélectionnés dans la collection.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RedirectNow(
  [in] RedirectDeviceType Type
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Type* \[ dans\]
</dt> <dd>

Type : **[ **RedirectDeviceType**](redirectdevicetype.md)**

Valeur de l’énumération [**RedirectDeviceType**](redirectdevicetype.md) qui spécifie le type de périphérique à rediriger.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RedirectDeviceType**](redirectdevicetype.md)
</dt> <dt>

[**IMsRdpDeviceCollection2**](imsrdpdevicecollection2.md)
</dt> </dl>

 

 





