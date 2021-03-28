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
ms.openlocfilehash: b036bdde2916c2fa037d1b6e286a2096d9e1d8bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104983082"
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

## <a name="remarks"></a>Notes

Une fenêtre reçoit un cookie lorsqu’elle est inscrite en tant que fenêtre d’interpréteur de commandes. Pour plus d’informations, consultez [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).

## <a name="requirements"></a>Spécifications



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

[**Révoquer**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-revoke)
</dt> </dl>

 

 




