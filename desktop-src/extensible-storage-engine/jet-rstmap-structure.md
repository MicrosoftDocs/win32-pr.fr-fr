---
description: 'En savoir plus sur : structure JET_RSTMAP'
title: Structure JET_RSTMAP
TOCTitle: JET_RSTMAP Structure
ms:assetid: bddf95e4-1bd4-4e3a-ad3e-d01f6564e33b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294077(v=EXCHG.10)
ms:contentKeyID: 32765692
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
ms.openlocfilehash: 646a055230b6476abf70abcde582fc2015cb241c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750556"
---
# <a name="jet_rstmap-structure"></a><span data-ttu-id="a88cf-103">Structure JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="a88cf-103">JET_RSTMAP Structure</span></span>


<span data-ttu-id="a88cf-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="a88cf-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_rstmap-structure"></a><span data-ttu-id="a88cf-105">Structure JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="a88cf-105">JET_RSTMAP Structure</span></span>

<span data-ttu-id="a88cf-106">La structure **JET_RSTMAP** permet le remappage des chemins d’accès aux fichiers de base de données qui sont stockés dans les journaux de transactions pendant la récupération, lorsqu’ils sont utilisés par les fonctions [JetInit](./jetinit-function.md) et [JetExternalRestore](./jetexternalrestore-function.md) .</span><span class="sxs-lookup"><span data-stu-id="a88cf-106">The **JET_RSTMAP** structure enables the remapping of database file paths that are stored in the transaction logs during recovery, when used by the [JetInit](./jetinit-function.md) and [JetExternalRestore](./jetexternalrestore-function.md) functions.</span></span> <span data-ttu-id="a88cf-107">Cela permet aux bases de données d’être déplacées hors connexion ou en cas de restauration à partir d’une sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="a88cf-107">This enables the databases to be moved when offline or when restored from backup.</span></span>

```cpp
    typedef struct {
      xRPC_STRING tchar* szDatabaseName;
      xRPC_STRING tchar* szNewDatabaseName;
    } JET_RSTMAP;
```

### <a name="members"></a><span data-ttu-id="a88cf-108">Membres</span><span class="sxs-lookup"><span data-stu-id="a88cf-108">Members</span></span>

<span data-ttu-id="a88cf-109">**szDatabaseName**</span><span class="sxs-lookup"><span data-stu-id="a88cf-109">**szDatabaseName**</span></span>

<span data-ttu-id="a88cf-110">Chemin d’accès absolu actuel d’une base de données associée aux journaux des transactions qui sont relus lors de la récupération.</span><span class="sxs-lookup"><span data-stu-id="a88cf-110">The current absolute path of a database that is associated with the transaction logs that are replayed during recovery.</span></span>

<span data-ttu-id="a88cf-111">**szNewDatabaseName**</span><span class="sxs-lookup"><span data-stu-id="a88cf-111">**szNewDatabaseName**</span></span>

<span data-ttu-id="a88cf-112">Nouveau chemin d’accès absolu de la base de données.</span><span class="sxs-lookup"><span data-stu-id="a88cf-112">The new absolute path for the database.</span></span>

### <a name="requirements"></a><span data-ttu-id="a88cf-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a88cf-113">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a88cf-114"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="a88cf-114"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a88cf-115">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="a88cf-115">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a88cf-116"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="a88cf-116"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a88cf-117">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a88cf-117">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a88cf-118"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="a88cf-118"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a88cf-119">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="a88cf-119">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a88cf-120"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="a88cf-120"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="a88cf-121">Implémenté comme <strong>JET_RSTMAP_W</strong> (Unicode) et <strong>JET_RSTMAP_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="a88cf-121">Implemented as <strong>JET_RSTMAP_W</strong> (Unicode) and <strong>JET_RSTMAP_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="a88cf-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a88cf-122">See Also</span></span>

[<span data-ttu-id="a88cf-123">JetExternalRestore</span><span class="sxs-lookup"><span data-stu-id="a88cf-123">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="a88cf-124">JetInit</span><span class="sxs-lookup"><span data-stu-id="a88cf-124">JetInit</span></span>](./jetinit-function.md)
