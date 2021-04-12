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
ms.openlocfilehash: 2810b0bbe1f10f013f39570aecda448a4ceeea6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104109915"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




