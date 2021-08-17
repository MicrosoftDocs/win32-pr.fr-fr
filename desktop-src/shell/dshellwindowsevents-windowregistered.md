---
description: Appelé lorsqu’une fenêtre est inscrite en tant que fenêtre d’interpréteur de commandes.
title: Méthode DShellWindowsEvents. WindowRegistered
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents.WindowRegistered
api_type:
- COM
api_location:
- Shdocvw.dll
ms.assetid: 7faf758a-daa0-47f5-9f95-61fe3d8286ea
ms.openlocfilehash: 7ad7270f9054b875eabcb1fd9f5a7ab2e299a5916d55ef4630988921b6b2f4ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455569"
---
# <a name="dshellwindowseventswindowregistered-method"></a>Méthode DShellWindowsEvents. WindowRegistered

Appelé lorsqu’une fenêtre est inscrite en tant que fenêtre d’interpréteur de commandes.

## <a name="syntax"></a>Syntaxe


```JScript
DShellWindowsEvents.WindowRegistered(
  lCookie
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lCookie* \[ dans\]
</dt> <dd>

Type : **entier**

Cookie qui identifie la fenêtre qui a été inscrite.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Une fenêtre reçoit un cookie lorsqu’elle est inscrite en tant que fenêtre d’interpréteur de commandes. Pour plus d’informations, consultez [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Product<br/> | Internet Explorer 5<br/>                                                                                           |
| DLL<br/>     | <dl> <dt>Shdocvw.dll (version 5.00.2014.0216 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DShellWindowsEvents**](dshellwindowsevents.md)
</dt> <dt>

[**WindowRevoked**](dshellwindowsevents-windowrevoked.md)
</dt> <dt>

[**Annuler**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register)
</dt> <dt>

[**RegisterPending**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-registerpending)
</dt> </dl>

 

 




