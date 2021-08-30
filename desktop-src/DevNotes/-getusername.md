---
description: Obtient le nom de l'utilisateur.
ms.assetid: 1373fc9d-ab1c-49b9-8b82-de2e99c4821c
title: _GetUserName fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetUserName
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 67ebcf5cb775a71475ebb0cb7366e8b57a261dff45646ad1259ad71e44321f93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053159"
---
# <a name="_getusername-function"></a>\_GetUserName, fonction

\[Cette fonction est un wrapper sur la fonction **getUserName** . Cette fonction peut être modifiée ou non disponible à l’avenir. Les applications doivent appeler **getUserName** directement.\]

Obtient le nom de l'utilisateur. Consultez [**getUserName**](/windows/win32/api/winbase/nf-winbase-getusernamea).

## <a name="syntax"></a>Syntaxe


```C++
BOOL _GetUserName(
    ...
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msmdun80.dll ; </dt> <dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetUserName**](/windows/win32/api/winbase/nf-winbase-getusernamea)
</dt> </dl>

 

 
