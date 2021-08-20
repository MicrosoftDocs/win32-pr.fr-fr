---
description: Supprime un utilisateur du volume.
ms.assetid: 56a07388-b7d8-41a4-b29a-8a57fe0b9d19
title: DiskQuotaControl. DeleteUser, méthode (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DeleteUser
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5220e7290f1487da336e22a744aed599df94baac4040877d4ce7713786668e4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118050662"
---
# <a name="diskquotacontroldeleteuser-method"></a>DiskQuotaControl. DeleteUser, méthode

Supprime un utilisateur du volume.

## <a name="syntax"></a>Syntaxe


```JScript
DiskQuotaControl.DeleteUser(
  oUser
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*oUser* 
</dt> <dd>

Type : **Object**

Expression d’objet qui prend la valeur de l’objet [**DIDiskQuotaUser**](didiskquotauser-object.md) de l’utilisateur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode échoue si l’utilisateur possède un stockage sur le volume. Avant de supprimer un utilisateur d’un volume, tout le stockage de cet utilisateur doit être supprimé, déplacé vers un autre volume ou une propriété est transférée à un autre utilisateur.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Dskquota. h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**AddUser**](diskquotacontrol-adduser.md)
</dt> <dt>

[**DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




