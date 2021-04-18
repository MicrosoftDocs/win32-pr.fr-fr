---
description: 'En savoir plus sur : méthode API. RetrieveColumnAsDateTime (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)'
title: Méthode API. RetrieveColumnAsDateTime (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
TOCTitle: RetrieveColumnAsDateTime method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsDateTime(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasdatetime(v=EXCHG.10)
ms:contentKeyID: 55100843
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsDateTime
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: befd4e7256c9d1ca52d6f0239f5e56c21842a85d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523034"
---
# <a name="apiretrievecolumnasdatetime-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a><span data-ttu-id="e9553-103">Méthode API. RetrieveColumnAsDateTime (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span><span class="sxs-lookup"><span data-stu-id="e9553-103">Api.RetrieveColumnAsDateTime method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="e9553-104">Récupère une valeur de colonne DateTime à partir de l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="e9553-104">Retrieves a datetime column value from the current record.</span></span> <span data-ttu-id="e9553-105">L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</span><span class="sxs-lookup"><span data-stu-id="e9553-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="e9553-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e9553-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e9553-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e9553-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e9553-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9553-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsDateTime ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of DateTime)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of DateTime)

returnValue = Api.RetrieveColumnAsDateTime(sesid, _
    tableid, columnid, grbit)
```

``` csharp
public static Nullable<DateTime> RetrieveColumnAsDateTime(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="e9553-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9553-109">Parameters</span></span>

  - <span data-ttu-id="e9553-110">sesid</span><span class="sxs-lookup"><span data-stu-id="e9553-110">sesid</span></span>  
    <span data-ttu-id="e9553-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e9553-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e9553-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="e9553-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e9553-113">TableID</span><span class="sxs-lookup"><span data-stu-id="e9553-113">tableid</span></span>  
    <span data-ttu-id="e9553-114">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e9553-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e9553-115">Curseur à partir duquel récupérer la colonne.</span><span class="sxs-lookup"><span data-stu-id="e9553-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="e9553-116">columnid</span><span class="sxs-lookup"><span data-stu-id="e9553-116">columnid</span></span>  
    <span data-ttu-id="e9553-117">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e9553-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="e9553-118">ColumnID à récupérer.</span><span class="sxs-lookup"><span data-stu-id="e9553-118">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="e9553-119">grbit</span><span class="sxs-lookup"><span data-stu-id="e9553-119">grbit</span></span>  
    <span data-ttu-id="e9553-120">Type : [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e9553-120">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="e9553-121">Options de récupération.</span><span class="sxs-lookup"><span data-stu-id="e9553-121">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="e9553-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e9553-122">Return value</span></span>

<span data-ttu-id="e9553-123">Type : [System. Nullable](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\></span><span class="sxs-lookup"><span data-stu-id="e9553-123">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\></span></span>  
<span data-ttu-id="e9553-124">Données extraites de la colonne sous la forme d’une valeur DateTime.</span><span class="sxs-lookup"><span data-stu-id="e9553-124">The data retrieved from the column as a datetime.</span></span> <span data-ttu-id="e9553-125">NULL si la colonne est null.</span><span class="sxs-lookup"><span data-stu-id="e9553-125">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e9553-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9553-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e9553-127">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="e9553-127">Reference</span></span>

[<span data-ttu-id="e9553-128">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="e9553-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e9553-129">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="e9553-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e9553-130">Surcharge RetrieveColumnAsDateTime</span><span class="sxs-lookup"><span data-stu-id="e9553-130">RetrieveColumnAsDateTime overload</span></span>](./api.retrievecolumnasdatetime-method.md)

[<span data-ttu-id="e9553-131">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e9553-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
