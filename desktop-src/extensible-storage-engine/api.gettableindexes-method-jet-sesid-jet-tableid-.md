---
description: 'En savoir plus sur : méthode API. GetTableIndexes (JET_SESID, JET_TABLEID)'
title: Méthode API. GetTableIndexes (JET_SESID, JET_TABLEID)
TOCTitle: GetTableIndexes method (JET_SESID, JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettableindexes(v=EXCHG.10)
ms:contentKeyID: 55107219
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetTableIndexes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8708f285445b13ecb1c9d2cb306ec14c7976905b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544635"
---
# <a name="apigettableindexes-method-jet_sesid-jet_tableid"></a><span data-ttu-id="d1a87-103">Méthode API. GetTableIndexes (JET_SESID, JET_TABLEID)</span><span class="sxs-lookup"><span data-stu-id="d1a87-103">Api.GetTableIndexes method (JET_SESID, JET_TABLEID)</span></span>

<span data-ttu-id="d1a87-104">Itère sur tous les index de la table, en retournant des informations sur chacune d’elles.</span><span class="sxs-lookup"><span data-stu-id="d1a87-104">Iterates over all the indexes in the table, returning information about each one.</span></span>

<span data-ttu-id="d1a87-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d1a87-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d1a87-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d1a87-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d1a87-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1a87-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetTableIndexes ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As IEnumerable(Of IndexInfo)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As IEnumerable(Of IndexInfo)

returnValue = Api.GetTableIndexes(sesid, _
    tableid)
```

``` csharp
public static IEnumerable<IndexInfo> GetTableIndexes(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="d1a87-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1a87-108">Parameters</span></span>

  - <span data-ttu-id="d1a87-109">sesid</span><span class="sxs-lookup"><span data-stu-id="d1a87-109">sesid</span></span>  
    <span data-ttu-id="d1a87-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d1a87-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d1a87-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="d1a87-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d1a87-112">TableID</span><span class="sxs-lookup"><span data-stu-id="d1a87-112">tableid</span></span>  
    <span data-ttu-id="d1a87-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d1a87-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="d1a87-114">Table pour laquelle récupérer les informations d’index.</span><span class="sxs-lookup"><span data-stu-id="d1a87-114">The table to retrieve index information for.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d1a87-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d1a87-115">Return value</span></span>

<span data-ttu-id="d1a87-116">Type : [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[IndexInfo](./indexinfo-class.md)\></span><span class="sxs-lookup"><span data-stu-id="d1a87-116">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[IndexInfo](./indexinfo-class.md)\></span></span>  
<span data-ttu-id="d1a87-117">Itérateur sur un IndexInfo pour chaque index de la table.</span><span class="sxs-lookup"><span data-stu-id="d1a87-117">An iterator over an IndexInfo for each index in the table.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d1a87-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1a87-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d1a87-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="d1a87-119">Reference</span></span>

[<span data-ttu-id="d1a87-120">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="d1a87-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d1a87-121">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="d1a87-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d1a87-122">Surcharge GetTableIndexes</span><span class="sxs-lookup"><span data-stu-id="d1a87-122">GetTableIndexes overload</span></span>](./api.gettableindexes-method.md)

[<span data-ttu-id="d1a87-123">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d1a87-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
