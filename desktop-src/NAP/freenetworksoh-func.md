---
title: FreeNetworkSoH, fonction (NapUtil. h)
description: Libère une structure de données NetworkSoH.
ms.assetid: a27d54a0-8b9c-4bf7-909c-1de5db55f429
keywords:
- FreeNetworkSoH fonction NAP
topic_type:
- apiref
api_name:
- FreeNetworkSoH
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9ea2b72011332939aa0c814203d0004949c8341
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466466"
---
# <a name="freenetworksoh-function"></a>FreeNetworkSoH fonction)

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La fonction **FreeNetworkSoH** libère une structure de données [**NetworkSoH**](/windows/win32/api/naptypes/ns-naptypes-networksoh) .

## <a name="syntax"></a>Syntaxe


```C++
NAPAPI VOID WINAPI FreeNetworkSoH(
  _In_ NetworkSoH *networkSoh
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*networkSoh* \[ dans\]
</dt> <dd>

Pointeur vers la structure de données [**NetworkSoH**](/windows/win32/api/naptypes/ns-naptypes-networksoh) à libérer.

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



 

 





