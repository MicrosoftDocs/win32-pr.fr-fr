---
description: Annule l’inscription d’une classe de fenêtre inscrite par LinkWindow \_ registerClass.
ms.assetid: 9e5c4326-efd1-43ca-a087-a436fe3f9bbd
title: LinkWindow_UnregisterClass fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LinkWindow_UnregisterClass
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 05a50d5f3af72c31ee04a1a9e8264acb22327c38f79f765ce2ad7a740086747e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968938"
---
# <a name="linkwindow_unregisterclass-function"></a>LinkWindow \_ fonction UnregisterClass

\[cette fonction est disponible par le biais de Windows XP avec Service Pack 2 (SP2) et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

Annule l’inscription d’une classe de fenêtre inscrite par [**LinkWindow \_ registerClass**](linkwindow-registerclass.md).

## <a name="syntax"></a>Syntaxe


```C++
BOOL LinkWindow_UnregisterClass(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Type : **bool**

Retourne la **valeur true** si l’opération a réussi ; **False** dans le cas contraire.

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de fichier d’en-tête ou de bibliothèque associé et doit donc être appelée par valeur ordinale. Appelez [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) avec le nom de la dll Shell32.dll pour obtenir un handle de module. Appelez ensuite [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) avec ce handle de module et le numéro ordinal 259 pour utiliser cette fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble des contrôles SysLink](../controls/syslink-overview.md)
</dt> </dl>

 

 
