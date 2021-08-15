---
description: Obtient des informations sur la version du système d’exploitation.
ms.assetid: 1af2c320-6e0b-4692-858b-a2c921ed7ce7
title: _GetVersionEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetVersionEx
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 2e3047edfaf2dabe591172dd3ca292f41aeefa90774231b417f5405e3aeb18c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956288"
---
# <a name="_getversionex-function"></a>\_Fonction GetVersionEx

\[Cette fonction est un wrapper sur la fonction **GetVersionEx** . Cette fonction peut être modifiée ou non disponible à l’avenir. Les applications doivent appeler **GetVersionEx** directement.\]

Obtient des informations sur la version du système d’exploitation. Consultez [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa).

## <a name="syntax"></a>Syntaxe


```C++
BOOL _GetVersionEx(
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

[**Tourne**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)
</dt> </dl>

 

 
