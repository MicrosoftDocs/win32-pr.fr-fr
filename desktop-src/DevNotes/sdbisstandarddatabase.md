---
description: Détermine si la base de données spécifiée est l’une des bases de données standard (SysMain, AppHelp, Drvmain ou Msimain).
ms.assetid: 7d7e3ca7-535e-40b3-b635-299eff8abea5
title: SdbIsStandardDatabase fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbIsStandardDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 9e9e445162c2bfc171ccf975981876f81a8bb804
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033577"
---
# <a name="sdbisstandarddatabase-function"></a>SdbIsStandardDatabase fonction)

Détermine si la base de données spécifiée est l’une des bases de données standard (SysMain, AppHelp, Drvmain ou Msimain).

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI SdbIsStandardDatabase(
  _In_ GUID GuidDB
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*GuidDB* \[ dans\]
</dt> <dd>

GUID de la base de données.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne **true** si le GUID représente une base de données standard ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




