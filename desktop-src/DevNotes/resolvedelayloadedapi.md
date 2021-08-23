---
description: Localise la fonction cible de l’importation spécifiée et remplace le pointeur de fonction dans le thunk d’importation par la cible de l’implémentation de fonction.
ms.assetid: 4ab79b7c-81d1-40bf-a76b-217d93567e40
title: ResolveDelayLoadedAPI fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResolveDelayLoadedAPI
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
ms.openlocfilehash: 359de5c52417f09c35e2fc994e36f0efd054f2a18dc3063be71dc12d588c60e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571549"
---
# <a name="resolvedelayloadedapi-function"></a>ResolveDelayLoadedAPI fonction)

Localise la fonction cible de l’importation spécifiée et remplace le pointeur de fonction dans le thunk d’importation par la cible de l’implémentation de fonction.

## <a name="syntax"></a>Syntaxe


```C++
PVOID WINAPI ResolveDelayLoadedAPI(
  _In_       PVOID                             ParentModuleBase,
  _In_       PCIMAGE_DELAYLOAD_DESCRIPTOR      DelayloadDescriptor,
  _In_opt_   PDELAYLOAD_FAILURE_DLL_CALLBACK   FailureDllHook,
  _In_opt_   PDELAYLOAD_FAILURE_SYSTEM_ROUTINE FailureSystemHook,
  _Out_      PIMAGE_THUNK_DATA                 ThunkAddress,
  _Reserved_ ULONG                             Flags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ParentModuleBase* \[ dans\]
</dt> <dd>

Adresse de la base du module qui importe une fonction à chargement différé.

</dd> <dt>

*DelayloadDescriptor* \[ dans\]
</dt> <dd>

Descripteur du module à charger.

</dd> <dt>

*FailureDllHook* \[ dans, facultatif\]
</dt> <dd>

Adresse du raccordement de l’échec. Consultez [**DelayLoadFailureHook**](delayloadfailurehook.md).

</dd> <dt>

*FailureSystemHook* \[ dans, facultatif\]
</dt> <dd>

Adresse du hook d’échec système.

</dd> <dt>

*ThunkAddress* \[ à\]
</dt> <dd>

Données de thunk pour la fonction cible. Utilisé pour Rechercher l’entrée de table de noms spécifique de la fonction.

</dd> <dt>

*Indicateurs* 
</dt> <dd>

Réservé doit être égal à 0.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Adresse de l’importation, ou stub d’échec pour celle-ci.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Bibliothèque<br/> | <dl> <dt>Kernel32.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Prise en charge de l’éditeur de liens pour les dll Delay-Loaded](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)
</dt> </dl>

 

 




