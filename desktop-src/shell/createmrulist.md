---
description: Crée une nouvelle liste des derniers fichiers utilisés (MRU).
title: CreateMRUListW, fonction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateMRUListW
- CreateMRUListW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: b2d9e3c7-8151-45ef-9658-bd33a87b4c9c
ms.openlocfilehash: 34cd3dd9e5b9e62bbdd13b31d95e7205e4427de6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412563"
---
# <a name="createmrulistw-function"></a>CreateMRUListW, fonction

Crée une nouvelle liste des derniers fichiers utilisés (MRU).

## <a name="syntax"></a>Syntaxe


```C++
int CreateMRUListW(
  _In_ LPMRUINFO lpmi
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpmi* \[ dans\]
</dt> <dd>

Type : **LPMRUINFO**

Pointeur vers une structure [**MRUINFO**](mruinfo.md) définissant la liste MRU.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **int**

Retourne un handle vers la nouvelle liste MRU, ou 0 en cas d’erreur.

## <a name="remarks"></a>Notes

Cette fonction n’est pas incluse dans un en-tête public ou une bibliothèque. Il est accessible par le biais de [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) ou extrait de comctl32.dll par son ordinal, qui est 400 pour **CreateMRUListW**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                     |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (version 5,0 ou ultérieure)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **CreateMRUListW** (Unicode)<br/>                                                                        |



 

 
