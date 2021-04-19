---
description: 'En savoir plus sur : structure JET_SIGNATURE'
title: Structure JET_SIGNATURE
TOCTitle: JET_SIGNATURE Structure
ms:assetid: 90d3fd56-be65-4126-b50c-b53e3c3f38f6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269340(v=EXCHG.10)
ms:contentKeyID: 32765629
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
ms.openlocfilehash: d6210853e22fda5085980c2fb285411ba431bb43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514214"
---
# <a name="jet_signature-structure"></a><span data-ttu-id="ba442-103">Structure JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="ba442-103">JET_SIGNATURE Structure</span></span>


<span data-ttu-id="ba442-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="ba442-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_signature-structure"></a><span data-ttu-id="ba442-105">Structure JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="ba442-105">JET_SIGNATURE Structure</span></span>

<span data-ttu-id="ba442-106">La structure **JET_SIGNATURE** contient des informations qui identifient de façon unique une base de données.</span><span class="sxs-lookup"><span data-stu-id="ba442-106">The **JET_SIGNATURE** structure contains information that uniquely identifies a database.</span></span>

```cpp
    typedef struct {
      unsigned long ulRandom;
      JET_LOGTIME logtimeCreate;
      char szComputerName[JET_MAX_COMPUTERNAME_LENGTH + 1];
    } JET_SIGNATURE;
```

### <a name="members"></a><span data-ttu-id="ba442-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ba442-107">Members</span></span>

<span data-ttu-id="ba442-108">**ulRandom**</span><span class="sxs-lookup"><span data-stu-id="ba442-108">**ulRandom**</span></span>

<span data-ttu-id="ba442-109">Nombre assigné de manière aléatoire.</span><span class="sxs-lookup"><span data-stu-id="ba442-109">A randomly assigned number.</span></span>

<span data-ttu-id="ba442-110">**logtimeCreate**</span><span class="sxs-lookup"><span data-stu-id="ba442-110">**logtimeCreate**</span></span>

<span data-ttu-id="ba442-111">Le [JET_LOGTIME](./jet-logtime-structure.md) au moment de l’exécution de [JetCreateDatabase](./jetcreatedatabase-function.md) .</span><span class="sxs-lookup"><span data-stu-id="ba442-111">The [JET_LOGTIME](./jet-logtime-structure.md) at the time of [JetCreateDatabase](./jetcreatedatabase-function.md) is executed.</span></span>

<span data-ttu-id="ba442-112">**szComputerName**</span><span class="sxs-lookup"><span data-stu-id="ba442-112">**szComputerName**</span></span>

<span data-ttu-id="ba442-113">Valeur de chaîne facultative du nom NetBIOS de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ba442-113">The optional string value of the NetBIOS name for the computer.</span></span> <span data-ttu-id="ba442-114">Cette valeur ne peut pas être définie.</span><span class="sxs-lookup"><span data-stu-id="ba442-114">This value may not be set.</span></span>

### <a name="remarks"></a><span data-ttu-id="ba442-115">Notes</span><span class="sxs-lookup"><span data-stu-id="ba442-115">Remarks</span></span>

<span data-ttu-id="ba442-116">Il peut s’agir d’un élément de [JET_DBINFOMISC](./jet-dbinfomisc-structure.md).</span><span class="sxs-lookup"><span data-stu-id="ba442-116">This can be found as an element of [JET_DBINFOMISC](./jet-dbinfomisc-structure.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="ba442-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba442-117">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ba442-118"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ba442-118"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ba442-119">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="ba442-119">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba442-120"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="ba442-120"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ba442-121">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ba442-121">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba442-122"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="ba442-122"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ba442-123">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="ba442-123">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="ba442-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba442-124">See Also</span></span>

[<span data-ttu-id="ba442-125">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="ba442-125">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)  
[<span data-ttu-id="ba442-126">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="ba442-126">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="ba442-127">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="ba442-127">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)
