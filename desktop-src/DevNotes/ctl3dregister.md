---
description: Inscrit une application en tant que client de CTL3D.
ms.assetid: 38a4a04a-6322-4eb8-b272-ae9b90f84e0f
title: Ctl3dRegister fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dRegister
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 9f58236891b8a673102905e0ef0c108ac9da6e6192788abea9c6e79baf8acfcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162157"
---
# <a name="ctl3dregister-function"></a>Ctl3dRegister fonction)

Inscrit une application en tant que client de CTL3D.

## <a name="syntax"></a>Syntaxe


```C++
BOOL Ctl3dRegister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hinstApp* 
</dt> <dd>

Handle de l’application à inscrire en tant que client.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si les effets 3D sont actifs ; Sinon, elle retourne **false**.

## <a name="remarks"></a>Remarques

Une application qui utilise CTL3D doit appeler cette fonction dans WinMain.

les effets 3D ne sont pas disponibles sur les systèmes qui ont une résolution inférieure à VGA.

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
