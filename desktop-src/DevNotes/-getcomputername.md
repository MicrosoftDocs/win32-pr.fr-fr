---
description: Obtient le nom de l'ordinateur.
ms.assetid: 8b6fd61a-dd5a-46b8-920e-cc8a848732b6
title: _GetComputerName fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetComputerName
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: f3049a51b59562a1f5b512f7cb6cace6eff995644d1524680ff0d3ec176efed7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103849"
---
# <a name="_getcomputername-function"></a>\_GetComputerName (fonction)

\[Cette fonction est un wrapper sur la fonction **GetComputerName** . Cette fonction peut être modifiée ou non disponible à l’avenir. Les applications doivent appeler **GetComputerName** directement.\]

Obtient le nom de l'ordinateur. Consultez [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea).

## <a name="syntax"></a>Syntaxe


```C++
BOOL _GetComputerName(
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

[**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea)
</dt> </dl>

 

 
