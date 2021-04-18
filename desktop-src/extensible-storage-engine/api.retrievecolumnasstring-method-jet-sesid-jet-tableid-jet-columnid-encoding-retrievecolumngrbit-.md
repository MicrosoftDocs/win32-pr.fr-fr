---
description: 'En savoir plus sur : méthode API. RetrieveColumnAsString (JET_SESID, JET_TABLEID, JET_COLUMNID, encodage, RetrieveColumnGrbit)'
title: Méthode API. RetrieveColumnAsString (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding, RetrieveColumnGrbit)
TOCTitle: RetrieveColumnAsString method (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsString(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Text.Encoding,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasstring(v=EXCHG.10)
ms:contentKeyID: 55100862
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2008726577bac37e129a887af2d8b1747323c81c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523076"
---
# <a name="apiretrievecolumnasstring-method-jet_sesid-jet_tableid-jet_columnid-encoding-retrievecolumngrbit"></a><span data-ttu-id="e4b0e-103">Méthode API. RetrieveColumnAsString (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding, RetrieveColumnGrbit)</span><span class="sxs-lookup"><span data-stu-id="e4b0e-103">Api.RetrieveColumnAsString method (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="e4b0e-104">Récupère une valeur de colonne de type chaîne à partir de l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="e4b0e-104">Retrieves a string column value from the current record.</span></span> <span data-ttu-id="e4b0e-105">L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</span><span class="sxs-lookup"><span data-stu-id="e4b0e-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="e4b0e-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e4b0e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e4b0e-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e4b0e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e4b0e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4b0e-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsString ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    encoding As Encoding, _
    grbit As RetrieveColumnGrbit _
) As String
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim encoding As Encoding
Dim grbit As RetrieveColumnGrbit
Dim returnValue As String

returnValue = Api.RetrieveColumnAsString(sesid, _
    tableid, columnid, encoding, grbit)
```

``` csharp
public static string RetrieveColumnAsString(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    Encoding encoding,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="e4b0e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4b0e-109">Parameters</span></span>

  - <span data-ttu-id="e4b0e-110">sesid</span><span class="sxs-lookup"><span data-stu-id="e4b0e-110">sesid</span></span>  
    <span data-ttu-id="e4b0e-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e4b0e-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e4b0e-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="e4b0e-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e4b0e-113">TableID</span><span class="sxs-lookup"><span data-stu-id="e4b0e-113">tableid</span></span>  
    <span data-ttu-id="e4b0e-114">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e4b0e-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e4b0e-115">Curseur à partir duquel récupérer la colonne.</span><span class="sxs-lookup"><span data-stu-id="e4b0e-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="e4b0e-116">columnid</span><span class="sxs-lookup"><span data-stu-id="e4b0e-116">columnid</span></span>  
    <span data-ttu-id="e4b0e-117">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e4b0e-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="e4b0e-118">ColumnID à récupérer.</span><span class="sxs-lookup"><span data-stu-id="e4b0e-118">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="e4b0e-119">encodage</span><span class="sxs-lookup"><span data-stu-id="e4b0e-119">encoding</span></span>  
    <span data-ttu-id="e4b0e-120">Type : [System. Text. Encoding](/dotnet/api/system.text.encoding)</span><span class="sxs-lookup"><span data-stu-id="e4b0e-120">Type: [System.Text.Encoding](/dotnet/api/system.text.encoding)</span></span>  
    
    <span data-ttu-id="e4b0e-121">Encodage de chaîne à utiliser lors de la conversion de données.</span><span class="sxs-lookup"><span data-stu-id="e4b0e-121">The string encoding to use when converting data.</span></span>

<!-- end list -->

  - <span data-ttu-id="e4b0e-122">grbit</span><span class="sxs-lookup"><span data-stu-id="e4b0e-122">grbit</span></span>  
    <span data-ttu-id="e4b0e-123">Type : [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e4b0e-123">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="e4b0e-124">Options de récupération.</span><span class="sxs-lookup"><span data-stu-id="e4b0e-124">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="e4b0e-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e4b0e-125">Return value</span></span>

<span data-ttu-id="e4b0e-126">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="e4b0e-126">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="e4b0e-127">Données extraites de la colonne sous la forme d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="e4b0e-127">The data retrieved from the column as a string.</span></span> <span data-ttu-id="e4b0e-128">NULL si la colonne est null.</span><span class="sxs-lookup"><span data-stu-id="e4b0e-128">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e4b0e-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4b0e-129">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e4b0e-130">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="e4b0e-130">Reference</span></span>

[<span data-ttu-id="e4b0e-131">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="e4b0e-131">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e4b0e-132">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="e4b0e-132">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e4b0e-133">Surcharge RetrieveColumnAsString</span><span class="sxs-lookup"><span data-stu-id="e4b0e-133">RetrieveColumnAsString overload</span></span>](./api.retrievecolumnasstring-method.md)

[<span data-ttu-id="e4b0e-134">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e4b0e-134">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
