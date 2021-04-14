---
description: Ferme la base de données de shims initialisée à l’aide de la fonction SdbInitDatabase.
ms.assetid: 8452ab14-a1e9-41b3-a1ac-7ff3a7d3a7ed
title: SdbReleaseDatabase fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReleaseDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7df4b62af6b2fe654269a8bea4b2e866d0d765b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523335"
---
# <a name="sdbreleasedatabase-function"></a>SdbReleaseDatabase fonction)

Ferme la base de données de shims initialisée à l’aide de la fonction [**SdbInitDatabase**](sdbinitdatabase.md) .

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI SdbReleaseDatabase(
  _In_ HSDB hSDB
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSDB* \[ dans\]
</dt> <dd>

Handle de la base de données de shims retournée par la fonction [**SdbInitDatabase**](sdbinitdatabase.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbInitDatabase**](sdbinitdatabase.md)
</dt> </dl>

 

 




