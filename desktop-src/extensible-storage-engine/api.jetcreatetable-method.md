---
description: 'En savoir plus sur : méthode API. JetCreateTable'
title: API. JetCreateTable, méthode
TOCTitle: 'JetCreateTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Int32,System.Int32,Microsoft.Isam.Esent.Interop.JET_TABLEID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreatetable(v=EXCHG.10)
ms:contentKeyID: 55100676
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateTable
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8025e35746d921fda3b601d289a9b361aefefb83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484537"
---
# <a name="apijetcreatetable-method"></a><span data-ttu-id="31dd3-103">API. JetCreateTable, méthode</span><span class="sxs-lookup"><span data-stu-id="31dd3-103">Api.JetCreateTable method</span></span>

<span data-ttu-id="31dd3-104">Créez une table vide.</span><span class="sxs-lookup"><span data-stu-id="31dd3-104">Create an empty table.</span></span> <span data-ttu-id="31dd3-105">La table nouvellement créée est ouverte en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="31dd3-105">The newly created table is opened exclusively.</span></span>

<span data-ttu-id="31dd3-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="31dd3-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="31dd3-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="31dd3-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="31dd3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31dd3-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    table As String, _
    pages As Integer, _
    density As Integer, _
    <OutAttribute> ByRef tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim table As String
Dim pages As Integer
Dim density As Integer
Dim tableid As JET_TABLEIDApi.JetCreateTable(sesid, dbid, _
    table, pages, density, tableid)
```

``` csharp
public static void JetCreateTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string table,
    int pages,
    int density,
    out JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="31dd3-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="31dd3-109">Parameters</span></span>

  - <span data-ttu-id="31dd3-110">sesid</span><span class="sxs-lookup"><span data-stu-id="31dd3-110">sesid</span></span>  
    <span data-ttu-id="31dd3-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="31dd3-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="31dd3-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="31dd3-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="31dd3-113">dbid</span><span class="sxs-lookup"><span data-stu-id="31dd3-113">dbid</span></span>  
    <span data-ttu-id="31dd3-114">Type : [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="31dd3-114">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="31dd3-115">Base de données dans laquelle créer la table.</span><span class="sxs-lookup"><span data-stu-id="31dd3-115">The database to create the table in.</span></span>

<!-- end list -->

  - <span data-ttu-id="31dd3-116">table</span><span class="sxs-lookup"><span data-stu-id="31dd3-116">table</span></span>  
    <span data-ttu-id="31dd3-117">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="31dd3-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="31dd3-118">Nom de la table à créer.</span><span class="sxs-lookup"><span data-stu-id="31dd3-118">The name of the table to create.</span></span>

<!-- end list -->

  - <span data-ttu-id="31dd3-119">pages</span><span class="sxs-lookup"><span data-stu-id="31dd3-119">pages</span></span>  
    <span data-ttu-id="31dd3-120">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="31dd3-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="31dd3-121">Nombre initial de pages dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="31dd3-121">Initial number of pages in the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="31dd3-122">masse</span><span class="sxs-lookup"><span data-stu-id="31dd3-122">density</span></span>  
    <span data-ttu-id="31dd3-123">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="31dd3-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="31dd3-124">Densité par défaut de la table.</span><span class="sxs-lookup"><span data-stu-id="31dd3-124">The default density of the table.</span></span> <span data-ttu-id="31dd3-125">Utilisé lors des insertions séquentielles.</span><span class="sxs-lookup"><span data-stu-id="31dd3-125">This is used when doing sequential inserts.</span></span>

<!-- end list -->

  - <span data-ttu-id="31dd3-126">TableID</span><span class="sxs-lookup"><span data-stu-id="31dd3-126">tableid</span></span>  
    <span data-ttu-id="31dd3-127">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="31dd3-127">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="31dd3-128">Retourne l’TableID de la nouvelle table.</span><span class="sxs-lookup"><span data-stu-id="31dd3-128">Returns the tableid of the new table.</span></span>

## <a name="see-also"></a><span data-ttu-id="31dd3-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31dd3-129">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="31dd3-130">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="31dd3-130">Reference</span></span>

[<span data-ttu-id="31dd3-131">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="31dd3-131">Api class</span></span>](./api-class.md)

[<span data-ttu-id="31dd3-132">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="31dd3-132">Api members</span></span>](./api-members.md)

[<span data-ttu-id="31dd3-133">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="31dd3-133">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
