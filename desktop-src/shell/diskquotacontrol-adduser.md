---
description: Affecte un quota de disque autre que celui par défaut à un nouvel utilisateur.
title: DiskQuotaControl. AddUser, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.AddUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: de20d016-83da-42ac-962f-86faf9b25419
ms.openlocfilehash: 9dd69b78210ecda418e784681694d84b27b1732a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530465"
---
# <a name="diskquotacontroladduser-method"></a>DiskQuotaControl. AddUser, méthode

Affecte un quota de disque autre que celui par défaut à un nouvel utilisateur.

## <a name="syntax"></a>Syntaxe


```JScript
objRetVal = DiskQuotaControl.AddUser(
  sLogonName
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sLogonName* 
</dt> <dd>

Type : **char**

Valeur de chaîne qui contient le nom d’ouverture de session de l’utilisateur. Utilisez la propriété [**UserNameResolution**](diskquotacontrol-usernameresolution.md) pour spécifier la façon dont le nom doit être résolu.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **Object**

Retourne une expression d’objet qui prend la valeur de l’objet [**DIDiskQuotaUser**](didiskquotauser-object.md) de l’utilisateur.

## <a name="remarks"></a>Notes

Le système de fichiers NTFS crée automatiquement une entrée de quota utilisateur lorsqu’un utilisateur écrit pour la première fois sur le volume. Les entrées créées de cette façon reçoivent le seuil d’avertissement par défaut et les valeurs de limite de quota matériel pour le volume. Cette méthode vous permet de créer une entrée de quota utilisateur avant qu’un utilisateur n’écrive des informations sur le volume. Elle retourne un objet [**DIDiskQuotaUser**](didiskquotauser-object.md) qui peut être utilisé pour assigner une valeur de seuil d’avertissement ou de limite de quota différente des paramètres par défaut du volume.

Si l’utilisateur existe déjà, aucune nouvelle entrée n’est créée. La méthode retourne l’objet [**DIDiskQuotaUser**](didiskquotauser-object.md) associé à l’entrée existante.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DefaultQuotaLimit**](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[**DefaultQuotaThreshold**](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[**Objet DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




