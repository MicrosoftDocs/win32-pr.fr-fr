---
description: 'En savoir plus sur : WCHAR'
title: WCHAR
TOCTitle: WCHAR
ms:assetid: 922431b3-bf9a-4aba-bc67-dd33d9aeaac0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269344(v=EXCHG.10)
ms:contentKeyID: 32765633
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
ms.openlocfilehash: 1dfa86cbc771059d941027385090dcbd2f401855
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516868"
---
# <a name="wchar"></a><span data-ttu-id="9f7ee-103">WCHAR</span><span class="sxs-lookup"><span data-stu-id="9f7ee-103">WCHAR</span></span>


<span data-ttu-id="9f7ee-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="9f7ee-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="wchar"></a><span data-ttu-id="9f7ee-105">WCHAR</span><span class="sxs-lookup"><span data-stu-id="9f7ee-105">WCHAR</span></span>

<span data-ttu-id="9f7ee-106">Le type de données WCHAR contient un caractère Unicode 16 bits.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-106">The WCHAR data type contains a 16-bit Unicode character.</span></span>

```cpp
    #if !defined(_NATIVE_WCHAR_T_DEFINED)
    typedef unsigned short WCHAR;
    #else
    typedef wchar_t WCHAR;
    #endif
```

### <a name="data-types"></a><span data-ttu-id="9f7ee-107">Types de données</span><span class="sxs-lookup"><span data-stu-id="9f7ee-107">Data Types</span></span>

<span data-ttu-id="9f7ee-108">WCHAR</span><span class="sxs-lookup"><span data-stu-id="9f7ee-108">WCHAR</span></span>

<span data-ttu-id="9f7ee-109">Caractère Unicode 16 bits.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-109">A 16-bit Unicode character.</span></span>

### <a name="requirements"></a><span data-ttu-id="9f7ee-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9f7ee-110">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f7ee-111"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="9f7ee-111"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9f7ee-112">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-112">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f7ee-113"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="9f7ee-113"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9f7ee-114">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-114">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f7ee-115"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="9f7ee-115"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9f7ee-116">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-116">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

