---
description: Récupère la taille et l’emplacement de la liste des modules déchargés de manière dynamique pour le processus en cours.
ms.assetid: 53ac9a7f-aa4a-412d-a6f7-a3a73bede5c2
title: RtlGetUnloadEventTraceEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetUnloadEventTraceEx
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 05b9e076041d0cd2298799970670478e9d358d32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533162"
---
# <a name="rtlgetunloadeventtraceex-function"></a>RtlGetUnloadEventTraceEx fonction)

Récupère la taille et l’emplacement de la liste des modules déchargés de manière dynamique pour le processus en cours.

## <a name="syntax"></a>Syntaxe


```C++
VOID WINAPI RtlGetUnloadEventTraceEx(
  _Out_ PULONG *ElementSize,
  _Out_ PULONG *ElementCount,
  _Out_ PVOID  *EventTrace
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Éléments* \[ à\]
</dt> <dd>

Pointeur vers une variable qui contient la taille d’un élément de la liste.

</dd> <dt>

*ElementCount* \[ à\]
</dt> <dd>

Pointeur vers une variable qui contient le nombre d’éléments dans la liste.

</dd> <dt>

*EventTrace* \[ à\]
</dt> <dd>

Pointeur vers un tableau de structures **de \_ \_ \_ trace d’événements de déchargement RTL** . Pour plus d'informations, consultez la section Notes.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Le chargeur stocke les informations sur les événements déchargés dans des emplacements pouvant être lus entre les processus en tirant parti du fait que Ntdll.dll est chargé à la même adresse de base dans tous les processus. Lorsqu’un débogueur doit interroger des informations de module déchargées, il appelle cette fonction pour déterminer l’adresse à laquelle les variables résident, puis interroge la mémoire virtuelle dans le processus cible à ces adresses pour lire les valeurs réelles.

Chaque élément de la liste est défini comme suit.

``` syntax
typedef struct _RTL_UNLOAD_EVENT_TRACE {
    PVOID BaseAddress;   // Base address of dll
    SIZE_T SizeOfImage;  // Size of image
    ULONG Sequence;      // Sequence number for this event
    ULONG TimeDateStamp; // Time and date of image
    ULONG CheckSum;      // Image checksum
    WCHAR ImageName[32]; // Image name
} RTL_UNLOAD_EVENT_TRACE, *PRTL_UNLOAD_EVENT_TRACE;
```

Cette fonction n’a aucun fichier d’en-tête associé. La bibliothèque d’importation associée, ntdll. lib, est disponible dans le kit WDK (Windows Driver Kit). Vous pouvez également appeler cette fonction à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
