---
description: Sous-classe et ajoute automatiquement des effets 3D à toutes les boîtes de dialogue de l’application.
ms.assetid: 96555052-c564-4cc7-9b24-e527f8e2f879
title: Ctl3dAutoSubclass fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dAutoSubclass
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 85f4c85d1d608ff97147a935806b090162f5a78a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525612"
---
# <a name="ctl3dautosubclass-function"></a>Ctl3dAutoSubclass fonction)

Sous-classe et ajoute automatiquement des effets 3D à toutes les boîtes de dialogue de l’application.

## <a name="syntax"></a>Syntaxe


```C++
PUBLIC BOOL FAR PASCAL Ctl3dAutoSubclass(
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

Retourne la **valeur true** , sauf si l’une des conditions suivantes existe, auquel cas elle retourne **false**:

-   CTL3D s’exécute sous Windows version 3,0 ou antérieure.
-   CTL3D n’a pas d’espace disponible dans ses tables pour l’application actuelle. CTL3D peut traiter jusqu’à 32 applications en même temps.
-   CTL3D ne peut pas installer son Hook CBT.

## <a name="remarks"></a>Notes

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
