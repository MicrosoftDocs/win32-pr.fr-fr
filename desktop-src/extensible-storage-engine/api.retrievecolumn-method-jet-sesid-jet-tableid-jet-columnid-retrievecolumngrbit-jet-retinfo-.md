---
description: 'En savoir plus sur : méthode API. RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)'
title: Méthode API. RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)
TOCTitle: RetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit,Microsoft.Isam.Esent.Interop.JET_RETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100853
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43657ec60e521795ba4d474306de9380618cd21f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515959"
---
# <a name="apiretrievecolumn-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit-jet_retinfo"></a><span data-ttu-id="e1e2a-103">Méthode API. RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)</span><span class="sxs-lookup"><span data-stu-id="e1e2a-103">Api.RetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)</span></span>

<span data-ttu-id="e1e2a-104">Récupère une valeur de colonne unique à partir de l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="e1e2a-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="e1e2a-105">L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</span><span class="sxs-lookup"><span data-stu-id="e1e2a-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="e1e2a-106">Cette fonction peut également récupérer une colonne d’un enregistrement en cours de création dans le tampon de copie de curseur.</span><span class="sxs-lookup"><span data-stu-id="e1e2a-106">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="e1e2a-107">Cette fonction peut également récupérer des données de colonne à partir d’une entrée d’index qui fait référence à l’enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="e1e2a-107">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="e1e2a-108">En plus de récupérer la valeur réelle de la colonne, JetRetrieveColumn peut également être utilisé pour récupérer la taille d’une colonne, avant de récupérer les données de la colonne elle-même afin que les tampons d’application puissent être dimensionnés de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="e1e2a-108">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span>

<span data-ttu-id="e1e2a-109">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e1e2a-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e1e2a-110">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e1e2a-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e1e2a-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1e2a-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit, _
    retinfo As JET_RETINFO _
) As Byte()
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim retinfo As JET_RETINFO
Dim returnValue As Byte()

returnValue = Api.RetrieveColumn(sesid, _
    tableid, columnid, grbit, retinfo)
```

``` csharp
public static byte[] RetrieveColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit,
    JET_RETINFO retinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="e1e2a-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1e2a-112">Parameters</span></span>

  - <span data-ttu-id="e1e2a-113">sesid</span><span class="sxs-lookup"><span data-stu-id="e1e2a-113">sesid</span></span>  
    <span data-ttu-id="e1e2a-114">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e1e2a-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e1e2a-115">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="e1e2a-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e1e2a-116">TableID</span><span class="sxs-lookup"><span data-stu-id="e1e2a-116">tableid</span></span>  
    <span data-ttu-id="e1e2a-117">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e1e2a-117">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e1e2a-118">Curseur à partir duquel récupérer la colonne.</span><span class="sxs-lookup"><span data-stu-id="e1e2a-118">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="e1e2a-119">columnid</span><span class="sxs-lookup"><span data-stu-id="e1e2a-119">columnid</span></span>  
    <span data-ttu-id="e1e2a-120">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e1e2a-120">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="e1e2a-121">ColumnID à récupérer.</span><span class="sxs-lookup"><span data-stu-id="e1e2a-121">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="e1e2a-122">grbit</span><span class="sxs-lookup"><span data-stu-id="e1e2a-122">grbit</span></span>  
    <span data-ttu-id="e1e2a-123">Type : [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e1e2a-123">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="e1e2a-124">Récupérez les options de colonne.</span><span class="sxs-lookup"><span data-stu-id="e1e2a-124">Retrieve column options.</span></span>

<!-- end list -->

  - <span data-ttu-id="e1e2a-125">retinfo</span><span class="sxs-lookup"><span data-stu-id="e1e2a-125">retinfo</span></span>  
    <span data-ttu-id="e1e2a-126">Type : [Microsoft.ISAM.esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="e1e2a-126">Type: [Microsoft.Isam.Esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span></span>  
    
    <span data-ttu-id="e1e2a-127">Si pretinfo a la valeur NULL, la fonction se comporte comme si un itagSequence de 1 et un ibLongValue de 0 (zéro) ont été donnés.</span><span class="sxs-lookup"><span data-stu-id="e1e2a-127">If pretinfo is give as NULL then the function behaves as though an itagSequence of 1 and an ibLongValue of 0 (zero) were given.</span></span> <span data-ttu-id="e1e2a-128">Ainsi, la récupération de colonne récupère la première valeur d’une colonne à valeurs multiples et récupère les données de type long à l’offset 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="e1e2a-128">This causes column retrieval to retrieve the first value of a multi-valued column, and to retrieve long data at offset 0 (zero).</span></span>

#### <a name="return-value"></a><span data-ttu-id="e1e2a-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e1e2a-129">Return value</span></span>

<span data-ttu-id="e1e2a-130">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="e1e2a-130">Type: \[\]</span></span>  
<span data-ttu-id="e1e2a-131">Données extraites de la colonne.</span><span class="sxs-lookup"><span data-stu-id="e1e2a-131">The data retrieved from the column.</span></span> <span data-ttu-id="e1e2a-132">NULL si la colonne est null.</span><span class="sxs-lookup"><span data-stu-id="e1e2a-132">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e1e2a-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1e2a-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e1e2a-134">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="e1e2a-134">Reference</span></span>

[<span data-ttu-id="e1e2a-135">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="e1e2a-135">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e1e2a-136">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="e1e2a-136">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e1e2a-137">Surcharge RetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="e1e2a-137">RetrieveColumn overload</span></span>](./api.retrievecolumn-method.md)

[<span data-ttu-id="e1e2a-138">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e1e2a-138">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
