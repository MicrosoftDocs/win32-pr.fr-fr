---
description: 'En savoir plus sur : méthode API. RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)'
title: Méthode API. RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)
TOCTitle: RetrieveColumnSize method (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnSize(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Int32,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnsize(v=EXCHG.10)
ms:contentKeyID: 55100912
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: afd09ecca0362487d6c8e78f8e7c8d943f2f3269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950911"
---
# <a name="apiretrievecolumnsize-method-jet_sesid-jet_tableid-jet_columnid-int32-retrievecolumngrbit"></a><span data-ttu-id="20fa1-103">Méthode API. RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)</span><span class="sxs-lookup"><span data-stu-id="20fa1-103">Api.RetrieveColumnSize method (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="20fa1-104">Récupère la taille d’une valeur de colonne unique à partir de l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="20fa1-104">Retrieves the size of a single column value from the current record.</span></span> <span data-ttu-id="20fa1-105">L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</span><span class="sxs-lookup"><span data-stu-id="20fa1-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="20fa1-106">Cette fonction peut également récupérer une colonne d’un enregistrement en cours de création dans le tampon de copie de curseur.</span><span class="sxs-lookup"><span data-stu-id="20fa1-106">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="20fa1-107">Cette fonction peut également récupérer des données de colonne à partir d’une entrée d’index qui fait référence à l’enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="20fa1-107">This function can also retrieve column data from an index entry that references the current record.</span></span>

<span data-ttu-id="20fa1-108">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="20fa1-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="20fa1-109">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="20fa1-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="20fa1-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20fa1-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnSize ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    itagSequence As Integer, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of Integer)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim itagSequence As Integer
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of Integer)

returnValue = Api.RetrieveColumnSize(sesid, _
    tableid, columnid, itagSequence, _
    grbit)
```

``` csharp
public static Nullable<int> RetrieveColumnSize(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    int itagSequence,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="20fa1-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20fa1-111">Parameters</span></span>

  - <span data-ttu-id="20fa1-112">sesid</span><span class="sxs-lookup"><span data-stu-id="20fa1-112">sesid</span></span>  
    <span data-ttu-id="20fa1-113">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="20fa1-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="20fa1-114">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="20fa1-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="20fa1-115">TableID</span><span class="sxs-lookup"><span data-stu-id="20fa1-115">tableid</span></span>  
    <span data-ttu-id="20fa1-116">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="20fa1-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="20fa1-117">Curseur à partir duquel récupérer la colonne.</span><span class="sxs-lookup"><span data-stu-id="20fa1-117">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="20fa1-118">columnid</span><span class="sxs-lookup"><span data-stu-id="20fa1-118">columnid</span></span>  
    <span data-ttu-id="20fa1-119">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="20fa1-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="20fa1-120">ColumnID à récupérer.</span><span class="sxs-lookup"><span data-stu-id="20fa1-120">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="20fa1-121">itagSequence</span><span class="sxs-lookup"><span data-stu-id="20fa1-121">itagSequence</span></span>  
    <span data-ttu-id="20fa1-122">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="20fa1-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="20fa1-123">Numéro de séquence de la valeur dans une colonne à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="20fa1-123">The sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="20fa1-124">Le tableau de valeurs est de base un.</span><span class="sxs-lookup"><span data-stu-id="20fa1-124">The array of values is one-based.</span></span> <span data-ttu-id="20fa1-125">La première valeur est séquence 1, et non 0.</span><span class="sxs-lookup"><span data-stu-id="20fa1-125">The first value is sequence 1, not 0.</span></span> <span data-ttu-id="20fa1-126">Si la colonne d’enregistrement n’a qu’une seule valeur, 1 doit être passé en tant que itagSequence.</span><span class="sxs-lookup"><span data-stu-id="20fa1-126">If the record column has only one value then 1 should be passed as the itagSequence.</span></span>

<!-- end list -->

  - <span data-ttu-id="20fa1-127">grbit</span><span class="sxs-lookup"><span data-stu-id="20fa1-127">grbit</span></span>  
    <span data-ttu-id="20fa1-128">Type : [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="20fa1-128">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="20fa1-129">Récupérez les options de colonne.</span><span class="sxs-lookup"><span data-stu-id="20fa1-129">Retrieve column options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20fa1-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="20fa1-130">Return value</span></span>

<span data-ttu-id="20fa1-131">Type : [System. Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span><span class="sxs-lookup"><span data-stu-id="20fa1-131">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span></span>  
<span data-ttu-id="20fa1-132">Taille de la colonne.</span><span class="sxs-lookup"><span data-stu-id="20fa1-132">The size of the column.</span></span> <span data-ttu-id="20fa1-133">0 si la colonne est null.</span><span class="sxs-lookup"><span data-stu-id="20fa1-133">0 if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="20fa1-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20fa1-134">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="20fa1-135">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="20fa1-135">Reference</span></span>

[<span data-ttu-id="20fa1-136">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="20fa1-136">Api class</span></span>](./api-class.md)

[<span data-ttu-id="20fa1-137">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="20fa1-137">Api members</span></span>](./api-members.md)

[<span data-ttu-id="20fa1-138">Surcharge RetrieveColumnSize</span><span class="sxs-lookup"><span data-stu-id="20fa1-138">RetrieveColumnSize overload</span></span>](./api.retrievecolumnsize-method.md)

[<span data-ttu-id="20fa1-139">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="20fa1-139">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
