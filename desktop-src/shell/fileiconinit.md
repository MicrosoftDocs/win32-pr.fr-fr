---
description: Initialise ou réinitialise la liste d’images système.
ms.assetid: 4e661326-157e-4c75-86df-cd213e01c3e5
title: FileIconInit fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIconInit
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 1771e1f0bde83f0fc7d070787b7a19f87007e26bd1ad42dcaa88e230e61a60af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111809"
---
# <a name="fileiconinit-function"></a>FileIconInit fonction)

Initialise ou réinitialise la liste d’images système.

## <a name="syntax"></a>Syntaxe


```C++
BOOL FileIconInit(
  _In_ BOOL fRestoreCache
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fRestoreCache* \[ dans\]
</dt> <dd>

Type : **bool**

**True** pour restaurer le cache de l’image système à partir du disque ; **False** dans le cas contraire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **bool**

**True** si le cache a été actualisé avec succès, **false** en cas d’échec de l’initialisation.

## <a name="remarks"></a>Remarques

Si vous utilisez des listes d’images système dans votre propre processus, vous devez appeler **FileIconInit** aux moments suivants :

-   Au lancement.
-   En réponse à un message [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) lorsque l’indicateur [**SPI \_ SETNONCLIENTMETRICS**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) est défini.

**FileIconInit** n’est pas inclus dans un fichier d’en-tête. Vous devez l’appeler directement à partir de Shell32.dll, en utilisant l’ordinal 660.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
