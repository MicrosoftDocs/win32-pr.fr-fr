---
description: Inscrit le fournisseur et initialise les ensembles de compteurs.
ms.assetid: edcf8df3-0f6d-4849-b41d-270509499b8e
title: CounterInitialize fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterInitialize
api_type:
- NA
api_location: ''
ms.openlocfilehash: e7c2fb61b53ca1847eefcc453a91f69b3c0602e06277b4858b8f0b733be7f71b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517679"
---
# <a name="counterinitialize-function"></a>CounterInitialize fonction)

Inscrit le fournisseur et initialise les ensembles de compteurs.

## <a name="syntax"></a>Syntaxe


```C++
ULONG WINAPI CounterInitialize(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Retourne l’erreur \_ de réussite en cas de réussite ; sinon, code d’erreur Win32 standard.

## <a name="remarks"></a>Remarques

Votre fournisseur appelle cette fonction. La fonction comprend des appels à la fonction [**PerfStartProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) et à la fonction [**PerfSetCounterSetInfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo) .

L’outil [**CTRPP**](ctrpp.md) génère cette fonction inline lorsque vous spécifiez l’argument **-o** . Le nom de la fonction inclut une chaîne de *préfixe* si vous spécifiez l’argument **-prefix** .

Si vous spécifiez les arguments **-MemoryRoutines** ou **-NotificationCallback** (ou si vous spécifiez l’attribut **callback** pour l’élément [**Provider**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) ), la signature **CounterInitialize** est remplacée par ce qui suit :

``` syntax
ULONG WINAPI CounterInitialize(
    __in_opt PERFLIBREQUEST NotificationCallback,
    __in_opt PERF_MEM_ALLOC MemoryAllocationFunction,
    __in_opt PERF_MEM_FREE MemoryFreeFunction,
    __inout_opt PVOID MemoryFunctionContext
);
```

où :

<dl> <dt>

<span id="NotificationCallback"></span><span id="notificationcallback"></span><span id="NOTIFICATIONCALLBACK"></span>NotificationCallback
</dt> <dd>

Nom de votre fonction de rappel [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) que vous implémentez pour recevoir la notification des demandes des consommateurs (par exemple, les demandes d’ajout ou de suppression de compteurs de la requête). Affectez la valeur **null** si vous n’implémentez pas la fonction de rappel *ControlCallback* .

</dd> <dt>

<span id="MemoryAllocationFunction"></span><span id="memoryallocationfunction"></span><span id="MEMORYALLOCATIONFUNCTION"></span>MemoryAllocationFunction
</dt> <dd>

Nom de votre fonction de rappel [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) que PERFLIB appelle pour allouer de la mémoire. Affectez la valeur **null** si vous n’avez pas spécifié l’argument **-MemoryRoutines** .

</dd> <dt>

<span id="MemoryFreeFunction"></span><span id="memoryfreefunction"></span><span id="MEMORYFREEFUNCTION"></span>MemoryFreeFunction
</dt> <dd>

Nom de votre fonction de rappel [*FreeMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) que PERFLIB appelle pour libérer la mémoire allouée à l’aide de la fonction [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) . A la valeur **null** si *MemoryAllocationFunction* a la **valeur null**.

</dd> <dt>

<span id="MemoryFunctionContext"></span><span id="memoryfunctioncontext"></span><span id="MEMORYFUNCTIONCONTEXT"></span>MemoryFunctionContext
</dt> <dd>

Informations de contexte à passer à votre allocation de mémoire et à vos routines gratuites. Peut avoir la **valeur null**.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/> |



 

