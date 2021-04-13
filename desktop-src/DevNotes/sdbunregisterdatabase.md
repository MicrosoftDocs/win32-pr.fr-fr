---
description: Annule l’inscription de la base de données spécifiée, ce qui la rend n’est plus disponible.
ms.assetid: 7e6c50f4-85f6-4b33-b639-d8fda143e5e7
title: SdbUnregisterDatabase fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbUnregisterDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 72171e1f9ae20ac2213a285046b2499093be4313
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483120"
---
# <a name="sdbunregisterdatabase-function"></a>SdbUnregisterDatabase fonction)

Annule l’inscription de la base de données spécifiée, ce qui la rend n’est plus disponible.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI SdbUnregisterDatabase(
  _In_ GUID *pguidDB
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pguidDB* \[ dans\]
</dt> <dd>

GUID de la base de données. Ce paramètre ne peut pas être **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbRegisterDatabaseEx**](sdbregisterdatabaseex.md)
</dt> </dl>

 

 




