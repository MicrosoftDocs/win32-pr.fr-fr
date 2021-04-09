---
description: Vide le cache de compatibilité des applications.
ms.assetid: 03f47813-87f6-4b71-b453-77a2facab019
title: BaseFlushAppcompatCache fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BaseFlushAppcompatCache
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-appcompat-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-appcompat-l1-1-1.dll
ms.openlocfilehash: 6118c78784bb96b9f25e008cd2221112eeb646f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110310"
---
# <a name="baseflushappcompatcache-function"></a>BaseFlushAppcompatCache fonction)

Vide le cache de compatibilité des applications.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI BaseFlushAppcompatCache(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

La fonction retourne **true** si elle est réussie et **false** dans le cas contraire.

## <a name="remarks"></a>Notes

L’appelant doit être un administrateur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ShimFlushCache**](shimflushcache.md)
</dt> </dl>

 

 




