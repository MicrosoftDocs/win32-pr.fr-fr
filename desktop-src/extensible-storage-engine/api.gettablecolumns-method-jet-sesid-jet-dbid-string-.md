---
description: 'En savoir plus sur : méthode API. GetTableColumns (JET_SESID, JET_DBID, String)'
title: Méthode API. GetTableColumns (JET_SESID, JET_DBID, String)
TOCTitle: GetTableColumns method (JET_SESID, JET_DBID, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettablecolumns(v=EXCHG.10)
ms:contentKeyID: 55107216
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetTableColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 68a05ee3d0887f4396df0b2ba3159737791c413d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524783"
---
# <a name="apigettablecolumns-method-jet_sesid-jet_dbid-string"></a><span data-ttu-id="7e0d5-103">Méthode API. GetTableColumns (JET_SESID, JET_DBID, String)</span><span class="sxs-lookup"><span data-stu-id="7e0d5-103">Api.GetTableColumns method (JET_SESID, JET_DBID, String)</span></span>

<span data-ttu-id="7e0d5-104">Itère sur toutes les colonnes de la table, en retournant des informations sur chacune d’elles.</span><span class="sxs-lookup"><span data-stu-id="7e0d5-104">Iterates over all the columns in the table, returning information about each one.</span></span>

<span data-ttu-id="7e0d5-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7e0d5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7e0d5-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7e0d5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7e0d5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7e0d5-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetTableColumns ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String _
) As IEnumerable(Of ColumnInfo)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim returnValue As IEnumerable(Of ColumnInfo)

returnValue = Api.GetTableColumns(sesid, _
    dbid, tablename)
```

``` csharp
public static IEnumerable<ColumnInfo> GetTableColumns(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename
)
```

#### <a name="parameters"></a><span data-ttu-id="7e0d5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7e0d5-108">Parameters</span></span>

  - <span data-ttu-id="7e0d5-109">sesid</span><span class="sxs-lookup"><span data-stu-id="7e0d5-109">sesid</span></span>  
    <span data-ttu-id="7e0d5-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7e0d5-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="7e0d5-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="7e0d5-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="7e0d5-112">dbid</span><span class="sxs-lookup"><span data-stu-id="7e0d5-112">dbid</span></span>  
    <span data-ttu-id="7e0d5-113">Type : [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7e0d5-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="7e0d5-114">Base de données contenant la table.</span><span class="sxs-lookup"><span data-stu-id="7e0d5-114">The database containing the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="7e0d5-115">tablename</span><span class="sxs-lookup"><span data-stu-id="7e0d5-115">tablename</span></span>  
    <span data-ttu-id="7e0d5-116">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="7e0d5-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="7e0d5-117">Nom de la table.</span><span class="sxs-lookup"><span data-stu-id="7e0d5-117">The name of the table.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7e0d5-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7e0d5-118">Return value</span></span>

<span data-ttu-id="7e0d5-119">Type : [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[ColumnInfo](./columninfo-class.md)\></span><span class="sxs-lookup"><span data-stu-id="7e0d5-119">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[ColumnInfo](./columninfo-class.md)\></span></span>  
<span data-ttu-id="7e0d5-120">Itérateur sur ColumnInfo pour chaque colonne de la table.</span><span class="sxs-lookup"><span data-stu-id="7e0d5-120">An iterator over ColumnInfo for each column in the table.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7e0d5-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e0d5-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7e0d5-122">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="7e0d5-122">Reference</span></span>

[<span data-ttu-id="7e0d5-123">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="7e0d5-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7e0d5-124">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="7e0d5-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7e0d5-125">Surcharge GetTableColumns</span><span class="sxs-lookup"><span data-stu-id="7e0d5-125">GetTableColumns overload</span></span>](./api.gettablecolumns-method.md)

[<span data-ttu-id="7e0d5-126">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7e0d5-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
