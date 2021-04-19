---
description: 'En savoir plus sur : méthode API. RetrieveColumnAsString (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Méthode API. RetrieveColumnAsString (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsString method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsString(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasstring(v=EXCHG.10)
ms:contentKeyID: 55100860
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
ms.openlocfilehash: 64500e9827d55fab4771963b95dbfd0efffdc5c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521161"
---
# <a name="apiretrievecolumnasstring-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="d2fe6-103">Méthode API. RetrieveColumnAsString (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="d2fe6-103">Api.RetrieveColumnAsString method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="d2fe6-104">Récupère une valeur de colonne unique à partir de l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="d2fe6-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="d2fe6-105">L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</span><span class="sxs-lookup"><span data-stu-id="d2fe6-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="d2fe6-106">L’encodage Unicode est utilisé.</span><span class="sxs-lookup"><span data-stu-id="d2fe6-106">The Unicode encoding is used.</span></span>

<span data-ttu-id="d2fe6-107">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d2fe6-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d2fe6-108">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d2fe6-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d2fe6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2fe6-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsString ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As String
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As String

returnValue = Api.RetrieveColumnAsString(sesid, _
    tableid, columnid)
```

``` csharp
public static string RetrieveColumnAsString(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="d2fe6-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2fe6-110">Parameters</span></span>

  - <span data-ttu-id="d2fe6-111">sesid</span><span class="sxs-lookup"><span data-stu-id="d2fe6-111">sesid</span></span>  
    <span data-ttu-id="d2fe6-112">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d2fe6-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d2fe6-113">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="d2fe6-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d2fe6-114">TableID</span><span class="sxs-lookup"><span data-stu-id="d2fe6-114">tableid</span></span>  
    <span data-ttu-id="d2fe6-115">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d2fe6-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="d2fe6-116">Curseur à partir duquel récupérer la colonne.</span><span class="sxs-lookup"><span data-stu-id="d2fe6-116">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="d2fe6-117">columnid</span><span class="sxs-lookup"><span data-stu-id="d2fe6-117">columnid</span></span>  
    <span data-ttu-id="d2fe6-118">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d2fe6-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="d2fe6-119">ColumnID à récupérer.</span><span class="sxs-lookup"><span data-stu-id="d2fe6-119">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d2fe6-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d2fe6-120">Return value</span></span>

<span data-ttu-id="d2fe6-121">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="d2fe6-121">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="d2fe6-122">Données extraites de la colonne sous la forme d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="d2fe6-122">The data retrieved from the column as a string.</span></span> <span data-ttu-id="d2fe6-123">NULL si la colonne est null.</span><span class="sxs-lookup"><span data-stu-id="d2fe6-123">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d2fe6-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2fe6-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d2fe6-125">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="d2fe6-125">Reference</span></span>

[<span data-ttu-id="d2fe6-126">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="d2fe6-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d2fe6-127">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="d2fe6-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d2fe6-128">Surcharge RetrieveColumnAsString</span><span class="sxs-lookup"><span data-stu-id="d2fe6-128">RetrieveColumnAsString overload</span></span>](./api.retrievecolumnasstring-method.md)

[<span data-ttu-id="d2fe6-129">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d2fe6-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
