---
description: 'En savoir plus sur : méthode API. JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)'
title: Méthode API. JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)
TOCTitle: JetRetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit,Microsoft.Isam.Esent.Interop.JET_RETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100790
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d417e188c72914f871df4b46dede204f6633a8b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514157"
---
# <a name="apijetretrievecolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--int32-int32-retrievecolumngrbit-jet_retinfo"></a><span data-ttu-id="ae1b6-103">Méthode API. JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</span><span class="sxs-lookup"><span data-stu-id="ae1b6-103">Api.JetRetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</span></span>

<span data-ttu-id="ae1b6-104">Récupère une valeur de colonne unique à partir de l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="ae1b6-105">L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="ae1b6-106">Cette fonction peut également récupérer une colonne d’un enregistrement en cours de création dans le tampon de copie de curseur.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-106">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="ae1b6-107">Cette fonction peut également récupérer des données de colonne à partir d’une entrée d’index qui fait référence à l’enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-107">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="ae1b6-108">En plus de récupérer la valeur réelle de la colonne, JetRetrieveColumn peut également être utilisé pour récupérer la taille d’une colonne, avant de récupérer les données de la colonne elle-même afin que les tampons d’application puissent être dimensionnés de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-108">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span>

<span data-ttu-id="ae1b6-109">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ae1b6-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ae1b6-110">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ae1b6-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ae1b6-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae1b6-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetRetrieveColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    dataSize As Integer, _
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
Dim actualDataSize As Integer
Dim grbit As RetrieveColumnGrbit
Dim retinfo As JET_RETINFO
Dim returnValue As JET_wrn

returnValue = Api.JetRetrieveColumn(sesid, _
    tableid, columnid, data, dataSize, _
    actualDataSize, grbit, retinfo)
```

``` csharp
public static JET_wrn JetRetrieveColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    int dataSize,
    out int actualDataSize,
    RetrieveColumnGrbit grbit,
    JET_RETINFO retinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="ae1b6-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae1b6-112">Parameters</span></span>

  - <span data-ttu-id="ae1b6-113">sesid</span><span class="sxs-lookup"><span data-stu-id="ae1b6-113">sesid</span></span>  
    <span data-ttu-id="ae1b6-114">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ae1b6-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ae1b6-115">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="ae1b6-116">TableID</span><span class="sxs-lookup"><span data-stu-id="ae1b6-116">tableid</span></span>  
    <span data-ttu-id="ae1b6-117">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ae1b6-117">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="ae1b6-118">Curseur à partir duquel récupérer la colonne.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-118">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="ae1b6-119">columnid</span><span class="sxs-lookup"><span data-stu-id="ae1b6-119">columnid</span></span>  
    <span data-ttu-id="ae1b6-120">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ae1b6-120">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="ae1b6-121">ColumnID à récupérer.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-121">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="ae1b6-122">data</span><span class="sxs-lookup"><span data-stu-id="ae1b6-122">data</span></span>  
    <span data-ttu-id="ae1b6-123">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="ae1b6-123">Type: \[\]</span></span>  
    
    <span data-ttu-id="ae1b6-124">Mémoire tampon de données à récupérer dans.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-124">The data buffer to be retrieved into.</span></span>

<!-- end list -->

  - <span data-ttu-id="ae1b6-125">dataSize</span><span class="sxs-lookup"><span data-stu-id="ae1b6-125">dataSize</span></span>  
    <span data-ttu-id="ae1b6-126">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="ae1b6-126">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="ae1b6-127">Taille de la mémoire tampon de données.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-127">The size of the data buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="ae1b6-128">actualDataSize</span><span class="sxs-lookup"><span data-stu-id="ae1b6-128">actualDataSize</span></span>  
    <span data-ttu-id="ae1b6-129">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="ae1b6-129">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="ae1b6-130">Retourne la taille réelle de la mémoire tampon de données.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-130">Returns the actual size of the data buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="ae1b6-131">grbit</span><span class="sxs-lookup"><span data-stu-id="ae1b6-131">grbit</span></span>  
    <span data-ttu-id="ae1b6-132">Type : [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="ae1b6-132">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="ae1b6-133">Récupérez les options de colonne.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-133">Retrieve column options.</span></span>

<!-- end list -->

  - <span data-ttu-id="ae1b6-134">retinfo</span><span class="sxs-lookup"><span data-stu-id="ae1b6-134">retinfo</span></span>  
    <span data-ttu-id="ae1b6-135">Type : [Microsoft.ISAM.esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="ae1b6-135">Type: [Microsoft.Isam.Esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span></span>  
    
    <span data-ttu-id="ae1b6-136">Si pretinfo a la valeur NULL, la fonction se comporte comme si un itagSequence de 1 et un ibLongValue de 0 (zéro) ont été donnés.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-136">If pretinfo is give as NULL then the function behaves as though an itagSequence of 1 and an ibLongValue of 0 (zero) were given.</span></span> <span data-ttu-id="ae1b6-137">Ainsi, la récupération de colonne récupère la première valeur d’une colonne à valeurs multiples et récupère les données de type long à l’offset 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="ae1b6-137">This causes column retrieval to retrieve the first value of a multi-valued column, and to retrieve long data at offset 0 (zero).</span></span>

#### <a name="return-value"></a><span data-ttu-id="ae1b6-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ae1b6-138">Return value</span></span>

<span data-ttu-id="ae1b6-139">Type : [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="ae1b6-139">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="ae1b6-140">Code d’avertissement ESENT.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-140">An ESENT warning code.</span></span>  

## <a name="remarks"></a><span data-ttu-id="ae1b6-141">Notes</span><span class="sxs-lookup"><span data-stu-id="ae1b6-141">Remarks</span></span>

<span data-ttu-id="ae1b6-142">Les fonctions RetrieveColumnAs fournissent des fonctions de récupération spécifiques au type de données.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-142">The RetrieveColumnAs functions provide datatype-specific retrieval functions.</span></span>

## <a name="see-also"></a><span data-ttu-id="ae1b6-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae1b6-143">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ae1b6-144">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="ae1b6-144">Reference</span></span>

[<span data-ttu-id="ae1b6-145">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="ae1b6-145">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ae1b6-146">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="ae1b6-146">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ae1b6-147">Surcharge JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="ae1b6-147">JetRetrieveColumn overload</span></span>](./api.jetretrievecolumn-method.md)

[<span data-ttu-id="ae1b6-148">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ae1b6-148">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
