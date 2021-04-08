---
description: 'En savoir plus sur : méthode API. JetCreateIndex2'
title: API. JetCreateIndex2, méthode
TOCTitle: 'JetCreateIndex2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateIndex2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_INDEXCREATE[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateindex2(v=EXCHG.10)
ms:contentKeyID: 55100673
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b5fa690ed127c41b8a84f5d8aa012510f3a9c3e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862246"
---
# <a name="apijetcreateindex2-method"></a><span data-ttu-id="9f7b3-103">API. JetCreateIndex2, méthode</span><span class="sxs-lookup"><span data-stu-id="9f7b3-103">Api.JetCreateIndex2 method</span></span>

<span data-ttu-id="9f7b3-104">Crée des index sur des données dans une base de données ESE.</span><span class="sxs-lookup"><span data-stu-id="9f7b3-104">Creates indexes over data in an ESE database.</span></span>

<span data-ttu-id="9f7b3-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9f7b3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9f7b3-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9f7b3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9f7b3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f7b3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateIndex2 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexcreates As JET_INDEXCREATE(), _
    numIndexCreates As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexcreates As JET_INDEXCREATE()
Dim numIndexCreates As IntegerApi.JetCreateIndex2(sesid, tableid, _
    indexcreates, numIndexCreates)
```

``` csharp
public static void JetCreateIndex2(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_INDEXCREATE[] indexcreates,
    int numIndexCreates
)
```

#### <a name="parameters"></a><span data-ttu-id="9f7b3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f7b3-108">Parameters</span></span>

  - <span data-ttu-id="9f7b3-109">sesid</span><span class="sxs-lookup"><span data-stu-id="9f7b3-109">sesid</span></span>  
    <span data-ttu-id="9f7b3-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9f7b3-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9f7b3-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="9f7b3-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="9f7b3-112">TableID</span><span class="sxs-lookup"><span data-stu-id="9f7b3-112">tableid</span></span>  
    <span data-ttu-id="9f7b3-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9f7b3-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="9f7b3-114">Table sur laquelle créer l’index.</span><span class="sxs-lookup"><span data-stu-id="9f7b3-114">The table to create the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="9f7b3-115">indexcreates</span><span class="sxs-lookup"><span data-stu-id="9f7b3-115">indexcreates</span></span>  
    <span data-ttu-id="9f7b3-116">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="9f7b3-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="9f7b3-117">Tableau d’objets décrivant les index à créer.</span><span class="sxs-lookup"><span data-stu-id="9f7b3-117">Array of objects describing the indexes to be created.</span></span>

<!-- end list -->

  - <span data-ttu-id="9f7b3-118">numIndexCreates</span><span class="sxs-lookup"><span data-stu-id="9f7b3-118">numIndexCreates</span></span>  
    <span data-ttu-id="9f7b3-119">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="9f7b3-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="9f7b3-120">Nombre d’objets de description d’index.</span><span class="sxs-lookup"><span data-stu-id="9f7b3-120">Number of index description objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f7b3-121">Notes</span><span class="sxs-lookup"><span data-stu-id="9f7b3-121">Remarks</span></span>

<span data-ttu-id="9f7b3-122">Lors de la création de plusieurs index (par exemple, avec numIndexCreates supérieur à 1), cette méthode doit être appelée en dehors de toutes les transactions et avec un accès exclusif à la table.</span><span class="sxs-lookup"><span data-stu-id="9f7b3-122">When creating multiple indexes (i.e. with numIndexCreates greater than 1) this method MUST be called outside of any transactions and with exclusive access to the table.</span></span> <span data-ttu-id="9f7b3-123">Le JET_TABLEID retourné par « JetCreateTable » aura un accès L2 exclusifs ou la table peut être ouverte pour un accès exclusif en passant [DenyRead](./opentablegrbit-enumeration.md) à [JetOpenTable (JET_SESID, JET_DBID, String, \[ \] , Int32, OpenTableGrbit, JET_TABLEID)](./api.jetopentable-method.md).</span><span class="sxs-lookup"><span data-stu-id="9f7b3-123">The JET_TABLEID returned by "JetCreateTable" will have exlusive access or the table can be opened for exclusive access by passing [DenyRead](./opentablegrbit-enumeration.md) to [JetOpenTable(JET_SESID, JET_DBID, String, \[\], Int32, OpenTableGrbit, JET_TABLEID)](./api.jetopentable-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="9f7b3-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f7b3-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9f7b3-125">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="9f7b3-125">Reference</span></span>

[<span data-ttu-id="9f7b3-126">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="9f7b3-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9f7b3-127">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="9f7b3-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9f7b3-128">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="9f7b3-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
