---
description: Utilisé pour déterminer s’il faut afficher l’option partager ce dossier dans l’affichage Web.
title: CanShareFolderW, fonction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CanShareFolderW
- CanShareFolderW
api_type:
- DllExport
api_location:
- Ntshrui.dll
ms.assetid: 5fd28a14-53e7-4016-9c49-9bb14ce7808b
ms.openlocfilehash: 7013c6ae825c34ae7d2dd7b9d507eac1e52c8d4e3a27182e5297e72ef13b4d9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032867"
---
# <a name="cansharefolderw-function"></a>CanShareFolderW, fonction

\[cette fonction est disponible par le biais de Windows XP avec Service Pack 2 (SP2) et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

Utilisé pour déterminer s’il faut afficher l’option **partager ce dossier** dans l’affichage Web.

## <a name="syntax"></a>Syntaxe


```C++
STDAPI CanShareFolderW(
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszPath* \[ dans\]
</dt> <dd>

Type : **LPCWSTR**

Pointeur vers une chaîne qui spécifie le chemin d’accès du dossier à tester.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **STDAPI**

Les valeurs de retour sont les suivantes.



| Code/valeur de retour                                                                        | Description                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>     | Le chemin d’accès pointé par *pszPath* spécifie un dossier qui peut être partagé.<br/>    |
| <dl> <dt>**S \_ false**</dt> </dl>  | Le chemin d’accès pointé par *pszPath* spécifie un dossier qui ne peut pas être partagé.<br/> |
| <dl> <dt>Erreur HRESULT</dt> </dl> | Une erreur s’est produite.<br/>                                                     |



 

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de fichier. lib associé. Vous devez utiliser [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour l’utiliser.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Ntshrui.dll</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **CanShareFolderW** (Unicode)<br/>                                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ShowShareFolderUI**](./showsharefolderui.md)
</dt> </dl>

 

 
