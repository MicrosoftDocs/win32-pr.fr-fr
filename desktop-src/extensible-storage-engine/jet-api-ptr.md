---
description: 'En savoir plus sur : JET_API_PTR'
title: JET_API_PTR
TOCTitle: JET_API_PTR
ms:assetid: 27b1eeec-1707-4edb-a4b2-2619190c21e7
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269209(v=EXCHG.10)
ms:contentKeyID: 32765512
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 687f28fcba3d20c5b72a3089d3a442dd97e2dfb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534084"
---
# <a name="jet_api_ptr"></a><span data-ttu-id="a5e42-103">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="a5e42-103">JET_API_PTR</span></span>


<span data-ttu-id="a5e42-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="a5e42-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_api_ptr"></a><span data-ttu-id="a5e42-105">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="a5e42-105">JET_API_PTR</span></span>

<span data-ttu-id="a5e42-106">Le type de données **JET_API_PTR** contient un entier ou une valeur de pointeur.</span><span class="sxs-lookup"><span data-stu-id="a5e42-106">The **JET_API_PTR** data type holds an integer or a pointer value.</span></span>

```cpp
    #if defined(_WIN64)
        typedef unsigned __int64 JET_API_PTR;
    #elif !defined(__midl) && (defined(_X86_) || defined(_M_IX86)) && _MSC_VER >= 1300
        typedef __w64 unsigned long JET_API_PTR;
    #else
        typedef unsigned long JET_API_PTR;
    #endif
```

### <a name="data-types"></a><span data-ttu-id="a5e42-107">Types de données</span><span class="sxs-lookup"><span data-stu-id="a5e42-107">Data Types</span></span>

<span data-ttu-id="a5e42-108">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="a5e42-108">JET_API_PTR</span></span>

<span data-ttu-id="a5e42-109">À l’instar d’un type de données **DWORD_PTR** , le type de données **JET_API_PTR** est défini sur 4 octets sur un ordinateur 32 bits et sur 8 octets sur un ordinateur 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a5e42-109">Like a **DWORD_PTR** data type, the **JET_API_PTR** data type is defined as 4 bytes on a 32-bit machine and 8 bytes on a 64-bit machine.</span></span>

### <a name="remarks"></a><span data-ttu-id="a5e42-110">Notes</span><span class="sxs-lookup"><span data-stu-id="a5e42-110">Remarks</span></span>

<span data-ttu-id="a5e42-111">Le type de données **JET_API_PTR** est utilisé pour définir les types de données suivants :</span><span class="sxs-lookup"><span data-stu-id="a5e42-111">The **JET_API_PTR** data type is used to define the following data types:</span></span>

  - [<span data-ttu-id="a5e42-112">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="a5e42-112">JET_HANDLE</span></span>](./jet-handle.md)

  - [<span data-ttu-id="a5e42-113">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="a5e42-113">JET_INSTANCE</span></span>](./jet-instance.md)

  - [<span data-ttu-id="a5e42-114">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a5e42-114">JET_SESID</span></span>](./jet-sesid.md)

  - [<span data-ttu-id="a5e42-115">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="a5e42-115">JET_TABLEID</span></span>](./jet-tableid.md)

  - [<span data-ttu-id="a5e42-116">JET_LS</span><span class="sxs-lookup"><span data-stu-id="a5e42-116">JET_LS</span></span>](./jet-ls.md)

### <a name="requirements"></a><span data-ttu-id="a5e42-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5e42-117">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a5e42-118"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="a5e42-118"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a5e42-119">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="a5e42-119">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5e42-120"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="a5e42-120"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a5e42-121">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a5e42-121">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5e42-122"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="a5e42-122"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a5e42-123">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="a5e42-123">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>
