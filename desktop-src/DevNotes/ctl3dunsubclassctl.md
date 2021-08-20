---
description: Désactive le sous-classement pour le contrôle spécifié.
ms.assetid: d4d34624-7d85-4c53-8318-b3e5d6f95f7a
title: Ctl3dUnsubclassCtl fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnsubclassCtl
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: db0f87b7aec956a74a0c54871da4019c1ddd4f1bcd57fce3806218003fcb70bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162120"
---
# <a name="ctl3dunsubclassctl-function"></a>Ctl3dUnsubclassCtl fonction)

Désactive le sous-classement pour le contrôle spécifié.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI Ctl3dUnsubclassCtl(
   HWND hwnd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* 
</dt> <dd>

Handle de la fenêtre de contrôle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si le contrôle est sous-classé avec succès ; Sinon, elle retourne **false**.

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Ctl3dSubclassCtl**](ctl3dsubclassctl.md)
</dt> </dl>

 

 
