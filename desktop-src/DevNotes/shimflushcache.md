---
description: Vide le cache de base de données de shims. Cette fonction doit être appelée après l’installation d’une nouvelle base de données de shims.
ms.assetid: 7e5bbdca-7b58-4c51-9cd1-105b05ee7fbe
title: ShimFlushCache fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShimFlushCache
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: ecf1291b7fdcfb43170ec7e269fa140c321fafdbc09989fc7ee2b392f11c1160
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075913"
---
# <a name="shimflushcache-function"></a>ShimFlushCache fonction)

Vide le cache de base de données de shims. Cette fonction doit être appelée après l’installation d’une nouvelle base de données de shims.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI ShimFlushCache(
  _In_opt_ HWND      hwnd,
  _In_opt_ HINSTANCE hInstance,
  _In_opt_ LPCSTR    lpszCmdLine,
  _In_     int       nCmdShow
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* \[ dans, facultatif\]
</dt> <dd>

Inutilisé doit être égal à 0.

</dd> <dt>

*HINSTANCE* \[ dans, facultatif\]
</dt> <dd>

Inutilisé doit être égal à 0.

</dd> <dt>

*lpszCmdLine* \[ dans, facultatif\]
</dt> <dd>

Inutilisé doit être égal à 0.

</dd> <dt>

*nCmdShow* \[ dans\]
</dt> <dd>

Inutilisé doit être égal à 0.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.

## <a name="remarks"></a>Remarques

L’appelant doit être un administrateur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BaseFlushAppcompatCache**](baseflushappcompatcache.md)
</dt> </dl>

 

 




