---
description: Utilisé pour déterminer s’il faut afficher l’option partager ce dossier dans l’affichage Web.
title: CanShareFolderW fonction)
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
ms.openlocfilehash: cf7d0feb31666f3a918c0307a0b0983bff246fea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525402"
---
# <a name="cansharefolderw-function"></a>CanShareFolderW fonction)

\[Cette fonction est disponible via Windows XP avec Service Pack 2 (SP2) et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

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



 

## <a name="remarks"></a>Notes

Cette fonction n’a pas de fichier. lib associé. Vous devez utiliser [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour l’utiliser.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Ntshrui.dll</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **CanShareFolderW** (Unicode)<br/>                                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ShowShareFolderUI**](./showsharefolderui.md)
</dt> </dl>

 

 
