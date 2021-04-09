---
description: 'En savoir plus sur : méthode API. RetrieveColumnAsByte (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Méthode API. RetrieveColumnAsByte (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsByte method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsByte(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasbyte(v=EXCHG.10)
ms:contentKeyID: 55100838
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsByte
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e3bc5db8aa14f3cabf05f15f8e1ecb41256496b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953035"
---
# <a name="apiretrievecolumnasbyte-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="e0d32-103">Méthode API. RetrieveColumnAsByte (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="e0d32-103">Api.RetrieveColumnAsByte method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="e0d32-104">Récupère une valeur de colonne d’octets à partir de l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="e0d32-104">Retrieves a byte column value from the current record.</span></span> <span data-ttu-id="e0d32-105">L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</span><span class="sxs-lookup"><span data-stu-id="e0d32-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="e0d32-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e0d32-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e0d32-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e0d32-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e0d32-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e0d32-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsByte ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of Byte)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of Byte)

returnValue = Api.RetrieveColumnAsByte(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<byte> RetrieveColumnAsByte(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="e0d32-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e0d32-109">Parameters</span></span>

  - <span data-ttu-id="e0d32-110">sesid</span><span class="sxs-lookup"><span data-stu-id="e0d32-110">sesid</span></span>  
    <span data-ttu-id="e0d32-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e0d32-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e0d32-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="e0d32-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e0d32-113">TableID</span><span class="sxs-lookup"><span data-stu-id="e0d32-113">tableid</span></span>  
    <span data-ttu-id="e0d32-114">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e0d32-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e0d32-115">Curseur à partir duquel récupérer la colonne.</span><span class="sxs-lookup"><span data-stu-id="e0d32-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="e0d32-116">columnid</span><span class="sxs-lookup"><span data-stu-id="e0d32-116">columnid</span></span>  
    <span data-ttu-id="e0d32-117">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e0d32-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="e0d32-118">ColumnID à récupérer.</span><span class="sxs-lookup"><span data-stu-id="e0d32-118">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="e0d32-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e0d32-119">Return value</span></span>

<span data-ttu-id="e0d32-120">Type : [System. Nullable](/dotnet/api/system.nullable-1)\<[Byte](/dotnet/api/system.byte)\></span><span class="sxs-lookup"><span data-stu-id="e0d32-120">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Byte](/dotnet/api/system.byte)\></span></span>  
<span data-ttu-id="e0d32-121">Données extraites de la colonne sous la forme d’un octet.</span><span class="sxs-lookup"><span data-stu-id="e0d32-121">The data retrieved from the column as a byte.</span></span> <span data-ttu-id="e0d32-122">NULL si la colonne est null.</span><span class="sxs-lookup"><span data-stu-id="e0d32-122">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e0d32-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0d32-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e0d32-124">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="e0d32-124">Reference</span></span>

[<span data-ttu-id="e0d32-125">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="e0d32-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e0d32-126">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="e0d32-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e0d32-127">Surcharge RetrieveColumnAsByte</span><span class="sxs-lookup"><span data-stu-id="e0d32-127">RetrieveColumnAsByte overload</span></span>](./api.retrievecolumnasbyte-method.md)

[<span data-ttu-id="e0d32-128">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e0d32-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
