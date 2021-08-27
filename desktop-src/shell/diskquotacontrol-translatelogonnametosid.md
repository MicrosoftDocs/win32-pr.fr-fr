---
description: Convertit un nom d’ouverture de session en ID de sécurité de l’utilisateur correspondant au format de chaîne.
title: Méthode DiskQuotaControl. TranslateLogonNameToSID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.TranslateLogonNameToSID
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3b6b0d03-e9ef-4575-bb67-f7b7b39d2a16
ms.openlocfilehash: 6bcaa5ac4f7dff4be80763b0aa411b7f104ff786b21e422044bdc7198697d54c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111819"
---
# <a name="diskquotacontroltranslatelogonnametosid-method"></a>Méthode DiskQuotaControl. TranslateLogonNameToSID

Convertit un nom d’ouverture de session en ID de sécurité de l’utilisateur correspondant au format de chaîne.

## <a name="syntax"></a>Syntaxe


```JScript
DiskQuotaControl.TranslateLogonNameToSID(
  logonname
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*logonname* 
</dt> <dd>

Type : **chaîne**

Valeur de chaîne qui spécifie le nom d’ouverture de session de l’utilisateur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’ID de sécurité (SID) de l’utilisateur au format chaîne correspondant au nom d’ouverture de session fourni. La chaîne retournée comprend les accolades fermantes standard. Par exemple :

« {S-1-5-21-2127521184-1604012920-1887927527-19009} »

## <a name="remarks"></a>Remarques

La chaîne SID retournée peut être transmise à la méthode [**FindUser**](diskquotacontrol-finduser.md) à la place d’un nom d’ouverture de session.

Lorsqu’un appel à la méthode [**FindUser**](diskquotacontrol-finduser.md)( *logonname*) échoue, cela peut être dû à une incompatibilité entre le formulaire (par exemple, le gestionnaire de compte de sécurité \[ sam \] compatible et le nom d’utilisateur principal \[ UPN \] ) du nom d’ouverture de session fourni et le formulaire stocké dans le cache sid-Name. Dans ce cas, le nom d’ouverture de session peut être converti en SID et l’appel à **FindUser** est répété. **FindUser** reconnaît une chaîne sid et contourne la recherche de cache de nom sid. le code Microsoft Visual Basic scripting Edition (VBScript) suivant illustre cette technique.


```
Function Find(dqc, name)
    On Error Resume Next
    SET Find = dqc.FindUser(name)

    If Err.Number <> 0 Then
        Err.Clear
        SET Find = dqc.FindUser(dqc.TranslateLogonNameToSID(name))
    End If    

End Function
```



La traduction de nom à SID peut être un processus lent par rapport aux recherches dans le cache SID-Name. Par conséquent, il est recommandé d’appeler d’abord [**FindUser**](diskquotacontrol-finduser.md) avec un nom d’ouverture de session. L’exemple ci-dessus utilise cette technique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




