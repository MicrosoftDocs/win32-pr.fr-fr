---
description: 'En savoir plus sur : méthode API. IntersectIndexes'
title: API. IntersectIndexes, méthode
TOCTitle: 'IntersectIndexes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.IntersectIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.intersectindexes(v=EXCHG.10)
ms:contentKeyID: 55107220
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.IntersectIndexes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.IntersectIndexes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8dfe5784ecd5ab517e183f8eeeb5f79315fe585a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524775"
---
# <a name="apiintersectindexes-method"></a><span data-ttu-id="2722b-103">API. IntersectIndexes, méthode</span><span class="sxs-lookup"><span data-stu-id="2722b-103">Api.IntersectIndexes method</span></span>

<span data-ttu-id="2722b-104">Croise un groupe de plages d’index et retourne les signets des enregistrements qui se trouvent dans toutes les plages d’index.</span><span class="sxs-lookup"><span data-stu-id="2722b-104">Intersect a group of index ranges and return the bookmarks of the records which are found in all the index ranges.</span></span> <span data-ttu-id="2722b-105">Consultez également [JetIntersectIndexes (JET_SESID, \[ \] , Int32, JET_RECORDLIST, IntersectIndexesGrbit)](./api.jetintersectindexes-method.md).</span><span class="sxs-lookup"><span data-stu-id="2722b-105">Also see [JetIntersectIndexes(JET_SESID, \[\], Int32, JET_RECORDLIST, IntersectIndexesGrbit)](./api.jetintersectindexes-method.md).</span></span>

<span data-ttu-id="2722b-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2722b-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2722b-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2722b-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2722b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2722b-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function IntersectIndexes ( _
    sesid As JET_SESID, _
    ParamArray tableids As JET_TABLEID() _
) As IEnumerable(Of Byte())
'Usage
Dim sesid As JET_SESID
Dim tableids As JET_TABLEID()
Dim returnValue As IEnumerable(Of Byte())

returnValue = Api.IntersectIndexes(sesid, _
    tableids)
```

``` csharp
public static IEnumerable<byte[]> IntersectIndexes(
    JET_SESID sesid,
    params JET_TABLEID[] tableids
)
```

#### <a name="parameters"></a><span data-ttu-id="2722b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2722b-109">Parameters</span></span>

  - <span data-ttu-id="2722b-110">sesid</span><span class="sxs-lookup"><span data-stu-id="2722b-110">sesid</span></span>  
    <span data-ttu-id="2722b-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2722b-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="2722b-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="2722b-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="2722b-113">ID</span><span class="sxs-lookup"><span data-stu-id="2722b-113">tableids</span></span>  
    <span data-ttu-id="2722b-114">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="2722b-114">Type: \[\]</span></span>  
    
    <span data-ttu-id="2722b-115">TableID à utiliser.</span><span class="sxs-lookup"><span data-stu-id="2722b-115">The tableids to use.</span></span> <span data-ttu-id="2722b-116">Chaque TableID doit provenir d’un index différent sur la même table et avoir une plage d’index active.</span><span class="sxs-lookup"><span data-stu-id="2722b-116">Each tableid must be from a different index on the same table and have an active index range.</span></span> <span data-ttu-id="2722b-117">Utilisez [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) pour créer une plage d’index.</span><span class="sxs-lookup"><span data-stu-id="2722b-117">Use [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) to create an index range.</span></span>

#### <a name="return-value"></a><span data-ttu-id="2722b-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2722b-118">Return value</span></span>

<span data-ttu-id="2722b-119">Type : [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<\[\]\></span><span class="sxs-lookup"><span data-stu-id="2722b-119">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<\[\]\></span></span>  
<span data-ttu-id="2722b-120">Les signets des enregistrements qui se trouvent dans toutes les plages d’index.</span><span class="sxs-lookup"><span data-stu-id="2722b-120">The bookmarks of the records which are found in all the index ranges.</span></span> <span data-ttu-id="2722b-121">Les signets sont retournés dans l’ordre des clés primaires.</span><span class="sxs-lookup"><span data-stu-id="2722b-121">The bookmarks are returned in primary key order.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2722b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2722b-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2722b-123">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="2722b-123">Reference</span></span>

[<span data-ttu-id="2722b-124">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="2722b-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="2722b-125">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="2722b-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="2722b-126">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2722b-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
