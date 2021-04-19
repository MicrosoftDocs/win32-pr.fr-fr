---
description: 'En savoir plus sur : méthode API. RetrieveColumnAsInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)'
title: Méthode API. RetrieveColumnAsInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
TOCTitle: RetrieveColumnAsInt64 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt64(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasint64(v=EXCHG.10)
ms:contentKeyID: 55100891
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt64
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 158e350dc3d85b99b4651c448c8b1b7d51a1ce14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521939"
---
# <a name="apiretrievecolumnasint64-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a><span data-ttu-id="79394-103">Méthode API. RetrieveColumnAsInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span><span class="sxs-lookup"><span data-stu-id="79394-103">Api.RetrieveColumnAsInt64 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="79394-104">Récupère une valeur de colonne unique à partir de l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="79394-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="79394-105">L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</span><span class="sxs-lookup"><span data-stu-id="79394-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="79394-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="79394-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="79394-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="79394-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="79394-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79394-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsInt64 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of Long)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of Long)

returnValue = Api.RetrieveColumnAsInt64(sesid, _
    tableid, columnid, grbit)
```

``` csharp
public static Nullable<long> RetrieveColumnAsInt64(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="79394-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79394-109">Parameters</span></span>

  - <span data-ttu-id="79394-110">sesid</span><span class="sxs-lookup"><span data-stu-id="79394-110">sesid</span></span>  
    <span data-ttu-id="79394-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="79394-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="79394-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="79394-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="79394-113">TableID</span><span class="sxs-lookup"><span data-stu-id="79394-113">tableid</span></span>  
    <span data-ttu-id="79394-114">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="79394-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="79394-115">Curseur à partir duquel récupérer la colonne.</span><span class="sxs-lookup"><span data-stu-id="79394-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="79394-116">columnid</span><span class="sxs-lookup"><span data-stu-id="79394-116">columnid</span></span>  
    <span data-ttu-id="79394-117">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="79394-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="79394-118">ColumnID à récupérer.</span><span class="sxs-lookup"><span data-stu-id="79394-118">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="79394-119">grbit</span><span class="sxs-lookup"><span data-stu-id="79394-119">grbit</span></span>  
    <span data-ttu-id="79394-120">Type : [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="79394-120">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="79394-121">Options de récupération.</span><span class="sxs-lookup"><span data-stu-id="79394-121">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="79394-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="79394-122">Return value</span></span>

<span data-ttu-id="79394-123">Type : [System. Nullable](/dotnet/api/system.nullable-1)\<[Int64](/dotnet/api/system.int64)\></span><span class="sxs-lookup"><span data-stu-id="79394-123">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int64](/dotnet/api/system.int64)\></span></span>  
<span data-ttu-id="79394-124">Données extraites de la colonne sous forme de long.</span><span class="sxs-lookup"><span data-stu-id="79394-124">The data retrieved from the column as a long.</span></span> <span data-ttu-id="79394-125">NULL si la colonne est null.</span><span class="sxs-lookup"><span data-stu-id="79394-125">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="79394-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79394-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="79394-127">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="79394-127">Reference</span></span>

[<span data-ttu-id="79394-128">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="79394-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="79394-129">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="79394-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="79394-130">Surcharge RetrieveColumnAsInt64</span><span class="sxs-lookup"><span data-stu-id="79394-130">RetrieveColumnAsInt64 overload</span></span>](./api.retrievecolumnasint64-method.md)

[<span data-ttu-id="79394-131">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="79394-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
