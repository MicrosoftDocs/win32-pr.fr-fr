---
description: Appelle la méthode qui est appelée lorsque l’action asynchrone spécifiée se termine.
ms.assetid: 97199C1A-7CE3-4BBD-86A3-2CA9B27CC05E
title: 'AsyncActionCompletedHandler :: Invoke, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncActionCompletedHandler.Invoke
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: f106dca9d1d01b2da12ffb527f3556a0a44cf535167e5af79adbd69e4a097055
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898649"
---
# <a name="asyncactioncompletedhandlerinvoke-method"></a>AsyncActionCompletedHandler :: Invoke, méthode

Appelle la méthode qui est appelée lorsque l’action asynchrone spécifiée se termine.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Invoke(
  [in] IAsyncAction *asyncInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*asyncInfo* \[ dans\]
</dt> <dd>

Type : **[ **IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)\***

Action asynchrone qui signale la fin de l’opération.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                    |
| En-tête<br/>                   | <dl> <dt>Windows. Foundation. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**AsyncActionCompletedHandler**](asyncactioncompletedhandler.md)
</dt> </dl>

 

