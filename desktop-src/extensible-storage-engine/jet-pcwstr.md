---
description: 'En savoir plus sur : JET_PCWSTR'
title: JET_PCWSTR
TOCTitle: JET_PCWSTR
ms:assetid: fef64bb9-c2e0-4cfb-8138-c98ae6f50952
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294145(v=EXCHG.10)
ms:contentKeyID: 32765759
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
ms.openlocfilehash: 51cd0dab17096fb8f7371a01ebabfca3abc595be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535626"
---
# <a name="jet_pcwstr"></a><span data-ttu-id="3aecc-103">JET_PCWSTR</span><span class="sxs-lookup"><span data-stu-id="3aecc-103">JET_PCWSTR</span></span>


<span data-ttu-id="3aecc-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="3aecc-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_pcwstr"></a><span data-ttu-id="3aecc-105">JET_PCWSTR</span><span class="sxs-lookup"><span data-stu-id="3aecc-105">JET_PCWSTR</span></span>

<span data-ttu-id="3aecc-106">Le type de données **JET_PCWSTR** contient une chaîne **Unicode** constante, qui se termine par un caractère null (char \* ).</span><span class="sxs-lookup"><span data-stu-id="3aecc-106">The **JET_PCWSTR** data type contains a null-terminated, constant **Unicode** string (char \*).</span></span>

<span data-ttu-id="3aecc-107">**Windows Vista : JET_PCWSTR** est introduite dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3aecc-107">**Windows Vista:  JET_PCWSTR** is introduced in Windows Vista.</span></span>

```cpp
    typedef __nullterminated const WCHAR * JET_PCWSTR;
```

### <a name="data-types"></a><span data-ttu-id="3aecc-108">Types de données</span><span class="sxs-lookup"><span data-stu-id="3aecc-108">Data Types</span></span>

<span data-ttu-id="3aecc-109">JET_PCWSTR</span><span class="sxs-lookup"><span data-stu-id="3aecc-109">JET_PCWSTR</span></span>

<span data-ttu-id="3aecc-110">Chaîne Unicode constante (Char) terminée par un caractère null \* .</span><span class="sxs-lookup"><span data-stu-id="3aecc-110">Null-terminated, constant Unicode string (char \*).</span></span>

### <a name="requirements"></a><span data-ttu-id="3aecc-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3aecc-111">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3aecc-112"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="3aecc-112"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3aecc-113">Nécessite Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3aecc-113">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3aecc-114"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="3aecc-114"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3aecc-115">Requiert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="3aecc-115">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3aecc-116"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="3aecc-116"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3aecc-117">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="3aecc-117">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

