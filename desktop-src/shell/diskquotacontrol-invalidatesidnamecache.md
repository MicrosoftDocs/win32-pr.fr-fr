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
ms.openlocfilehash: 1a171aaaf8f3faa45f967f29bf0f9d742aa0fe0221b46ae4ba4f8527d9cf9715
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455889"
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

## <a name="remarks"></a>Remarques

Les noms d’utilisateur et les ID de sécurité associés sont stockés dans un cache. Vous pouvez effacer ce cache en appelant **InvalidateSidNameCache**. Si, par la suite, vous créez un nouvel objet utilisateur, les informations doivent être obtenues à partir du contrôleur de domaine, et le cache doit être rétabli.

## <a name="requirements"></a>Configuration requise



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

 

 




