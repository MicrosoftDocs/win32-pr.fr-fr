---
description: 'En savoir plus sur : méthode API. TryOpenTable'
title: API. TryOpenTable, méthode
TOCTitle: 'TryOpenTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryOpenTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,Microsoft.Isam.Esent.Interop.OpenTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.tryopentable(v=EXCHG.10)
ms:contentKeyID: 55100889
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryOpenTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryOpenTable
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 556d3f12f24229326a6b26f357e5b19801119b74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393480"
---
# <a name="apitryopentable-method"></a><span data-ttu-id="26952-103">API. TryOpenTable, méthode</span><span class="sxs-lookup"><span data-stu-id="26952-103">Api.TryOpenTable method</span></span>

<span data-ttu-id="26952-104">Essayez d’ouvrir une table.</span><span class="sxs-lookup"><span data-stu-id="26952-104">Try to open a table.</span></span>

<span data-ttu-id="26952-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="26952-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="26952-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="26952-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="26952-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26952-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryOpenTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    grbit As OpenTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim grbit As OpenTableGrbit
Dim tableid As JET_TABLEID
Dim returnValue As Boolean

returnValue = Api.TryOpenTable(sesid, _
    dbid, tablename, grbit, tableid)
```

``` csharp
public static bool TryOpenTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    OpenTableGrbit grbit,
    out JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="26952-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26952-108">Parameters</span></span>

  - <span data-ttu-id="26952-109">sesid</span><span class="sxs-lookup"><span data-stu-id="26952-109">sesid</span></span>  
    <span data-ttu-id="26952-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="26952-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="26952-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="26952-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="26952-112">dbid</span><span class="sxs-lookup"><span data-stu-id="26952-112">dbid</span></span>  
    <span data-ttu-id="26952-113">Type : [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="26952-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="26952-114">Base de données dans laquelle rechercher la table.</span><span class="sxs-lookup"><span data-stu-id="26952-114">The database to look for the table in.</span></span>

<!-- end list -->

  - <span data-ttu-id="26952-115">tablename</span><span class="sxs-lookup"><span data-stu-id="26952-115">tablename</span></span>  
    <span data-ttu-id="26952-116">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="26952-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="26952-117">Nom de la table.</span><span class="sxs-lookup"><span data-stu-id="26952-117">The name of the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="26952-118">grbit</span><span class="sxs-lookup"><span data-stu-id="26952-118">grbit</span></span>  
    <span data-ttu-id="26952-119">Type : [Microsoft. ISAM. esent. Interop. OpenTableGrbit](./opentablegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="26952-119">Type: [Microsoft.Isam.Esent.Interop.OpenTableGrbit](./opentablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="26952-120">Options d’ouverture de la table.</span><span class="sxs-lookup"><span data-stu-id="26952-120">Table open options.</span></span>

<!-- end list -->

  - <span data-ttu-id="26952-121">TableID</span><span class="sxs-lookup"><span data-stu-id="26952-121">tableid</span></span>  
    <span data-ttu-id="26952-122">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="26952-122">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="26952-123">Retourne l’TableID ouvert.</span><span class="sxs-lookup"><span data-stu-id="26952-123">Returns the opened tableid.</span></span>

#### <a name="return-value"></a><span data-ttu-id="26952-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="26952-124">Return value</span></span>

<span data-ttu-id="26952-125">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="26952-125">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="26952-126">True si la table a été ouverte, false si elle n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="26952-126">True if the table was opened, false if the table doesn't exist.</span></span>  

## <a name="see-also"></a><span data-ttu-id="26952-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26952-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="26952-128">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="26952-128">Reference</span></span>

[<span data-ttu-id="26952-129">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="26952-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="26952-130">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="26952-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="26952-131">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="26952-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
