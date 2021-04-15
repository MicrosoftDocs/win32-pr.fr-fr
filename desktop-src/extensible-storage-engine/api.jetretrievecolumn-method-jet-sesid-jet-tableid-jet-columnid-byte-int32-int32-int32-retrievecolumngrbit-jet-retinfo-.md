---
description: 'En savoir plus sur : méthode API. JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)'
title: Méthode API. JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)
TOCTitle: JetRetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit,Microsoft.Isam.Esent.Interop.JET_RETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100792
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 832e6d6cc123e4a85a2cacb2df688348732fcc0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320817"
---
# <a name="apijetretrievecolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--int32-int32-int32-retrievecolumngrbit-jet_retinfo"></a><span data-ttu-id="268d5-103">Méthode API. JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</span><span class="sxs-lookup"><span data-stu-id="268d5-103">Api.JetRetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</span></span>

<span data-ttu-id="268d5-104">Récupère une valeur de colonne unique à partir de l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="268d5-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="268d5-105">L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</span><span class="sxs-lookup"><span data-stu-id="268d5-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="268d5-106">Cette fonction peut également récupérer une colonne d’un enregistrement en cours de création dans le tampon de copie de curseur.</span><span class="sxs-lookup"><span data-stu-id="268d5-106">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="268d5-107">Cette fonction peut également récupérer des données de colonne à partir d’une entrée d’index qui fait référence à l’enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="268d5-107">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="268d5-108">En plus de récupérer la valeur réelle de la colonne, JetRetrieveColumn peut également être utilisé pour récupérer la taille d’une colonne, avant de récupérer les données de la colonne elle-même afin que les tampons d’application puissent être dimensionnés de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="268d5-108">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span>

<span data-ttu-id="268d5-109">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="268d5-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="268d5-110">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="268d5-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="268d5-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="268d5-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetRetrieveColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    dataSize As Integer, _
    dataOffset As Integer, _
    <OutAttribute> ByRef actualDataSize As Integer, _
    grbit As RetrieveColumnGrbit, _
    retinfo As JET_RETINFO _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As Byte()
Dim dataSize As Integer
Dim dataOffset As Integer
Dim actualDataSize As Integer
Dim grbit As RetrieveColumnGrbit
Dim retinfo As JET_RETINFO
Dim returnValue As JET_wrn

returnValue = Api.JetRetrieveColumn(sesid, _
    tableid, columnid, data, dataSize, _
    dataOffset, actualDataSize, grbit, _
    retinfo)
```

``` csharp
public static JET_wrn JetRetrieveColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    int dataSize,
    int dataOffset,
    out int actualDataSize,
    RetrieveColumnGrbit grbit,
    JET_RETINFO retinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="268d5-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="268d5-112">Parameters</span></span>

  - <span data-ttu-id="268d5-113">sesid</span><span class="sxs-lookup"><span data-stu-id="268d5-113">sesid</span></span>  
    <span data-ttu-id="268d5-114">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="268d5-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="268d5-115">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="268d5-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="268d5-116">TableID</span><span class="sxs-lookup"><span data-stu-id="268d5-116">tableid</span></span>  
    <span data-ttu-id="268d5-117">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="268d5-117">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="268d5-118">Curseur à partir duquel récupérer la colonne.</span><span class="sxs-lookup"><span data-stu-id="268d5-118">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="268d5-119">columnid</span><span class="sxs-lookup"><span data-stu-id="268d5-119">columnid</span></span>  
    <span data-ttu-id="268d5-120">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="268d5-120">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="268d5-121">ColumnID à récupérer.</span><span class="sxs-lookup"><span data-stu-id="268d5-121">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="268d5-122">data</span><span class="sxs-lookup"><span data-stu-id="268d5-122">data</span></span>  
    <span data-ttu-id="268d5-123">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="268d5-123">Type: \[\]</span></span>  
    
    <span data-ttu-id="268d5-124">Mémoire tampon de données à récupérer dans.</span><span class="sxs-lookup"><span data-stu-id="268d5-124">The data buffer to be retrieved into.</span></span>

<!-- end list -->

  - <span data-ttu-id="268d5-125">dataSize</span><span class="sxs-lookup"><span data-stu-id="268d5-125">dataSize</span></span>  
    <span data-ttu-id="268d5-126">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="268d5-126">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="268d5-127">Taille de la mémoire tampon de données.</span><span class="sxs-lookup"><span data-stu-id="268d5-127">The size of the data buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="268d5-128">dataOffset</span><span class="sxs-lookup"><span data-stu-id="268d5-128">dataOffset</span></span>  
    <span data-ttu-id="268d5-129">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="268d5-129">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="268d5-130">Offset dans la mémoire tampon de données dans laquelle lire les données.</span><span class="sxs-lookup"><span data-stu-id="268d5-130">Offset into the data buffer to read data into.</span></span>

<!-- end list -->

  - <span data-ttu-id="268d5-131">actualDataSize</span><span class="sxs-lookup"><span data-stu-id="268d5-131">actualDataSize</span></span>  
    <span data-ttu-id="268d5-132">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="268d5-132">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="268d5-133">Retourne la taille réelle de la mémoire tampon de données.</span><span class="sxs-lookup"><span data-stu-id="268d5-133">Returns the actual size of the data buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="268d5-134">grbit</span><span class="sxs-lookup"><span data-stu-id="268d5-134">grbit</span></span>  
    <span data-ttu-id="268d5-135">Type : [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="268d5-135">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="268d5-136">Récupérez les options de colonne.</span><span class="sxs-lookup"><span data-stu-id="268d5-136">Retrieve column options.</span></span>

<!-- end list -->

  - <span data-ttu-id="268d5-137">retinfo</span><span class="sxs-lookup"><span data-stu-id="268d5-137">retinfo</span></span>  
    <span data-ttu-id="268d5-138">Type : [Microsoft.ISAM.esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="268d5-138">Type: [Microsoft.Isam.Esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span></span>  
    
    <span data-ttu-id="268d5-139">Si pretinfo a la valeur NULL, la fonction se comporte comme si un itagSequence de 1 et un ibLongValue de 0 (zéro) ont été donnés.</span><span class="sxs-lookup"><span data-stu-id="268d5-139">If pretinfo is give as NULL then the function behaves as though an itagSequence of 1 and an ibLongValue of 0 (zero) were given.</span></span> <span data-ttu-id="268d5-140">Ainsi, la récupération de colonne récupère la première valeur d’une colonne à valeurs multiples et récupère les données de type long à l’offset 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="268d5-140">This causes column retrieval to retrieve the first value of a multi-valued column, and to retrieve long data at offset 0 (zero).</span></span>

#### <a name="return-value"></a><span data-ttu-id="268d5-141">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="268d5-141">Return value</span></span>

<span data-ttu-id="268d5-142">Type : [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="268d5-142">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="268d5-143">Code d’avertissement ESENT.</span><span class="sxs-lookup"><span data-stu-id="268d5-143">An ESENT warning code.</span></span>  

## <a name="remarks"></a><span data-ttu-id="268d5-144">Notes</span><span class="sxs-lookup"><span data-stu-id="268d5-144">Remarks</span></span>

<span data-ttu-id="268d5-145">Il s’agit d’une méthode interne qui prend un décalage de mémoire tampon et une taille.</span><span class="sxs-lookup"><span data-stu-id="268d5-145">This is an internal method that takes a buffer offset as well as size.</span></span>

## <a name="see-also"></a><span data-ttu-id="268d5-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="268d5-146">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="268d5-147">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="268d5-147">Reference</span></span>

[<span data-ttu-id="268d5-148">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="268d5-148">Api class</span></span>](./api-class.md)

[<span data-ttu-id="268d5-149">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="268d5-149">Api members</span></span>](./api-members.md)

[<span data-ttu-id="268d5-150">Surcharge JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="268d5-150">JetRetrieveColumn overload</span></span>](./api.jetretrievecolumn-method.md)

[<span data-ttu-id="268d5-151">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="268d5-151">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
