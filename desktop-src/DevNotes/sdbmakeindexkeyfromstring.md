---
description: Crée une clé à partir d’une chaîne.
ms.assetid: 107138b9-96f0-4144-a4bc-7115b6deab60
title: SdbMakeIndexKeyFromString fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbMakeIndexKeyFromString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 3298b0e038218aecb9676c596e7dbad09acbbdd4441d0f1cd79c3ec2a0188720
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161222"
---
# <a name="sdbmakeindexkeyfromstring-function"></a>SdbMakeIndexKeyFromString fonction)

Crée une clé à partir d’une chaîne.

## <a name="syntax"></a>Syntaxe


```C++
ULONGLONG WINAPI SdbMakeIndexKeyFromString(
  _In_ LPCTSTR pwszKey
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pwszKey* \[ dans\]
</dt> <dd>

Chaîne.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne la clé ou 0 en cas d’erreur.

## <a name="remarks"></a>Remarques

La clé d’index standard est les huit premiers caractères de la chaîne, convertis en majuscules, puis castés en valeur **ULONGLONG** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




