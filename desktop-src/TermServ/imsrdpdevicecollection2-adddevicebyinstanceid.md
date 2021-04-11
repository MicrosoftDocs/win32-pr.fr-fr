---
title: Méthode IMsRdpDeviceCollection2 AddDeviceByInstanceId
description: Ajoute un appareil non répertorié au regroupement de périphériques.
ms.assetid: 7ef200c5-b99e-40c9-80e1-0758ddfa0902
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode AddDeviceByInstanceId
- Méthode AddDeviceByInstanceId Services Bureau à distance, interface IMsRdpDeviceCollection2
- Services Bureau à distance de l’interface IMsRdpDeviceCollection2, méthode AddDeviceByInstanceId
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2.AddDeviceByInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f817a5beb4d8762787c4bf2f8a3995d3918e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032376"
---
# <a name="imsrdpdevicecollection2adddevicebyinstanceid-method"></a>IMsRdpDeviceCollection2 :: AddDeviceByInstanceId, méthode

Ajoute un appareil non répertorié au regroupement de périphériques.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AddDeviceByInstanceId(
  [in] RedirectDeviceType Type,
  [in] BSTR               InstanceId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Type* \[ dans\]
</dt> <dd>

Type : **[ **RedirectDeviceType**](redirectdevicetype.md)**

Valeur de l’énumération [**RedirectDeviceType**](redirectdevicetype.md) qui spécifie le type d’appareil ajouté.

</dd> <dt>

*InstanceID* \[ dans\]
</dt> <dd>

Type : **BSTR**

Identificateur d’instance de l’appareil à ajouter.

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

 

 





