---
description: Affiche l’onglet partage de dossiers de la feuille de propriétés du dossier spécifié.
ms.assetid: e622e4bb-eaf7-494f-b2a2-78ba1311a496
title: ShowShareFolderUI fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShowShareFolderUI
- ShowShareFolderUIW
api_type:
- DllExport
api_location:
- Ntshrui.dll
ms.openlocfilehash: 9683d7faee4bd44bd8f21e14250503f351e1a134119f978f872d7a0fe3ad6c4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968258"
---
# <a name="showsharefolderui-function"></a>ShowShareFolderUI fonction)

Affiche l’onglet **partage de dossiers** de la feuille de propriétés du dossier spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ShowShareFolderUI(
  _In_ HWND    hwndParent,
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hwndParent* \[ dans\]
</dt> <dd>

Type : **HWND**

Handle de la fenêtre parente pour la feuille de propriétés.

</dd> <dt>

*pszPath* \[ dans\]
</dt> <dd>

Type : **LPCWSTR**

Pointeur vers une chaîne qui spécifie le chemin d’accès au dossier qui affiche son onglet **partage de dossiers** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Cette fonction retourne toujours S \_ OK.

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de fichier. lib associé. Vous devez utiliser [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour l’utiliser.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Ntshrui.dll</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **ShowShareFolderUIW** (Unicode)<br/>                                            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CanShareFolderW**](cansharefolderw.md)
</dt> </dl>

 

 
