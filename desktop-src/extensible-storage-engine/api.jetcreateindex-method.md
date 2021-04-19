---
description: 'En savoir plus sur : méthode API. JetCreateIndex'
title: API. JetCreateIndex, méthode
TOCTitle: 'JetCreateIndex method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateIndex(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.CreateIndexGrbit,System.String,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateindex(v=EXCHG.10)
ms:contentKeyID: 55100693
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a9b3549461324f396408bb7d370531907248e8c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513375"
---
# <a name="apijetcreateindex-method"></a><span data-ttu-id="2463f-103">API. JetCreateIndex, méthode</span><span class="sxs-lookup"><span data-stu-id="2463f-103">Api.JetCreateIndex method</span></span>

<span data-ttu-id="2463f-104">Crée un index sur les données d’une base de données ESE.</span><span class="sxs-lookup"><span data-stu-id="2463f-104">Creates an index over data in an ESE database.</span></span> <span data-ttu-id="2463f-105">Un index peut être utilisé pour localiser rapidement des données spécifiques.</span><span class="sxs-lookup"><span data-stu-id="2463f-105">An index can be used to locate specific data quickly.</span></span>

<span data-ttu-id="2463f-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2463f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2463f-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2463f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2463f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2463f-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateIndex ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexName As String, _
    grbit As CreateIndexGrbit, _
    keyDescription As String, _
    keyDescriptionLength As Integer, _
    density As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexName As String
Dim grbit As CreateIndexGrbit
Dim keyDescription As String
Dim keyDescriptionLength As Integer
Dim density As IntegerApi.JetCreateIndex(sesid, tableid, _
    indexName, grbit, keyDescription, _
    keyDescriptionLength, density)
```

``` csharp
public static void JetCreateIndex(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexName,
    CreateIndexGrbit grbit,
    string keyDescription,
    int keyDescriptionLength,
    int density
)
```

#### <a name="parameters"></a><span data-ttu-id="2463f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2463f-109">Parameters</span></span>

  - <span data-ttu-id="2463f-110">sesid</span><span class="sxs-lookup"><span data-stu-id="2463f-110">sesid</span></span>  
    <span data-ttu-id="2463f-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2463f-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="2463f-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="2463f-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="2463f-113">TableID</span><span class="sxs-lookup"><span data-stu-id="2463f-113">tableid</span></span>  
    <span data-ttu-id="2463f-114">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2463f-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="2463f-115">Table sur laquelle créer l’index.</span><span class="sxs-lookup"><span data-stu-id="2463f-115">The table to create the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="2463f-116">indexName</span><span class="sxs-lookup"><span data-stu-id="2463f-116">indexName</span></span>  
    <span data-ttu-id="2463f-117">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="2463f-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="2463f-118">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’index à créer.</span><span class="sxs-lookup"><span data-stu-id="2463f-118">Pointer to a null-terminated string that specifies the name of the index to create.</span></span>

<!-- end list -->

  - <span data-ttu-id="2463f-119">grbit</span><span class="sxs-lookup"><span data-stu-id="2463f-119">grbit</span></span>  
    <span data-ttu-id="2463f-120">Type : [Microsoft. ISAM. esent. Interop. CreateIndexGrbit](./createindexgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="2463f-120">Type: [Microsoft.Isam.Esent.Interop.CreateIndexGrbit](./createindexgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="2463f-121">Options de création d’index.</span><span class="sxs-lookup"><span data-stu-id="2463f-121">Index creation options.</span></span>

<!-- end list -->

  - <span data-ttu-id="2463f-122">keydescription</span><span class="sxs-lookup"><span data-stu-id="2463f-122">keyDescription</span></span>  
    <span data-ttu-id="2463f-123">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="2463f-123">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="2463f-124">Pointeur vers une chaîne double terminée par un caractère null des jetons délimités par des valeurs NULL.</span><span class="sxs-lookup"><span data-stu-id="2463f-124">Pointer to a double null-terminated string of null-delimited tokens.</span></span>

<!-- end list -->

  - <span data-ttu-id="2463f-125">keyDescriptionLength</span><span class="sxs-lookup"><span data-stu-id="2463f-125">keyDescriptionLength</span></span>  
    <span data-ttu-id="2463f-126">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="2463f-126">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="2463f-127">Longueur, en caractères, de szKey, y compris les deux valeurs null de fin.</span><span class="sxs-lookup"><span data-stu-id="2463f-127">The length, in characters, of szKey including the two terminating nulls.</span></span>

<!-- end list -->

  - <span data-ttu-id="2463f-128">masse</span><span class="sxs-lookup"><span data-stu-id="2463f-128">density</span></span>  
    <span data-ttu-id="2463f-129">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="2463f-129">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="2463f-130">Densité initiale B + arborescence.</span><span class="sxs-lookup"><span data-stu-id="2463f-130">Initial B+ tree density.</span></span>

## <a name="see-also"></a><span data-ttu-id="2463f-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2463f-131">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2463f-132">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="2463f-132">Reference</span></span>

[<span data-ttu-id="2463f-133">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="2463f-133">Api class</span></span>](./api-class.md)

[<span data-ttu-id="2463f-134">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="2463f-134">Api members</span></span>](./api-members.md)

[<span data-ttu-id="2463f-135">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2463f-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
