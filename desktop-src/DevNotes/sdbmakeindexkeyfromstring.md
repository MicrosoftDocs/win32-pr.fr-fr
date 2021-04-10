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
ms.openlocfilehash: 691e691f14692775f0c681a7efa3ce91f756be1d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950367"
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

## <a name="remarks"></a>Notes

La clé d’index standard est les huit premiers caractères de la chaîne, convertis en majuscules, puis castés en valeur **ULONGLONG** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




