---
description: 'En savoir plus sur les alertes suivantes : Constructeur de table'
title: Constructeur de table
TOCTitle: 'Table constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Table.#ctor(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,Microsoft.Isam.Esent.Interop.OpenTableGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.table.table(v=EXCHG.10)
ms:contentKeyID: 55104142
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Table.Table
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Table..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8987e643253791e5315dd07b7b20a40dee66cf9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516910"
---
# <a name="table-constructor"></a><span data-ttu-id="97f50-103">Constructeur de table</span><span class="sxs-lookup"><span data-stu-id="97f50-103">Table constructor</span></span>

<span data-ttu-id="97f50-104">Initialise une nouvelle instance de la classe table.</span><span class="sxs-lookup"><span data-stu-id="97f50-104">Initializes a new instance of the Table class.</span></span> <span data-ttu-id="97f50-105">La table est ouverte à partir de la base de données spécifiée.</span><span class="sxs-lookup"><span data-stu-id="97f50-105">The table is opened from the given database.</span></span>

<span data-ttu-id="97f50-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="97f50-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="97f50-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="97f50-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="97f50-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97f50-108">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    name As String, _
    grbit As OpenTableGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim name As String
Dim grbit As OpenTableGrbit

Dim instance As New Table(sesid, dbid, _
    name, grbit)
```

``` csharp
public Table(
    JET_SESID sesid,
    JET_DBID dbid,
    string name,
    OpenTableGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="97f50-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97f50-109">Parameters</span></span>

  - <span data-ttu-id="97f50-110">sesid</span><span class="sxs-lookup"><span data-stu-id="97f50-110">sesid</span></span>  
    <span data-ttu-id="97f50-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="97f50-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="97f50-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="97f50-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="97f50-113">dbid</span><span class="sxs-lookup"><span data-stu-id="97f50-113">dbid</span></span>  
    <span data-ttu-id="97f50-114">Type : [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="97f50-114">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="97f50-115">Base de données dans laquelle ouvrir la table.</span><span class="sxs-lookup"><span data-stu-id="97f50-115">The database to open the table in.</span></span>

<!-- end list -->

  - <span data-ttu-id="97f50-116">name</span><span class="sxs-lookup"><span data-stu-id="97f50-116">name</span></span>  
    <span data-ttu-id="97f50-117">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="97f50-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="97f50-118">Nom de la table.</span><span class="sxs-lookup"><span data-stu-id="97f50-118">The name of the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="97f50-119">grbit</span><span class="sxs-lookup"><span data-stu-id="97f50-119">grbit</span></span>  
    <span data-ttu-id="97f50-120">Type : [Microsoft. ISAM. esent. Interop. OpenTableGrbit](./opentablegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="97f50-120">Type: [Microsoft.Isam.Esent.Interop.OpenTableGrbit](./opentablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="97f50-121">Options JetOpenTable.</span><span class="sxs-lookup"><span data-stu-id="97f50-121">JetOpenTable options.</span></span>

## <a name="see-also"></a><span data-ttu-id="97f50-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97f50-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="97f50-123">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="97f50-123">Reference</span></span>

[<span data-ttu-id="97f50-124">Classe de table</span><span class="sxs-lookup"><span data-stu-id="97f50-124">Table class</span></span>](./table-class.md)

[<span data-ttu-id="97f50-125">Membres de table</span><span class="sxs-lookup"><span data-stu-id="97f50-125">Table members</span></span>](./table-members.md)

[<span data-ttu-id="97f50-126">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="97f50-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
