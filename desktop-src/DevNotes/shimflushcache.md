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
ms.openlocfilehash: 35e279c5036142ec87c5bad6d7c512388033bc94
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033574"
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

## <a name="remarks"></a>Notes

L’appelant doit être un administrateur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BaseFlushAppcompatCache**](baseflushappcompatcache.md)
</dt> </dl>

 

 




