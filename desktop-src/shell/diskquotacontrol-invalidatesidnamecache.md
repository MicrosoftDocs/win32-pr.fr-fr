---
description: Invalide le cache du nom d’utilisateur de l’ID de sécurité.
ms.assetid: 52f4a051-0caf-43c1-b190-c83c20e9fcf8
title: Méthode DiskQuotaControl. InvalidateSidNameCache (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.InvalidateSidNameCache
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4e7202c1293d32d55e12e88671ed9960d376f63e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951017"
---
# <a name="diskquotacontrolinvalidatesidnamecache-method"></a>Méthode DiskQuotaControl. InvalidateSidNameCache

Invalide le cache du nom d’utilisateur de l’ID de sécurité.

## <a name="syntax"></a>Syntaxe


```JScript
DiskQuotaControl.InvalidateSidNameCache()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Les noms d’utilisateur et les ID de sécurité associés sont stockés dans un cache. Vous pouvez effacer ce cache en appelant **InvalidateSidNameCache**. Si, par la suite, vous créez un nouvel objet utilisateur, les informations doivent être obtenues à partir du contrôleur de domaine, et le cache doit être rétabli.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Dskquota. h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




