---
description: La fonction ThunkConnect32 est utilisée par les pilotes de périphériques 16 bits (pour MS-DOS) qui appellent le noyau 32 bits.
ms.assetid: 3376ca67-04ea-4765-a2f4-15a84d5c84d4
title: ThunkConnect32 fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ThunkConnect32
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 7f22d7ceb59732e986c23c873133b11f358364cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542448"
---
# <a name="thunkconnect32-function"></a>ThunkConnect32 fonction)

\[Cette fonction était prise en charge pour la compatibilité descendante, mais elle n’est pas présente dans les versions actuelles de Windows. Les nouveaux pilotes de périphérique doivent être de 32 ou 64 bits et n’ont pas besoin de cette fonction.\]

La fonction **ThunkConnect32** est utilisée par les pilotes de périphériques 16 bits (pour MS-DOS) qui appellent le noyau 32 bits.

## <a name="syntax"></a>Syntaxe


```C++
BOOL ThunkConnect32(
   LPVOID lpThunkData32,
   LPSTR  pszThunkData16Name,
   LPSTR  pszDll16,
   LPSTR  pszDll32,
   HANDLE hInstance,
   DWORD  dwReason
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpThunkData32* 
</dt> <dd>

Ignoré.

</dd> <dt>

*pszThunkData16Name* 
</dt> <dd>

Ignoré.

</dd> <dt>

*pszDll16* 
</dt> <dd>

Ignoré.

</dd> <dt>

*pszDll32* 
</dt> <dd>

Ignoré.

</dd> <dt>

*hInstance* 
</dt> <dd>

Ignoré.

</dd> <dt>

*dwReason* 
</dt> <dd>

Ignoré.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne toujours **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Kernel32.dll</dt> </dl> |



 

 




