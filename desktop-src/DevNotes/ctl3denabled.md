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
ms.openlocfilehash: 0d8a234736631517a0e77f5ab23f07688e3d80aa4c8b74a3b2ee51351beece90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654589"
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

## <a name="remarks"></a>Remarques

dans Windows 4,0 ou version ultérieure, **Ctl3dEnabled** et [**Ctl3dRegister**](ctl3dregister.md) retournent **false**.

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
