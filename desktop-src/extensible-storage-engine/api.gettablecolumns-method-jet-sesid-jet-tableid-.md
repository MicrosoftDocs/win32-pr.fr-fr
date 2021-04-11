---
description: 'En savoir plus sur : méthode API. GetTableColumns (JET_SESID, JET_TABLEID)'
title: Méthode API. GetTableColumns (JET_SESID, JET_TABLEID)
TOCTitle: GetTableColumns method (JET_SESID, JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettablecolumns(v=EXCHG.10)
ms:contentKeyID: 55107218
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetTableColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 393f730920ce7abb3ef24916c9e1c9e9591ba020
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111954"
---
# <a name="apigettablecolumns-method-jet_sesid-jet_tableid"></a><span data-ttu-id="c9abb-103">Méthode API. GetTableColumns (JET_SESID, JET_TABLEID)</span><span class="sxs-lookup"><span data-stu-id="c9abb-103">Api.GetTableColumns method (JET_SESID, JET_TABLEID)</span></span>

<span data-ttu-id="c9abb-104">Itère sur toutes les colonnes de la table, en retournant des informations sur chacune d’elles.</span><span class="sxs-lookup"><span data-stu-id="c9abb-104">Iterates over all the columns in the table, returning information about each one.</span></span>

<span data-ttu-id="c9abb-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c9abb-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c9abb-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c9abb-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c9abb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9abb-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetTableColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As IEnumerable(Of ColumnInfo)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As IEnumerable(Of ColumnInfo)

returnValue = Api.GetTableColumns(sesid, _
    tableid)
```

``` csharp
public static IEnumerable<ColumnInfo> GetTableColumns(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="c9abb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9abb-108">Parameters</span></span>

  - <span data-ttu-id="c9abb-109">sesid</span><span class="sxs-lookup"><span data-stu-id="c9abb-109">sesid</span></span>  
    <span data-ttu-id="c9abb-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c9abb-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c9abb-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="c9abb-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c9abb-112">TableID</span><span class="sxs-lookup"><span data-stu-id="c9abb-112">tableid</span></span>  
    <span data-ttu-id="c9abb-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c9abb-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="c9abb-114">Table pour laquelle récupérer les informations de colonne.</span><span class="sxs-lookup"><span data-stu-id="c9abb-114">The table to retrieve column information for.</span></span>

#### <a name="return-value"></a><span data-ttu-id="c9abb-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c9abb-115">Return value</span></span>

<span data-ttu-id="c9abb-116">Type : [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[ColumnInfo](./columninfo-class.md)\></span><span class="sxs-lookup"><span data-stu-id="c9abb-116">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[ColumnInfo](./columninfo-class.md)\></span></span>  
<span data-ttu-id="c9abb-117">Itérateur sur ColumnInfo pour chaque colonne de la table.</span><span class="sxs-lookup"><span data-stu-id="c9abb-117">An iterator over ColumnInfo for each column in the table.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c9abb-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9abb-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c9abb-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="c9abb-119">Reference</span></span>

[<span data-ttu-id="c9abb-120">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="c9abb-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c9abb-121">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="c9abb-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c9abb-122">Surcharge GetTableColumns</span><span class="sxs-lookup"><span data-stu-id="c9abb-122">GetTableColumns overload</span></span>](./api.gettablecolumns-method.md)

[<span data-ttu-id="c9abb-123">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c9abb-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
