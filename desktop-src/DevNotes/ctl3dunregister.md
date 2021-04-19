---
description: Annule l’inscription d’une application en tant que client de CTL3D.
ms.assetid: 21990A79-F90D-4AE1-AB02-2B33583B47F5
title: Ctl3dUnregister fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnregister
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 85cd45062da9c01ef8af5a312a855bfaab6a6bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531075"
---
# <a name="ctl3dunregister-function"></a>Ctl3dUnregister fonction)

Annule l’inscription d’une application en tant que client de CTL3D.

## <a name="syntax"></a>Syntaxe


```C++
BOOL Ctl3dUnregister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hinstApp* 
</dt> <dd>

Handle vers l’application dont l’inscription doit être annulée en tant que client.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si l’inscription de l’application en tant que client de CTL3D est annulée. Sinon, elle retourne **false**.

## <a name="remarks"></a>Notes

Une application qui utilise CTL3D doit appeler cette fonction dans WinMain.

les effets 3D ne sont pas disponibles sur les systèmes qui ont une résolution inférieure à VGA.

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
