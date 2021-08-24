---
description: détermine si le Terminal Server est en mode d’installation (uniquement sur Terminal Windows Server 4,0).
ms.assetid: f6cb7971-d4f5-49ca-938a-9c280028764a
title: CtxGetIniMapping fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CtxGetIniMapping
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 7085e595b1f9c1fb8ea36e59aae4a90c816b508c92bcd33a99fe5051f2b722d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654209"
---
# <a name="ctxgetinimapping-function"></a>CtxGetIniMapping fonction)

\[Cette fonction n’est pas prise en charge et ne doit pas être utilisée. Elle peut changer ou disparaître complètement sans préavis. Utilisez plutôt **VerifyVersionInfo**.\]

détermine si le Terminal Server est en mode d’installation (uniquement sur Terminal Windows Server 4,0).

## <a name="syntax"></a>Syntaxe


```C++
BOOLEAN CtxGetIniMapping(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne **false** si le Terminal Server est en mode d’installation, **true** s’il est en mode exécution.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)
</dt> </dl>

 

 
