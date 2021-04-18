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
ms.openlocfilehash: f61be4596c5076dd7763ed171124888382f3ef6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532780"
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

 

 
