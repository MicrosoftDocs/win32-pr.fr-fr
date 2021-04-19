---
description: 'En savoir plus sur : méthode API. DeserializeObjectFromColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)'
title: Méthode API. DeserializeObjectFromColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
TOCTitle: DeserializeObjectFromColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.DeserializeObjectFromColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.deserializeobjectfromcolumn(v=EXCHG.10)
ms:contentKeyID: 55100669
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.DeserializeObjectFromColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fe2bb9757216dc4b0a671ae9d5da6cdf4bd5eb7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516600"
---
# <a name="apideserializeobjectfromcolumn-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a><span data-ttu-id="f2f64-103">Méthode API. DeserializeObjectFromColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span><span class="sxs-lookup"><span data-stu-id="f2f64-103">Api.DeserializeObjectFromColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="f2f64-104">Désérialiser un objet à partir d’une colonne.</span><span class="sxs-lookup"><span data-stu-id="f2f64-104">Deserialize an object from a column.</span></span>

<span data-ttu-id="f2f64-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f2f64-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f2f64-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f2f64-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f2f64-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2f64-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function DeserializeObjectFromColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Object
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Object

returnValue = Api.DeserializeObjectFromColumn(sesid, _
    tableid, columnid, grbit)
```

``` csharp
public static Object DeserializeObjectFromColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="f2f64-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2f64-108">Parameters</span></span>

  - <span data-ttu-id="f2f64-109">sesid</span><span class="sxs-lookup"><span data-stu-id="f2f64-109">sesid</span></span>  
    <span data-ttu-id="f2f64-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f2f64-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f2f64-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="f2f64-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f2f64-112">TableID</span><span class="sxs-lookup"><span data-stu-id="f2f64-112">tableid</span></span>  
    <span data-ttu-id="f2f64-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f2f64-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="f2f64-114">Table à partir de laquelle effectuer la lecture.</span><span class="sxs-lookup"><span data-stu-id="f2f64-114">The table to read from.</span></span>

<!-- end list -->

  - <span data-ttu-id="f2f64-115">columnid</span><span class="sxs-lookup"><span data-stu-id="f2f64-115">columnid</span></span>  
    <span data-ttu-id="f2f64-116">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f2f64-116">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="f2f64-117">Colonne à partir de laquelle effectuer la lecture.</span><span class="sxs-lookup"><span data-stu-id="f2f64-117">The column to read from.</span></span>

<!-- end list -->

  - <span data-ttu-id="f2f64-118">grbit</span><span class="sxs-lookup"><span data-stu-id="f2f64-118">grbit</span></span>  
    <span data-ttu-id="f2f64-119">Type : [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="f2f64-119">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="f2f64-120">Options de récupération à utiliser.</span><span class="sxs-lookup"><span data-stu-id="f2f64-120">The retrieval options to use.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f2f64-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f2f64-121">Return value</span></span>

<span data-ttu-id="f2f64-122">Type : [System. Object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="f2f64-122">Type: [System.Object](/dotnet/api/system.object)</span></span>  
<span data-ttu-id="f2f64-123">L'objet désérialisé.</span><span class="sxs-lookup"><span data-stu-id="f2f64-123">The deserialized object.</span></span> <span data-ttu-id="f2f64-124">NULL si la colonne est null.</span><span class="sxs-lookup"><span data-stu-id="f2f64-124">Null if the column was null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f2f64-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2f64-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f2f64-126">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="f2f64-126">Reference</span></span>

[<span data-ttu-id="f2f64-127">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="f2f64-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f2f64-128">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="f2f64-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f2f64-129">Surcharge DeserializeObjectFromColumn</span><span class="sxs-lookup"><span data-stu-id="f2f64-129">DeserializeObjectFromColumn overload</span></span>](./api.deserializeobjectfromcolumn-method.md)

[<span data-ttu-id="f2f64-130">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f2f64-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
