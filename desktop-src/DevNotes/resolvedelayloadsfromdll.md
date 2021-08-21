---
description: Transfère le travail en résolvant les importations à chargement différé à partir du fichier binaire parent vers un fichier binaire cible.
ms.assetid: 65629d7b-36b0-426b-a20d-ec736b8461dc
title: ResolveDelayLoadsFromDll fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResolveDelayLoadsFromDll
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
ms.openlocfilehash: 894360a20456b73d0cfad19cd125405caf0c3624821aca21e3e107699d1cc372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571539"
---
# <a name="resolvedelayloadsfromdll-function"></a>ResolveDelayLoadsFromDll fonction)

Transfère le travail en résolvant les importations à chargement différé à partir du fichier binaire parent vers un fichier binaire cible.

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS WINAPI ResolveDelayLoadsFromDll(
  _In_       PVOID  ParentBase,
  _In_       LPCSTR TargetDllName,
  _Reserved_ ULONG  Flags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ParentBase* \[ dans\]
</dt> <dd>

Adresse de base du module qui retarde le chargement d’un autre binaire.

</dd> <dt>

*TargetDllName* \[ dans\]
</dt> <dd>

Nom de la DLL cible.

</dd> <dt>

*Indicateurs* 
</dt> <dd>

Réservé doit être égal à 0.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Adresse du descripteur de chargement différé, s’il est trouvé ; Sinon, **null**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Bibliothèque<br/> | <dl> <dt>Kernel32.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Prise en charge de l’éditeur de liens pour les dll Delay-Loaded](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)
</dt> </dl>

 

 




