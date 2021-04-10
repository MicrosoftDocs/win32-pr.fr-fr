---
description: 'En savoir plus sur : méthode API. JetIntersectIndexes'
title: API. JetIntersectIndexes, méthode
TOCTitle: 'JetIntersectIndexes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_INDEXRANGE[],System.Int32,Microsoft.Isam.Esent.Interop.JET_RECORDLIST@,Microsoft.Isam.Esent.Interop.IntersectIndexesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetintersectindexes(v=EXCHG.10)
ms:contentKeyID: 55100761
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3bae632f386ef944e79a17813d1cc86451441e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953140"
---
# <a name="apijetintersectindexes-method"></a><span data-ttu-id="f8bfc-103">API. JetIntersectIndexes, méthode</span><span class="sxs-lookup"><span data-stu-id="f8bfc-103">Api.JetIntersectIndexes method</span></span>

<span data-ttu-id="f8bfc-104">Calcule l’intersection entre plusieurs jeux d’entrées d’index à partir d’index secondaires différents sur la même table.</span><span class="sxs-lookup"><span data-stu-id="f8bfc-104">Computes the intersection between multiple sets of index entries from different secondary indices over the same table.</span></span> <span data-ttu-id="f8bfc-105">Cette opération est utile pour Rechercher l’ensemble des enregistrements d’une table qui correspondent à plusieurs critères qui peuvent être exprimés à l’aide de plages d’index.</span><span class="sxs-lookup"><span data-stu-id="f8bfc-105">This operation is useful for finding the set of records in a table that match two or more criteria that can be expressed using index ranges.</span></span> <span data-ttu-id="f8bfc-106">Consultez également [IntersectIndexes (JET_SESID, \[ \] )](./api.intersectindexes-method.md).</span><span class="sxs-lookup"><span data-stu-id="f8bfc-106">Also see [IntersectIndexes(JET_SESID, \[\])](./api.intersectindexes-method.md).</span></span>

<span data-ttu-id="f8bfc-107">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f8bfc-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f8bfc-108">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f8bfc-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f8bfc-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8bfc-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetIntersectIndexes ( _
    sesid As JET_SESID, _
    ranges As JET_INDEXRANGE(), _
    numRanges As Integer, _
    <OutAttribute> ByRef recordlist As JET_RECORDLIST, _
    grbit As IntersectIndexesGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim ranges As JET_INDEXRANGE()
Dim numRanges As Integer
Dim recordlist As JET_RECORDLIST
Dim grbit As IntersectIndexesGrbitApi.JetIntersectIndexes(sesid, _
    ranges, numRanges, recordlist, grbit)
```

``` csharp
public static void JetIntersectIndexes(
    JET_SESID sesid,
    JET_INDEXRANGE[] ranges,
    int numRanges,
    out JET_RECORDLIST recordlist,
    IntersectIndexesGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="f8bfc-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8bfc-110">Parameters</span></span>

  - <span data-ttu-id="f8bfc-111">sesid</span><span class="sxs-lookup"><span data-stu-id="f8bfc-111">sesid</span></span>  
    <span data-ttu-id="f8bfc-112">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f8bfc-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f8bfc-113">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="f8bfc-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f8bfc-114">ranges</span><span class="sxs-lookup"><span data-stu-id="f8bfc-114">ranges</span></span>  
    <span data-ttu-id="f8bfc-115">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="f8bfc-115">Type: \[\]</span></span>  
    
    <span data-ttu-id="f8bfc-116">Une plage d’index à croiser.</span><span class="sxs-lookup"><span data-stu-id="f8bfc-116">An the index ranges to intersect.</span></span> <span data-ttu-id="f8bfc-117">Les TableID des plages doivent avoir des plages d’index définies.</span><span class="sxs-lookup"><span data-stu-id="f8bfc-117">The tableids in the ranges must have index ranges set on them.</span></span> <span data-ttu-id="f8bfc-118">Utilisez [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) pour créer une plage d’index.</span><span class="sxs-lookup"><span data-stu-id="f8bfc-118">Use [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) to create an index range.</span></span>

<!-- end list -->

  - <span data-ttu-id="f8bfc-119">numRanges</span><span class="sxs-lookup"><span data-stu-id="f8bfc-119">numRanges</span></span>  
    <span data-ttu-id="f8bfc-120">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="f8bfc-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="f8bfc-121">Nombre de plages d’index.</span><span class="sxs-lookup"><span data-stu-id="f8bfc-121">The number of index ranges.</span></span>

<!-- end list -->

  - <span data-ttu-id="f8bfc-122">recordlist</span><span class="sxs-lookup"><span data-stu-id="f8bfc-122">recordlist</span></span>  
    <span data-ttu-id="f8bfc-123">Type : [Microsoft.ISAM.esent.Interop.JET_RECORDLIST](./jet-recordlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="f8bfc-123">Type: [Microsoft.Isam.Esent.Interop.JET_RECORDLIST](./jet-recordlist-class.md)</span></span>  
    
    <span data-ttu-id="f8bfc-124">Retourne des informations sur la table temporaire contenant les résultats de l’intersection.</span><span class="sxs-lookup"><span data-stu-id="f8bfc-124">Returns information about the temporary table containing the intersection results.</span></span>

<!-- end list -->

  - <span data-ttu-id="f8bfc-125">grbit</span><span class="sxs-lookup"><span data-stu-id="f8bfc-125">grbit</span></span>  
    <span data-ttu-id="f8bfc-126">Type : [Microsoft. ISAM. esent. Interop. IntersectIndexesGrbit](./intersectindexesgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="f8bfc-126">Type: [Microsoft.Isam.Esent.Interop.IntersectIndexesGrbit](./intersectindexesgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="f8bfc-127">Options d’intersection.</span><span class="sxs-lookup"><span data-stu-id="f8bfc-127">Intersection options.</span></span>

## <a name="see-also"></a><span data-ttu-id="f8bfc-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8bfc-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f8bfc-129">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="f8bfc-129">Reference</span></span>

[<span data-ttu-id="f8bfc-130">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="f8bfc-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f8bfc-131">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="f8bfc-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f8bfc-132">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f8bfc-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
