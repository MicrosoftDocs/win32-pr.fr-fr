---
description: Récupère le TAGID et un descripteur de la base de données de shims pour le TAGREF spécifié.
ms.assetid: 869c6af5-4c10-4358-9d6a-1a354be6f4e9
title: SdbTagRefToTagID fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbTagRefToTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: feeb622fd196ed20efb60d866d59b634fdcd9ecd955a97a1d7af0aef1347c8f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815318"
---
# <a name="sdbtagreftotagid-function"></a>SdbTagRefToTagID fonction)

Récupère le **TagId** et un descripteur de la base de données de shims pour le [**TAGREF**](tagref.md)spécifié.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI SdbTagRefToTagID(
  _In_  HSDB   hSDB,
  _In_  TAGREF trWhich,
  _Out_ PDB    *ppdb,
  _Out_ TAGID  *ptiWhich
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSDB* \[ dans\]
</dt> <dd>

Handle de la base de données de shims retournée par la fonction [**SdbInitDatabase**](sdbinitdatabase.md) .

</dd> <dt>

*trWhich* \[ dans\]
</dt> <dd>

[**TAGREF**](tagref.md).

</dd> <dt>

*PPDB* \[ à\]
</dt> <dd>

Handle résultant de la base de données de shims.

</dd> <dt>

*ptiWhich* \[ à\]
</dt> <dd>

**TagId** résultant.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbInitDatabase**](sdbinitdatabase.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> <dt>

[**TAGREF**](tagref.md)
</dt> </dl>

 

 




