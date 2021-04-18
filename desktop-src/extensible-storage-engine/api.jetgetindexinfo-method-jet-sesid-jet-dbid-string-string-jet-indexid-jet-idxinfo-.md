---
description: 'En savoir plus sur : méthode API. JetGetIndexInfo (JET_SESID, JET_DBID, String, String, JET_INDEXID, JET_IdxInfo)'
title: Méthode API. JetGetIndexInfo (JET_SESID, JET_DBID, String, String, JET_INDEXID, JET_IdxInfo)
TOCTitle: JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, JET_INDEXID, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXID@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100772
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ac8a622f3b653885374888fa9fa6b2835ef8ede0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536325"
---
# <a name="apijetgetindexinfo-method-jet_sesid-jet_dbid-string-string-jet_indexid-jet_idxinfo"></a><span data-ttu-id="3d3fd-103">Méthode API. JetGetIndexInfo (JET_SESID, JET_DBID, String, String, JET_INDEXID, JET_IdxInfo)</span><span class="sxs-lookup"><span data-stu-id="3d3fd-103">Api.JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, JET_INDEXID, JET_IdxInfo)</span></span>

<span data-ttu-id="3d3fd-104">Récupère des informations sur les index d’une table.</span><span class="sxs-lookup"><span data-stu-id="3d3fd-104">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="3d3fd-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3d3fd-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3d3fd-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3d3fd-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3d3fd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d3fd-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetIndexInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    indexname As String, _
    <OutAttribute> ByRef result As JET_INDEXID, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim indexname As String
Dim result As JET_INDEXID
Dim infoLevel As JET_IdxInfoApi.JetGetIndexInfo(sesid, dbid, _
    tablename, indexname, result, infoLevel)
```

``` csharp
public static void JetGetIndexInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string indexname,
    out JET_INDEXID result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="3d3fd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3d3fd-108">Parameters</span></span>

  - <span data-ttu-id="3d3fd-109">sesid</span><span class="sxs-lookup"><span data-stu-id="3d3fd-109">sesid</span></span>  
    <span data-ttu-id="3d3fd-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3d3fd-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="3d3fd-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="3d3fd-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="3d3fd-112">dbid</span><span class="sxs-lookup"><span data-stu-id="3d3fd-112">dbid</span></span>  
    <span data-ttu-id="3d3fd-113">Type : [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3d3fd-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="3d3fd-114">Base de données à utiliser.</span><span class="sxs-lookup"><span data-stu-id="3d3fd-114">The database to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="3d3fd-115">tablename</span><span class="sxs-lookup"><span data-stu-id="3d3fd-115">tablename</span></span>  
    <span data-ttu-id="3d3fd-116">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="3d3fd-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="3d3fd-117">Nom de la table sur laquelle récupérer les informations d’index.</span><span class="sxs-lookup"><span data-stu-id="3d3fd-117">The name of the table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="3d3fd-118">IndexName</span><span class="sxs-lookup"><span data-stu-id="3d3fd-118">indexname</span></span>  
    <span data-ttu-id="3d3fd-119">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="3d3fd-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="3d3fd-120">Nom de l’index sur lequel récupérer des informations.</span><span class="sxs-lookup"><span data-stu-id="3d3fd-120">The name of the index to retrieve information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="3d3fd-121">result</span><span class="sxs-lookup"><span data-stu-id="3d3fd-121">result</span></span>  
    <span data-ttu-id="3d3fd-122">Type : [Microsoft.ISAM.esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="3d3fd-122">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span></span>  
    
    <span data-ttu-id="3d3fd-123">Renseigné avec des informations sur les index de la table.</span><span class="sxs-lookup"><span data-stu-id="3d3fd-123">Filled in with information about indexes on the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="3d3fd-124">infoLevel</span><span class="sxs-lookup"><span data-stu-id="3d3fd-124">infoLevel</span></span>  
    <span data-ttu-id="3d3fd-125">Type : [Microsoft.ISAM.esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="3d3fd-125">Type: [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="3d3fd-126">Type d’informations à récupérer.</span><span class="sxs-lookup"><span data-stu-id="3d3fd-126">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="3d3fd-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d3fd-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3d3fd-128">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="3d3fd-128">Reference</span></span>

[<span data-ttu-id="3d3fd-129">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="3d3fd-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="3d3fd-130">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="3d3fd-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="3d3fd-131">Surcharge JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="3d3fd-131">JetGetIndexInfo overload</span></span>](./api.jetgetindexinfo-method.md)

[<span data-ttu-id="3d3fd-132">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3d3fd-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
