---
title: FreeSystemHealthAgentState, fonction (NapUtil. h)
description: Libère une structure de données SystemHealthAgentState.
ms.assetid: e9bfa8ee-c335-416e-94cf-28646709d419
keywords:
- FreeSystemHealthAgentState fonction NAP
topic_type:
- apiref
api_name:
- FreeSystemHealthAgentState
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ce59135de1c8f47d84a07f01dbb5f2bbe697f9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103301"
---
# <a name="freesystemhealthagentstate-function"></a>FreeSystemHealthAgentState fonction)

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La fonction **FreeSystemHealthAgentState** libère une structure de données [**SystemHealthAgentState**](/windows/win32/api/naptypes/ns-naptypes-systemhealthagentstate) .

## <a name="syntax"></a>Syntaxe


```C++
NAPAPI VOID WINAPI FreeSystemHealthAgentState(
  _In_ SystemHealthAgentState *state
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*État* \[ dans\]
</dt> <dd>

Pointeur vers la structure de données [**SystemHealthAgentState**](/windows/win32/api/naptypes/ns-naptypes-systemhealthagentstate) à libérer.

</dd> </dl>

## <a name="remarks"></a>Notes

Toutes les interfaces COM prises en charge par le système NAP utilisent des règles de gestion de mémoire COM standard et les allocateurs de mémoire COM (**CoTaskMemAlloc** et **CoTaskMemFree**) :

-   Les paramètres **in** sont alloués et libérés par l’appelant.
-   Les paramètres **out** sont alloués par l’appelé et libérés par l’appelant à l’aide de **CoTaskMem**.
-   Les paramètres **in/out** sont alloués par l’appelant, libérés et réalloués par l’appelé, et libérés au final par l’appelant, à l’aide de **CoTaskMem**.

Toutes les fonctions NAP pour libérer de la mémoire libèrent également tous les pointeurs incorporés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>NapUtil. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



 

 





