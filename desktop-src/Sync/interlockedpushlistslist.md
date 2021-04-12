---
UID: ''
title: InterlockedPushListSList, fonction
description: Insère une liste à liaison unique à l’avant d’une autre liste à liaison unique.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: InterlockedPushListSListEx
ms.topic: reference
req.header:
- WinBase.h on Windows Vista, Windows 7, Windows Server 2008 and Windows Server 2008 R2
- InterlockedAPI.h on Windows 8 and Windows Server 2012
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Kernel32.lib
req.dll: API-MS-Win-Core-interlocked-l1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Core-interlocked-l1-1-0.dll
api_name:
- InterlockedPushListSList
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: ccecdae3af5119a86594c31856dac11ecb4507bc
ms.sourcegitcommit: be77ed1f97d3be57a2f42070589de21b66034adf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2020
ms.locfileid: "104381710"
---
# <a name="interlockedpushlistslist-function"></a>InterlockedPushListSList, fonction

## <a name="description"></a>Description

Insère une liste à liaison unique à l’avant d’une autre liste à liaison unique.
L’accès aux listes est synchronisé sur un système multiprocesseur.

```cpp
PSLIST_ENTRY  FASTCALL InterlockedPushListSList(
  _Inout_ PSLIST_HEADER ListHead,
  _Inout_ PSLIST_ENTRY  List,
  _Inout_ PSLIST_ENTRY  ListEnd,
  _In_    ULONG         Count
);
```

## <a name="parameters"></a>Paramètres

### <a name="listhead-in-out"></a>ListHead [in, out]

Pointeur vers une structure **SLIST_HEADER** qui représente l’en-tête d’une liste liée de façon unique.
La liste spécifiée par la *liste* et les paramètres d' *écoute* est insérée au début de cette liste.

### <a name="list-in-out"></a>List [in, out]

Pointeur vers une structure [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) qui représente le premier élément de la liste à insérer.

### <a name="listend-in-out"></a>ListEned [in, out]

Pointeur vers une structure [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) qui représente le dernier élément de la liste à insérer.

### <a name="count-in"></a>Nombre [in]

Nombre d’éléments dans la liste à insérer.

## <a name="returns"></a>Retours

La valeur de retour est le premier élément précédent dans la liste spécifiée par le paramètre *listhead* .
Si la liste était déjà vide, la valeur de retour est **null**.

## <a name="remarks"></a>Notes

Tous les éléments de liste doivent être alignés sur une limite de **MEMORY_ALLOCATION_ALIGNMENT** ; dans le cas contraire, cette fonction se comportera de façon imprévisible.
Consultez **_aligned_malloc**.

**Windows 8 et Windows Server 2012 :**  Cette fonction a été remplacée par [InterlockedPushListSListEx](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex).
Lors de la compilation avec **NTDDI_VERSION** défini sur **NTDDI_WIN8** ou une valeur supérieure, les appels à **InterlockedPushListSList** vont à **InterlockedPushListSListEx** à la place.

## <a name="see-also"></a>Voir aussi

[Listes liées de façon isolée](/windows/desktop/Sync/interlocked-singly-linked-lists)

[InterlockedPopEntrySList](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist)

[InterlockedPushEntrySList](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist)

[InterlockedPushListSListEx](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)

[InterlockedFlushSList](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedflushslist)

[SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry)

[Utilisation de listes liées de façon unique](/windows/desktop/Sync/using-singly-linked-lists)
