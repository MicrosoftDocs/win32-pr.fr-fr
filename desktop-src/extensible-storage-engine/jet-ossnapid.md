---
description: 'En savoir plus sur : JET_OSSNAPID'
title: JET_OSSNAPID
TOCTitle: JET_OSSNAPID
ms:assetid: 89b15492-674a-46e4-8aea-991df4f22a6f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269325(v=EXCHG.10)
ms:contentKeyID: 32765615
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
ms.openlocfilehash: b0ca1bb5e2e5a80c9166574708efc7875ed95446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518839"
---
# <a name="jet_ossnapid"></a><span data-ttu-id="f3ea8-103">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="f3ea8-103">JET_OSSNAPID</span></span>


<span data-ttu-id="f3ea8-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="f3ea8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_ossnapid"></a><span data-ttu-id="f3ea8-105">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="f3ea8-105">JET_OSSNAPID</span></span>

<span data-ttu-id="f3ea8-106">Le type de données **JET_OSSNAPID** contient un descripteur d’instantané de la base de données.</span><span class="sxs-lookup"><span data-stu-id="f3ea8-106">The **JET_OSSNAPID** data type contains a handle to a snapshot of the database.</span></span>

```cpp
    typedef JET_API_PTR JET_OSSNAPID;
```

### <a name="data-types"></a><span data-ttu-id="f3ea8-107">Types de données</span><span class="sxs-lookup"><span data-stu-id="f3ea8-107">Data Types</span></span>

<span data-ttu-id="f3ea8-108">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="f3ea8-108">JET_OSSNAPID</span></span>

<span data-ttu-id="f3ea8-109">Handle d’un instantané de la base de données.</span><span class="sxs-lookup"><span data-stu-id="f3ea8-109">A handle to a snapshot of the database.</span></span> <span data-ttu-id="f3ea8-110">Ce descripteur est utilisé dans les éléments de l’API JET impliqués dans la sauvegarde d’instantané.</span><span class="sxs-lookup"><span data-stu-id="f3ea8-110">This handle is used in JET API elements that are involved with snapshot backup.</span></span>

<span data-ttu-id="f3ea8-111">La **valeur null** peut être utilisée pour indiquer un handle non valide.</span><span class="sxs-lookup"><span data-stu-id="f3ea8-111">**NULL** can be used to indicate an invalid handle.</span></span>

### <a name="requirements"></a><span data-ttu-id="f3ea8-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3ea8-112">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3ea8-113"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f3ea8-113"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f3ea8-114">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="f3ea8-114">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3ea8-115"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="f3ea8-115"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f3ea8-116">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f3ea8-116">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3ea8-117"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="f3ea8-117"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f3ea8-118">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="f3ea8-118">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

