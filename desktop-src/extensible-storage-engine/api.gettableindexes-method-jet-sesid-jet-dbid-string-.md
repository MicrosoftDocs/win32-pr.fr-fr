---
description: 'En savoir plus sur : méthode API. GetTableIndexes (JET_SESID, JET_DBID, String)'
title: Méthode API. GetTableIndexes (JET_SESID, JET_DBID, String)
TOCTitle: GetTableIndexes method (JET_SESID, JET_DBID, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettableindexes(v=EXCHG.10)
ms:contentKeyID: 55100648
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
ms.openlocfilehash: 90ac8dd014e0594fbffbb12b3ea4f3698f850de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861842"
---
# <a name="apigettableindexes-method-jet_sesid-jet_dbid-string"></a><span data-ttu-id="07c4f-103">Méthode API. GetTableIndexes (JET_SESID, JET_DBID, String)</span><span class="sxs-lookup"><span data-stu-id="07c4f-103">Api.GetTableIndexes method (JET_SESID, JET_DBID, String)</span></span>

<span data-ttu-id="07c4f-104">Itère sur tous les index de la table, en retournant des informations sur chacune d’elles.</span><span class="sxs-lookup"><span data-stu-id="07c4f-104">Iterates over all the indexs in the table, returning information about each one.</span></span>

<span data-ttu-id="07c4f-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="07c4f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="07c4f-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="07c4f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="07c4f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="07c4f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetTableIndexes ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String _
) As IEnumerable(Of IndexInfo)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim returnValue As IEnumerable(Of IndexInfo)

returnValue = Api.GetTableIndexes(sesid, _
    dbid, tablename)
```

``` csharp
public static IEnumerable<IndexInfo> GetTableIndexes(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename
)
```

#### <a name="parameters"></a><span data-ttu-id="07c4f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="07c4f-108">Parameters</span></span>

  - <span data-ttu-id="07c4f-109">sesid</span><span class="sxs-lookup"><span data-stu-id="07c4f-109">sesid</span></span>  
    <span data-ttu-id="07c4f-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="07c4f-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="07c4f-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="07c4f-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="07c4f-112">dbid</span><span class="sxs-lookup"><span data-stu-id="07c4f-112">dbid</span></span>  
    <span data-ttu-id="07c4f-113">Type : [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="07c4f-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="07c4f-114">Base de données contenant la table.</span><span class="sxs-lookup"><span data-stu-id="07c4f-114">The database containing the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="07c4f-115">tablename</span><span class="sxs-lookup"><span data-stu-id="07c4f-115">tablename</span></span>  
    <span data-ttu-id="07c4f-116">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="07c4f-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="07c4f-117">Nom de la table.</span><span class="sxs-lookup"><span data-stu-id="07c4f-117">The name of the table.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07c4f-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="07c4f-118">Return value</span></span>

<span data-ttu-id="07c4f-119">Type : [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[IndexInfo](./indexinfo-class.md)\></span><span class="sxs-lookup"><span data-stu-id="07c4f-119">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[IndexInfo](./indexinfo-class.md)\></span></span>  
<span data-ttu-id="07c4f-120">Itérateur sur un IndexInfo pour chaque index de la table.</span><span class="sxs-lookup"><span data-stu-id="07c4f-120">An iterator over an IndexInfo for each index in the table.</span></span>  

## <a name="see-also"></a><span data-ttu-id="07c4f-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07c4f-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="07c4f-122">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="07c4f-122">Reference</span></span>

[<span data-ttu-id="07c4f-123">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="07c4f-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="07c4f-124">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="07c4f-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="07c4f-125">Surcharge GetTableIndexes</span><span class="sxs-lookup"><span data-stu-id="07c4f-125">GetTableIndexes overload</span></span>](./api.gettableindexes-method.md)

[<span data-ttu-id="07c4f-126">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="07c4f-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
