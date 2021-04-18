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
ms.openlocfilehash: 4b855c162d9d5f1c43a15d1ebd7219da6f847f37
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528961"
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

## <a name="remarks"></a>Notes

Une application qui utilise CTL3D doit appeler cette fonction dans WinMain.

les effets 3D ne sont pas disponibles sur les systèmes qui ont une résolution inférieure à VGA.

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
