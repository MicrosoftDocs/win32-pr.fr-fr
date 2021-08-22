---
description: Ouvre la base de données de détails AppHelp spécifiée.
ms.assetid: c3b07c00-a3c6-419c-94c6-34c573a04d6d
title: SdbOpenApphelpDetailsDatabase fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenApphelpDetailsDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: d6bd0bc7cbd1404c3bcf5459254f53e62a777d0936b89a0f7a282dd8d0094227
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045159"
---
# <a name="sdbopenapphelpdetailsdatabase-function"></a>SdbOpenApphelpDetailsDatabase fonction)

Ouvre la base de données de détails AppHelp spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
PDB WINAPI SdbOpenApphelpDetailsDatabase(
  _In_opt_ LPCWSTR pwsDetailsDatabasePath
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pwsDetailsDatabasePath* \[ dans, facultatif\]
</dt> <dd>

Chemin d’accès de la base de données. Si ce paramètre a la **valeur null**, la base de données système locale est ouverte.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne un descripteur à la base de données de détails AppHelp.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




