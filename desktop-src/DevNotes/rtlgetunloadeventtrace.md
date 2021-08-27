---
description: Permet au code de vidage d’obtenir les informations de module déchargées à partir de Ntdll.dll pour le stockage dans le minidump.
ms.assetid: 017398da-e13e-4261-bda5-6f400a91dbe3
title: RtlGetUnloadEventTrace fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetUnloadEventTrace
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: d8575610ab34b62c9228f87fa64fbd6a40fa0201b7fe1a70ab95c7daae706854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058589"
---
# <a name="rtlgetunloadeventtrace-function"></a>RtlGetUnloadEventTrace fonction)

\[cette fonction peut être modifiée ou supprimée de Windows sans préavis.\]

Permet au code de vidage d’obtenir les informations de module déchargées à partir de Ntdll.dll pour le stockage dans le minidump.

## <a name="syntax"></a>Syntaxe


```C++
 PRTL_UNLOAD_EVENT_TRACE RtlGetUnloadEventTrace(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne un pointeur vers un tableau. Pour plus d'informations, consultez la section Notes.

## <a name="remarks"></a>Remarques

Le tableau RtlpUnloadEventTrace est défini comme suit :

``` syntax
#define RTL_UNLOAD_EVENT_TRACE_NUMBER 64

typedef struct _RTL_UNLOAD_EVENT_TRACE {
    PVOID BaseAddress;   // Base address of dll
    SIZE_T SizeOfImage;  // Size of image
    ULONG Sequence;      // Sequence number for this event
    ULONG TimeDateStamp; // Time and date of image
    ULONG CheckSum;      // Image checksum
    WCHAR ImageName[32]; // Image name
} RTL_UNLOAD_EVENT_TRACE, *PRTL_UNLOAD_EVENT_TRACE;

RTL_UNLOAD_EVENT_TRACE RtlpUnloadEventTrace[RTL_UNLOAD_EVENT_TRACE_NUMBER];
```

Cette fonction n’a aucun fichier d’en-tête associé. la bibliothèque d’importation associée, Ntdll. lib, est disponible dans le Kit de pilotes Windows (WDK). Vous pouvez également appeler cette fonction à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
