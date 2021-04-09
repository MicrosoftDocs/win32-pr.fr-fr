---
description: Ferme la base de données de shims spécifiée.
ms.assetid: e4480860-8055-4134-b6ed-926c010d462f
title: SdbCloseDatabase fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCloseDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 376d97b8386f127a945cb118639be1e38ae68737
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033673"
---
# <a name="sdbclosedatabase-function"></a>SdbCloseDatabase fonction)

Ferme la base de données de shims spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI SdbCloseDatabase(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

fichier *PDB* \[ in, out\]
</dt> <dd>

Handle de la base de données de shims. Ce paramètre ne peut pas être **null**.

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

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




