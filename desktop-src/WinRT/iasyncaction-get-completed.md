---
description: Obtient la méthode qui est appelée lorsque l’action asynchrone se termine.
ms.assetid: 5050BF84-F9E0-4B3E-9252-6C5C1060826E
title: 'IAsyncAction :: get_Completed, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.get_Completed
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 90e26947f0771490334ee731b25576759943c44cc47a9fda6681da9aa1f11fbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323440"
---
# <a name="iasyncactionget_completed-method"></a>IAsyncAction :: méthode d’extraction \_ terminée

Obtient la méthode qui est appelée lorsque l’action asynchrone se termine.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Completed(
  [out] AsyncActionCompletedHandler **handler
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Gestionnaire* \[ à\]
</dt> <dd>

Type : **[ **AsyncActionCompletedHandler**](asyncactioncompletedhandler.md)\*\***

Méthode qui gère la notification d’achèvement.

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

[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
