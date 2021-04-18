---
description: 'En savoir plus sur : méthode API. RetrieveColumnAsUInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Méthode API. RetrieveColumnAsUInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsUInt32 method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt32(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasuint32(v=EXCHG.10)
ms:contentKeyID: 55100903
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt32
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b889245cd2e2f37907a15e3ec31b04a4d932dd02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524719"
---
# <a name="apiretrievecolumnasuint32-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="283ea-103">Méthode API. RetrieveColumnAsUInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="283ea-103">Api.RetrieveColumnAsUInt32 method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="283ea-104">Récupère une valeur de colonne UInt32 de l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="283ea-104">Retrieves a uint32 column value from the current record.</span></span> <span data-ttu-id="283ea-105">L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</span><span class="sxs-lookup"><span data-stu-id="283ea-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="283ea-106">Cette API n’est pas conforme CLS.</span><span class="sxs-lookup"><span data-stu-id="283ea-106">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="283ea-107">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="283ea-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="283ea-108">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="283ea-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="283ea-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="283ea-109">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function RetrieveColumnAsUInt32 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of UInteger)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of UInteger)

returnValue = Api.RetrieveColumnAsUInt32(sesid, _
    tableid, columnid)
```

``` csharp
[CLSCompliantAttribute(false)]
public static Nullable<uint> RetrieveColumnAsUInt32(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="283ea-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="283ea-110">Parameters</span></span>

  - <span data-ttu-id="283ea-111">sesid</span><span class="sxs-lookup"><span data-stu-id="283ea-111">sesid</span></span>  
    <span data-ttu-id="283ea-112">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="283ea-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="283ea-113">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="283ea-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="283ea-114">TableID</span><span class="sxs-lookup"><span data-stu-id="283ea-114">tableid</span></span>  
    <span data-ttu-id="283ea-115">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="283ea-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="283ea-116">Curseur à partir duquel récupérer la colonne.</span><span class="sxs-lookup"><span data-stu-id="283ea-116">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="283ea-117">columnid</span><span class="sxs-lookup"><span data-stu-id="283ea-117">columnid</span></span>  
    <span data-ttu-id="283ea-118">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="283ea-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="283ea-119">ColumnID à récupérer.</span><span class="sxs-lookup"><span data-stu-id="283ea-119">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="283ea-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="283ea-120">Return value</span></span>

<span data-ttu-id="283ea-121">Type : [System. Nullable](/dotnet/api/system.nullable-1)\<[UInt32](/dotnet/api/system.uint32)\></span><span class="sxs-lookup"><span data-stu-id="283ea-121">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[UInt32](/dotnet/api/system.uint32)\></span></span>  
<span data-ttu-id="283ea-122">Données extraites de la colonne sous la forme d’un UInt32.</span><span class="sxs-lookup"><span data-stu-id="283ea-122">The data retrieved from the column as an UInt32.</span></span> <span data-ttu-id="283ea-123">NULL si la colonne est null.</span><span class="sxs-lookup"><span data-stu-id="283ea-123">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="283ea-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="283ea-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="283ea-125">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="283ea-125">Reference</span></span>

[<span data-ttu-id="283ea-126">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="283ea-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="283ea-127">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="283ea-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="283ea-128">Surcharge RetrieveColumnAsUInt32</span><span class="sxs-lookup"><span data-stu-id="283ea-128">RetrieveColumnAsUInt32 overload</span></span>](./api.retrievecolumnasuint32-method.md)

[<span data-ttu-id="283ea-129">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="283ea-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
