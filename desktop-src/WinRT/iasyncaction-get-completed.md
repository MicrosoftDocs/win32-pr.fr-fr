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
ms.openlocfilehash: bc018912b2b4643cc4ef2f48cc76eb997a2627fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113123"
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

 

 
