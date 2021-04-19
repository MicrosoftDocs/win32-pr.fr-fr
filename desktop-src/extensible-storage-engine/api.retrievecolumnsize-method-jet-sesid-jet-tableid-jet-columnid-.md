---
description: 'En savoir plus sur : méthode API. RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Méthode API. RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnSize method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnSize(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnsize(v=EXCHG.10)
ms:contentKeyID: 55100868
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
ms.openlocfilehash: 6f75ce51e942cfde7fddc4f9ec0154feae985e02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521979"
---
# <a name="apiretrievecolumnsize-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="cb742-103">Méthode API. RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="cb742-103">Api.RetrieveColumnSize method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="cb742-104">Récupère la taille d’une valeur de colonne unique à partir de l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="cb742-104">Retrieves the size of a single column value from the current record.</span></span> <span data-ttu-id="cb742-105">L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</span><span class="sxs-lookup"><span data-stu-id="cb742-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="cb742-106">Cette fonction peut également récupérer une colonne d’un enregistrement en cours de création dans le tampon de copie de curseur.</span><span class="sxs-lookup"><span data-stu-id="cb742-106">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="cb742-107">Cette fonction peut également récupérer des données de colonne à partir d’une entrée d’index qui fait référence à l’enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="cb742-107">This function can also retrieve column data from an index entry that references the current record.</span></span>

<span data-ttu-id="cb742-108">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cb742-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cb742-109">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cb742-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cb742-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb742-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnSize ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of Integer)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of Integer)

returnValue = Api.RetrieveColumnSize(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<int> RetrieveColumnSize(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="cb742-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cb742-111">Parameters</span></span>

  - <span data-ttu-id="cb742-112">sesid</span><span class="sxs-lookup"><span data-stu-id="cb742-112">sesid</span></span>  
    <span data-ttu-id="cb742-113">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cb742-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="cb742-114">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="cb742-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="cb742-115">TableID</span><span class="sxs-lookup"><span data-stu-id="cb742-115">tableid</span></span>  
    <span data-ttu-id="cb742-116">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cb742-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="cb742-117">Curseur à partir duquel récupérer la colonne.</span><span class="sxs-lookup"><span data-stu-id="cb742-117">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="cb742-118">columnid</span><span class="sxs-lookup"><span data-stu-id="cb742-118">columnid</span></span>  
    <span data-ttu-id="cb742-119">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cb742-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="cb742-120">ColumnID à récupérer.</span><span class="sxs-lookup"><span data-stu-id="cb742-120">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="cb742-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cb742-121">Return value</span></span>

<span data-ttu-id="cb742-122">Type : [System. Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span><span class="sxs-lookup"><span data-stu-id="cb742-122">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span></span>  
<span data-ttu-id="cb742-123">Taille de la colonne.</span><span class="sxs-lookup"><span data-stu-id="cb742-123">The size of the column.</span></span> <span data-ttu-id="cb742-124">0 si la colonne est null.</span><span class="sxs-lookup"><span data-stu-id="cb742-124">0 if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cb742-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb742-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cb742-126">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="cb742-126">Reference</span></span>

[<span data-ttu-id="cb742-127">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="cb742-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="cb742-128">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="cb742-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="cb742-129">Surcharge RetrieveColumnSize</span><span class="sxs-lookup"><span data-stu-id="cb742-129">RetrieveColumnSize overload</span></span>](./api.retrievecolumnsize-method.md)

[<span data-ttu-id="cb742-130">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="cb742-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
