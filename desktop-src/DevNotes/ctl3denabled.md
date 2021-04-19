---
description: Vérifie si les contrôles peuvent utiliser des effets 3D.
ms.assetid: fb7b892f-2580-41ac-b2ef-938da3cc1dc2
title: Ctl3dEnabled fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dEnabled
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: d0eecec5650ecc00b69c0745e58a3e1d0f931a00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525604"
---
# <a name="ctl3denabled-function"></a>Ctl3dEnabled fonction)

Vérifie si les contrôles peuvent utiliser des effets 3D.

## <a name="syntax"></a>Syntaxe


```C++
BOOL Ctl3dEnabled(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si les contrôles peuvent utiliser des effets 3D. Sinon, elle retourne **false**.

## <a name="remarks"></a>Notes

Dans Windows 4,0 ou version ultérieure, **Ctl3dEnabled** et [**Ctl3dRegister**](ctl3dregister.md) retournent **false**.

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
