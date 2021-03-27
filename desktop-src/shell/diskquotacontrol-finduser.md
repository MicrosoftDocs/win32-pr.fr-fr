---
description: Recherche l’entrée d’un utilisateur, par son nom, dans le fichier de quota du volume.
title: Méthode DiskQuotaControl. FindUser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.FindUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e5767d28-4c0a-49bc-a1d3-ba809411456d
ms.openlocfilehash: af1bc9c0398d37f04e47515a2b85cb4520795b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971966"
---
# <a name="diskquotacontrolfinduser-method"></a>Méthode DiskQuotaControl. FindUser

Recherche l’entrée d’un utilisateur, par son nom, dans le fichier de quota du volume.

## <a name="syntax"></a>Syntaxe


```JScript
DiskQuotaControl.FindUser(
  sLogonName
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sLogonName* 
</dt> <dd>

Type : **chaîne**

Valeur de chaîne qui contient le nom d’ouverture de session de l’utilisateur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une expression d’objet qui prend la valeur de l’objet [**DIDiskQuotaUser**](didiskquotauser-object.md) de l’utilisateur.

## <a name="remarks"></a>Notes

Cette méthode retourne un objet [**DIDiskQuotaUser**](didiskquotauser-object.md) même s’il n’y a aucune entrée pour l’utilisateur dans le fichier de quota. Le seuil d’avertissement et les limites de quota matériel sont définis pour l’objet utilisateur retourné sur les valeurs par défaut du volume.

La chaîne retournée par [**TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md) peut être passée à la place du paramètre *sLogonName* . Quand **FindUser** reçoit une chaîne sid, il utilise le SID correspondant pour la recherche directe de l’enregistrement de quota de l’utilisateur sur le volume. Cela contourne le cache de noms SID. Dans les cas où **FindUser** échoue en raison d’une incompatibilité de format (par exemple, compatible Sam et UPN) du nom d’ouverture de session fourni et du nom d’ouverture de session mis en cache, le nom d’ouverture de session peut être traduit en une chaîne sid à l’aide de **TranslateLogonNameToSID** , puis retransmis à **FindUser**. Le code VBScript suivant illustre cette technique.


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



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




