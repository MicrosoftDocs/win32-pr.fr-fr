---
title: Désactivation de la méthode de la classe SystemRestore
description: Désactive la surveillance sur un lecteur particulier.
ms.assetid: 2ad37dd4-7d80-4697-9dbb-abb329a34ff7
keywords:
- Désactiver la restauration du système de méthode
- Désactiver la restauration du système de la méthode, classe SystemRestore
- Restauration du système de la classe SystemRestore, désactivation de la méthode
topic_type:
- apiref
api_name:
- SystemRestore.Disable
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41a05d53ee13e2f06c2f4765d2947f49a417ed798965406185619dfce207cf76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452920"
---
# <a name="disable-method-of-the-systemrestore-class"></a>Désactivation de la méthode de la classe SystemRestore

Désactive la surveillance sur un lecteur particulier.

## <a name="syntax"></a>Syntaxe


```mof
uint32 Disable(
  [in] String Drive
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Lecteur* \[ dans\]
</dt> <dd>

Lecteur à désactiver. La chaîne de lecteur doit se présenter sous la forme « C : \\ ». Si ce paramètre est le lecteur système ou une chaîne vide (""), aucun lecteur n’est analysé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, la valeur de retour est S \_ OK. Sinon, la méthode retourne l’un des codes d’erreur COM définis dans WinError. h.

## <a name="examples"></a>Exemples


```VB
'Disable Method of the SystemRestore Class
'Disables monitoring on a particular drive.
Set Args = wscript.Arguments
If Args.Count() > 0 Then
    Drive = Args.item(0)
Else
    Drive = ""
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")

If (obj.Disable(Drive)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                         |
| Espace de noms<br/>                | Racine \\ par défaut<br/>                                                          |
| MOF<br/>                      | <dl> <dt>SR. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemRestore**](systemrestore.md)
</dt> </dl>

 

 





