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
ms.openlocfilehash: 5edc8bafb00d5444f18b61e0600fb075b6a7367c315c2ab1cfe38f911e9a84d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654609"
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

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
