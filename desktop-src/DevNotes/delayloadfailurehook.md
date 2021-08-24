---
description: Retourne l’adresse d’une fonction de rappel d’échec de chargement différé pour la DLL et le processus spécifiés.
ms.assetid: db1d34cb-800a-4984-b4a3-d1ce1c6ee86c
title: DelayLoadFailureHook fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DelayLoadFailureHook
api_type:
- DllExport
api_location:
- kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-0.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
ms.openlocfilehash: 8724073a8f5f124cf23d6ba15390c8028d308354aa1e2c896f1d2c9f5030ea45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795280"
---
# <a name="delayloadfailurehook-function"></a>DelayLoadFailureHook fonction)

Retourne l’adresse d’une fonction de rappel d’échec de chargement différé pour la DLL et le processus spécifiés.

## <a name="syntax"></a>Syntaxe


```C++
FARPROC WINAPI DelayLoadFailureHook(
  _In_ LPCSTR pszDllName,
  _In_ LPCSTR pszProcName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszDllName* \[ dans\]
</dt> <dd>

Nom de la DLL.

</dd> <dt>

*pszProcName* \[ dans\]
</dt> <dd>

Nom du processus.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Adresse de la fonction de rappel.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Bibliothèque<br/> | <dl> <dt>Kernel32.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Raccordements de défaillance](https://msdn.microsoft.com/library/sfcfb0a3(v=VS.71).aspx)
</dt> </dl>

 

 




