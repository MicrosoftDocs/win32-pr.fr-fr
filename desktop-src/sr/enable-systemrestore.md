---
title: Activer la méthode de la classe SystemRestore
description: Active la surveillance sur un lecteur particulier.
ms.assetid: f3140f6d-d190-46a4-8587-c2e928ac8ecf
keywords:
- Activer la restauration du système de méthode
- Activer la restauration du système de la méthode, classe SystemRestore
- Restauration du système de la classe SystemRestore, activer la méthode
topic_type:
- apiref
api_name:
- SystemRestore.Enable
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090aa01b4028a7146ea1d7f271ba4390f43ca260
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510144"
---
# <a name="enable-method-of-the-systemrestore-class"></a>Activer la méthode de la classe SystemRestore

Active la surveillance sur un lecteur particulier.

## <a name="syntax"></a>Syntaxe


```mof
uint32 Enable(
  [in] String Drive
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Lecteur* \[ dans\]
</dt> <dd>

Lecteur à activer. La chaîne de lecteur doit se présenter sous la forme « C : \\ ». Si ce paramètre est le lecteur système ou une chaîne vide (""), tous les lecteurs sont analysés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, la valeur de retour est S \_ OK. Sinon, la méthode retourne l’un des codes d’erreur COM définis dans WinError. h.

## <a name="remarks"></a>Notes

La méthode **Enable** n’attend pas l’activation complète de l’analyse avant son retour, car cela peut prendre un certain temps. Au lieu de cela, elle est retournée immédiatement après le démarrage du service de restauration du système et du pilote de filtre.

Pour activer la restauration du système sur un lecteur non-système, vous devez d’abord activer la restauration du système sur le lecteur système.

Cette méthode échoue en mode sans échec.

## <a name="examples"></a>Exemples


```VB
'Enable Method of the SystemRestore Class
'Enables monitoring on a particular drive.

Set Args = wscript.Arguments
If Args.Count() > 0 Then
    Drive = Args.item(0)
Else 
    Drive = ""
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
If (obj.Enable(Drive)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                         |
| Espace de noms<br/>                | Racine \\ par défaut<br/>                                                          |
| MOF<br/>                      | <dl> <dt>SR. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemRestore**](systemrestore.md)
</dt> </dl>

 

 





