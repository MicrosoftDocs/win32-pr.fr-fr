---
title: Méthode GetLastRestoreStatus de la classe SystemRestore
description: Récupère l’état de la dernière restauration du système.
ms.assetid: 03f9fd71-9f20-428e-bdca-4692e838581a
keywords:
- Restauration du système de méthode GetLastRestoreStatus
- Restauration du système de méthode GetLastRestoreStatus, classe SystemRestore
- Restauration du système de la classe SystemRestore, méthode GetLastRestoreStatus
topic_type:
- apiref
api_name:
- SystemRestore.GetLastRestoreStatus
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd1ef0e62f7874bb92f3c8e9ecec7b62a1b3ff3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512777"
---
# <a name="getlastrestorestatus-method-of-the-systemrestore-class"></a>Méthode GetLastRestoreStatus de la classe SystemRestore

Récupère l’état de la dernière restauration du système.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetLastRestoreStatus();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs d’État suivantes.



| Valeur retournée                                                                 | Description                                  |
|------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>0</dt> </dl> | La dernière restauration a échoué.<br/>          |
| <dl> <dt>1</dt> </dl> | La dernière restauration a réussi.<br/>  |
| <dl> <dt>2</dt> </dl> | La dernière restauration a été interrompue.<br/> |



 

## <a name="examples"></a>Exemples


```VB
'GetLastRestoreStatus Method of the SystemRestore Class
'Retrieves the status of the last system restore.
Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
stat = obj.GetLastRestoreStatus()
If stat = 0 Then
    wscript.Echo "Failed"
ElseIf stat = 1 Then 
    wscript.Echo "Success"
ElseIf stat = 2 Then
    wscript.Echo "Interrrupted"
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

 

 





