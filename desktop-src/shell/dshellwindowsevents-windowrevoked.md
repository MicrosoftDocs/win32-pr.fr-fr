---
description: Appelé lorsque l’inscription d’une fenêtre d’interpréteur de commandes est révoquée.
title: Méthode DShellWindowsEvents. WindowRevoked
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents.WindowRevoked
api_type:
- COM
api_location:
- Shdocvw.dll
ms.assetid: 92e8653f-7f41-4e0b-97e5-429fddc51951
ms.openlocfilehash: 571808962d65d25d4fb08f8d4cb57ffd1d51da67a7ba60def191edcf2fe19575
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459846"
---
# <a name="dshellwindowseventswindowrevoked-method"></a>Méthode DShellWindowsEvents. WindowRevoked

Appelé lorsque l’inscription d’une fenêtre d’interpréteur de commandes est révoquée.

## <a name="syntax"></a>Syntaxe


```JScript
DShellWindowsEvents.WindowRevoked(
  lCookie
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lCookie* \[ dans\]
</dt> <dd>

Type : **entier**

Cookie qui identifie la fenêtre qui a été révoquée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Une fenêtre reçoit un cookie lorsqu’elle est inscrite en tant que fenêtre d’interpréteur de commandes. Pour plus d’informations, consultez [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Produit<br/> | Internet Explorer 5<br/>                                                                                           |
| DLL<br/>     | <dl> <dt>Shdocvw.dll (version 5.00.2014.0216 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DShellWindowsEvents**](dshellwindowsevents.md)
</dt> <dt>

[**WindowRegistered**](dshellwindowsevents-windowregistered.md)
</dt> <dt>

[**Supprimés**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-revoke)
</dt> </dl>

 

 




