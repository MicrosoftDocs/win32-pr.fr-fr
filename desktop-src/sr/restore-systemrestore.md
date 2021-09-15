---
title: Méthode Restore de la classe SystemRestore
description: Lance une restauration du système.
ms.assetid: ca4aa97b-fa59-407d-b127-951d46932c33
keywords:
- Restaurer la méthode restauration du système
- Restore, méthode restauration du système, classe SystemRestore
- Restauration du système de la classe SystemRestore, méthode Restore
topic_type:
- apiref
api_name:
- SystemRestore.Restore
api_location:
- Root\\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b7747b710801718d9b169c8999c51dd30cefde
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412320"
---
# <a name="restore-method-of-the-systemrestore-class"></a>Méthode Restore de la classe SystemRestore

Lance une restauration du système. L’appelant doit forcer un redémarrage du système. La restauration réelle se produit lors du redémarrage.

## <a name="syntax"></a>Syntaxe


```mof
uint32 Restore(
  [in] uint32 SequenceNumber
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

 N \[ dans\]
</dt> <dd>

Numéro de séquence du point de restauration. Pour déterminer le numéro de séquence d’un point de restauration spécifique, énumérez tous les points de restauration sur le système.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la méthode est réussie, la valeur de retour est S \_ OK. Sinon, la méthode retourne l’un des codes d’erreur COM définis dans WinError. h.

## <a name="examples"></a>Exemples


```VB
'Restore Method of the SystemRestore Class
'Initiates a system restore. The caller must 
'force a system reboot. The actual restoration 
'occurs during the reboot.
Set Args = wscript.Arguments
RpNum = Args.item(0)
Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
if obj.Restore(RpNum) <> 0 Then
    wscript.Echo "Restore failed"
End If
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
for each OpSys in OpSysSet
    OpSys.Reboot()
next
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                         |
| Espace de noms<br/>                | Racine \\ \\ par défaut<br/>                                                        |
| MOF<br/>                      | <dl> <dt>SR. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemRestore**](systemrestore.md)
</dt> </dl>

 

 





