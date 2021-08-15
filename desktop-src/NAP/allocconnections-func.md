---
title: AllocConnections, fonction (NapUtil. h)
description: Alloue de la mémoire pour un nombre spécifié de structures de connexions.
ms.assetid: 0e0075ed-6e4c-43f7-af40-c6dea2808d05
keywords:
- AllocConnections fonction NAP
topic_type:
- apiref
api_name:
- AllocConnections
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf86a44b81ef12234fdac675aa55d36c5e1a336b4316382c3fd322cf0d6ba87a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800203"
---
# <a name="allocconnections-function"></a>AllocConnections fonction)

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La fonction **AllocConnections** alloue de la mémoire pour un nombre spécifié de structures de [**connexions**](connections-struct.md) .

## <a name="syntax"></a>Syntaxe


```C++
NAPAPI HRESULT WINAPI AllocConnections(
  _Inout_ Connections **connections,
  _In_    UINT16      connectionsCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*connexions* \[ in, out\]
</dt> <dd>

Pointeur vers un tableau de structures de [**connexions**](connections-struct.md) qui viennent d’être allouées.

</dd> <dt>

*connectionsCount* \[ dans\]
</dt> <dd>

Nombre de structures à allouer aux *connexions*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée



| Code de retour                                                                                   | Description                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | L’opération s’est terminée avec succès.<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Un argument non valide a été passé.<br/>                                 |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire virtuelle du système est insuffisante. Cette opération a échoué.<br/> |



 

## <a name="remarks"></a>Remarques

Toutes les interfaces COM prises en charge par le système NAP utilisent des règles de gestion de mémoire COM standard et les allocateurs de mémoire COM (**CoTaskMemAlloc** et **CoTaskMemFree**) :

-   Les paramètres **in** sont alloués et libérés par l’appelant.
-   Les paramètres **out** sont alloués par l’appelé et libérés par l’appelant à l’aide de **CoTaskMem**.
-   Les paramètres **in/out** sont alloués par l’appelant, libérés et réalloués par l’appelé, et libérés au final par l’appelant, à l’aide de **CoTaskMem**.

Toutes les fonctions NAP pour libérer de la mémoire libèrent également tous les pointeurs incorporés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>NapUtil. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FreeConnections**](freeconnections-func.md)
</dt> </dl>

 

 





