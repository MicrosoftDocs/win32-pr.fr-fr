---
description: Inscrit une classe de fenêtre qui permet d’utiliser le contrôle commun SysLink dans une fenêtre.
ms.assetid: 1e6dd741-81be-40bb-a8b5-d565f593c4e9
title: LinkWindow_RegisterClass fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LinkWindow_RegisterClass
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 7b5bfd2e1a45ff3f65df7cf3d3cae41bf4926aaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973383"
---
# <a name="linkwindow_registerclass-function"></a>LinkWindow \_ registerClass, fonction

\[Cette fonction est disponible via Windows XP avec Service Pack 2 (SP2) et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows. Utilisez [**InitCommonControlsEx**](/windows/win32/api/commctrl/nf-commctrl-initcommoncontrolsex) à la place.\]

Inscrit une classe de fenêtre qui permet d’utiliser le contrôle commun [Syslink](../controls/syslink-overview.md) dans une fenêtre.

## <a name="syntax"></a>Syntaxe


```C++
BOOL LinkWindow_RegisterClass(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Type : **bool**

Retourne la **valeur true** si l’inscription a réussi ; **False** dans le cas contraire.

## <a name="remarks"></a>Notes

Cette fonction n’a pas de fichier d’en-tête ou de bibliothèque associé et doit donc être appelée par valeur ordinale. Appelez [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) avec le nom de la dll Shell32.dll pour obtenir un handle de module. Appelez ensuite [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) avec ce handle de module et le numéro ordinal 258 pour utiliser cette fonction.

Utilisez [**LinkWindow \_ UnregisterClass**](linkwindow-unregisterclass.md) pour annuler l’inscription de la classe après utilisation.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble des contrôles SysLink](../controls/syslink-overview.md)
</dt> </dl>

 

 
