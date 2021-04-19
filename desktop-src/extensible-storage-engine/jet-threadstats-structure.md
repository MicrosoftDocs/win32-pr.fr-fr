---
description: 'En savoir plus sur : structure JET_THREADSTATS'
title: Structure JET_THREADSTATS
TOCTitle: JET_THREADSTATS Structure
ms:assetid: 37e86e14-7719-4991-aae8-bcff1baa80df
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269227(v=EXCHG.10)
ms:contentKeyID: 32765529
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
ms.openlocfilehash: 2b84de9a4f64db5dda261b8ee177787f62fd01ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106537057"
---
# <a name="jet_threadstats-structure"></a><span data-ttu-id="b48d3-103">Structure JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="b48d3-103">JET_THREADSTATS Structure</span></span>


<span data-ttu-id="b48d3-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="b48d3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_threadstats-structure"></a><span data-ttu-id="b48d3-105">Structure JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="b48d3-105">JET_THREADSTATS Structure</span></span>

<span data-ttu-id="b48d3-106">La structure **JET_THREADSTATS** contient des statistiques cumulatives sur le travail effectué par le moteur de base de données sur le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="b48d3-106">The **JET_THREADSTATS** structure contains cumulative statistics on the work performed by the database engine on the current thread.</span></span> <span data-ttu-id="b48d3-107">Ces informations sont retournées via [JetGetThreadStats](./jetgetthreadstats-function.md).</span><span class="sxs-lookup"><span data-stu-id="b48d3-107">This information is returned via [JetGetThreadStats](./jetgetthreadstats-function.md).</span></span>

<span data-ttu-id="b48d3-108">**Windows Vista :**  La structure **JET_THREADSTATS** est introduite dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b48d3-108">**Windows Vista:**  The **JET_THREADSTATS** structure is introduced in Windows Vista.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cPageReferenced;
      unsigned long cPageRead;
      unsigned long cPagePreread;
      unsigned long cPageDirtied;
      unsigned long cPageRedirtied;
      unsigned long cLogRecord;
      unsigned long cbLogRecord;
    } JET_THREADSTATS;
```

### <a name="members"></a><span data-ttu-id="b48d3-109">Membres</span><span class="sxs-lookup"><span data-stu-id="b48d3-109">Members</span></span>

<span data-ttu-id="b48d3-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="b48d3-110">**cbStruct**</span></span>

<span data-ttu-id="b48d3-111">Taille de la structure **JET_THREADSTATS** retournée, en octets.</span><span class="sxs-lookup"><span data-stu-id="b48d3-111">The size of the returned **JET_THREADSTATS** structure, in bytes.</span></span>

<span data-ttu-id="b48d3-112">**Remarque**  La structure **JET_THREADSTATS** sera développée à l’avenir pour contenir plus de statistiques.</span><span class="sxs-lookup"><span data-stu-id="b48d3-112">**Note**  The **JET_THREADSTATS** structure will expand in the future to contain more statistics.</span></span> <span data-ttu-id="b48d3-113">De nouvelles statistiques seront ajoutées à la fin de la structure et peuvent être récupérées avec une taille de mémoire tampon de sortie accrue.</span><span class="sxs-lookup"><span data-stu-id="b48d3-113">New statistics will be added to the end of the structure and can be retrieved with an increased output buffer size.</span></span> <span data-ttu-id="b48d3-114">La présence de statistiques supplémentaires peut être déduite par une valeur **cbStruct** plus grande.</span><span class="sxs-lookup"><span data-stu-id="b48d3-114">The presence of additional statistics can be inferred by a larger **cbStruct** value.</span></span>

<span data-ttu-id="b48d3-115">**cPageReferenced**</span><span class="sxs-lookup"><span data-stu-id="b48d3-115">**cPageReferenced**</span></span>

<span data-ttu-id="b48d3-116">Nombre total de pages de base de données visitées par le moteur de base de données sur le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="b48d3-116">The total number of database pages visited by the database engine on the current thread.</span></span>

<span data-ttu-id="b48d3-117">**cPageRead**</span><span class="sxs-lookup"><span data-stu-id="b48d3-117">**cPageRead**</span></span>

<span data-ttu-id="b48d3-118">Nombre total de pages de base de données extraites du disque par le moteur de base de données sur le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="b48d3-118">The total number of database pages fetched from disk by the database engine on the current thread.</span></span>

<span data-ttu-id="b48d3-119">**cPagePreread**</span><span class="sxs-lookup"><span data-stu-id="b48d3-119">**cPagePreread**</span></span>

<span data-ttu-id="b48d3-120">Nombre total de pages de base de données prérécupérées à partir du disque par le moteur de base de données sur le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="b48d3-120">The total number of database pages prefetched from disk by the database engine on the current thread.</span></span>

<span data-ttu-id="b48d3-121">**cPageDirtied**</span><span class="sxs-lookup"><span data-stu-id="b48d3-121">**cPageDirtied**</span></span>

<span data-ttu-id="b48d3-122">Nombre total de pages de base de données, sans modification non écrite, qui ont été modifiées par le moteur de base de données sur le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="b48d3-122">The total number of database pages, with no unwritten changes, that have been modified by the database engine on the current thread.</span></span>

<span data-ttu-id="b48d3-123">**cPageRedirtied**</span><span class="sxs-lookup"><span data-stu-id="b48d3-123">**cPageRedirtied**</span></span>

<span data-ttu-id="b48d3-124">Nombre total de pages de base de données, avec des modifications non écrites, qui ont été modifiées par le moteur de base de données sur le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="b48d3-124">The total number of database pages, with unwritten changes, that have been modified by the database engine on the current thread.</span></span>

<span data-ttu-id="b48d3-125">**cLogRecord**</span><span class="sxs-lookup"><span data-stu-id="b48d3-125">**cLogRecord**</span></span>

<span data-ttu-id="b48d3-126">Nombre total d’enregistrements du journal des transactions qui ont été générés par le moteur de base de données sur le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="b48d3-126">The total number of transaction log records that have been generated by the database engine on the current thread.</span></span>

<span data-ttu-id="b48d3-127">**cbLogRecord**</span><span class="sxs-lookup"><span data-stu-id="b48d3-127">**cbLogRecord**</span></span>

<span data-ttu-id="b48d3-128">Taille totale, en octets, des enregistrements du journal des transactions qui ont été générés par le moteur de base de données sur le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="b48d3-128">The total size in bytes of transaction log records that have been generated by the database engine on the current thread.</span></span>

### <a name="requirements"></a><span data-ttu-id="b48d3-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b48d3-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b48d3-130"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="b48d3-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b48d3-131">Nécessite Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b48d3-131">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b48d3-132"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="b48d3-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b48d3-133">Requiert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="b48d3-133">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b48d3-134"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="b48d3-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b48d3-135">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="b48d3-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="b48d3-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b48d3-136">See Also</span></span>

[<span data-ttu-id="b48d3-137">JetGetThreadStats</span><span class="sxs-lookup"><span data-stu-id="b48d3-137">JetGetThreadStats</span></span>](./jetgetthreadstats-function.md)
