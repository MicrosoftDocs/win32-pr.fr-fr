---
description: 'En savoir plus sur : structure JET_LGPOS'
title: Structure JET_LGPOS
TOCTitle: JET_LGPOS Structure
ms:assetid: dbce1a60-b32b-40c1-a215-e93bb77cd8c1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294113(v=EXCHG.10)
ms:contentKeyID: 32765727
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
ms.openlocfilehash: 25f00c73a4bb922a8152335babe222b539c70ade
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034917"
---
# <a name="jet_lgpos-structure"></a><span data-ttu-id="b7803-103">Structure JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="b7803-103">JET_LGPOS Structure</span></span>


<span data-ttu-id="b7803-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="b7803-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_lgpos-structure"></a><span data-ttu-id="b7803-105">Structure JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="b7803-105">JET_LGPOS Structure</span></span>

<span data-ttu-id="b7803-106">La structure **JET_LGPOS** contient des données qui sont internes au mécanisme de journalisation du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="b7803-106">The **JET_LGPOS** structure holds data that is internal to the logging mechanism of the database engine.</span></span> <span data-ttu-id="b7803-107">Cette structure est considérée comme interne.</span><span class="sxs-lookup"><span data-stu-id="b7803-107">This structure is considered internal.</span></span>

```cpp
    typedef struct {
      unsigned short ib;
      unsigned short isec;
      long lGeneration;
    } JET_LGPOS;
```

### <a name="members"></a><span data-ttu-id="b7803-108">Membres</span><span class="sxs-lookup"><span data-stu-id="b7803-108">Members</span></span>

<span data-ttu-id="b7803-109">**IB**</span><span class="sxs-lookup"><span data-stu-id="b7803-109">**ib**</span></span>

<span data-ttu-id="b7803-110">Prend en charge l’infrastructure ESE et ne peut pas être utilisé à partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="b7803-110">Supports the ESE infrastructure and cannot be used from your code.</span></span>

<span data-ttu-id="b7803-111">**ISEC**</span><span class="sxs-lookup"><span data-stu-id="b7803-111">**isec**</span></span>

<span data-ttu-id="b7803-112">Prend en charge l’infrastructure ESE et ne peut pas être utilisé à partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="b7803-112">Supports the ESE infrastructure and cannot be used from your code.</span></span>

<span data-ttu-id="b7803-113">**lGeneration**</span><span class="sxs-lookup"><span data-stu-id="b7803-113">**lGeneration**</span></span>

<span data-ttu-id="b7803-114">Prend en charge l’infrastructure ESE et ne peut pas être utilisé à partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="b7803-114">Supports the ESE infrastructure and cannot be used from your code.</span></span>

### <a name="requirements"></a><span data-ttu-id="b7803-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7803-115">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7803-116"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="b7803-116"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b7803-117">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="b7803-117">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7803-118"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="b7803-118"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b7803-119">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b7803-119">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7803-120"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="b7803-120"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b7803-121">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="b7803-121">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="b7803-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7803-122">See Also</span></span>

[<span data-ttu-id="b7803-123">JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="b7803-123">JET_BKINFO</span></span>](./jet-bkinfo-structure.md)  
[<span data-ttu-id="b7803-124">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="b7803-124">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)
