---
description: 'En savoir plus sur : méthode Server2003Api. JetUpdate2'
title: Méthode Server2003Api. JetUpdate2 (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: 'JetUpdate2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003api.jetupdate2(v=EXCHG.10)
ms:contentKeyID: 55104110
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fff3687d42160df331bfe52660be232fe3b41d5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112039"
---
# <a name="server2003apijetupdate2-method"></a><span data-ttu-id="95792-103">Méthode Server2003Api. JetUpdate2</span><span class="sxs-lookup"><span data-stu-id="95792-103">Server2003Api.JetUpdate2 method</span></span>

<span data-ttu-id="95792-104">La fonction JetUpdate effectue une opération de mise à jour, notamment l’insertion d’une nouvelle ligne dans une table ou la mise à jour d’une ligne existante.</span><span class="sxs-lookup"><span data-stu-id="95792-104">The JetUpdate function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="95792-105">La suppression d’une ligne de table s’effectue en appelant [JetDelete (JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span><span class="sxs-lookup"><span data-stu-id="95792-105">Deleting a table row is performed by calling [JetDelete(JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span></span>

<span data-ttu-id="95792-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="95792-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="95792-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="95792-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="95792-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95792-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetUpdate2 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer, _
    grbit As UpdateGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As Integer
Dim grbit As UpdateGrbitServer2003Api.JetUpdate2(sesid, tableid, bookmark, _
    bookmarkSize, actualBookmarkSize, _
    grbit)
```

``` csharp
public static void JetUpdate2(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize,
    UpdateGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="95792-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95792-109">Parameters</span></span>

  - <span data-ttu-id="95792-110">sesid</span><span class="sxs-lookup"><span data-stu-id="95792-110">sesid</span></span>  
    <span data-ttu-id="95792-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="95792-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="95792-112">Session qui a démarré la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="95792-112">The session which started the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="95792-113">TableID</span><span class="sxs-lookup"><span data-stu-id="95792-113">tableid</span></span>  
    <span data-ttu-id="95792-114">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="95792-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="95792-115">Curseur à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="95792-115">The cursor to update.</span></span> <span data-ttu-id="95792-116">Une mise à jour doit être préparée.</span><span class="sxs-lookup"><span data-stu-id="95792-116">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="95792-117">signet</span><span class="sxs-lookup"><span data-stu-id="95792-117">bookmark</span></span>  
    <span data-ttu-id="95792-118">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="95792-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="95792-119">Retourne le signet de l’enregistrement mis à jour.</span><span class="sxs-lookup"><span data-stu-id="95792-119">Returns the bookmark of the updated record.</span></span> <span data-ttu-id="95792-120">Peut être Null.</span><span class="sxs-lookup"><span data-stu-id="95792-120">This can be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="95792-121">bookmarkSize</span><span class="sxs-lookup"><span data-stu-id="95792-121">bookmarkSize</span></span>  
    <span data-ttu-id="95792-122">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="95792-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="95792-123">Taille de la mémoire tampon du signet.</span><span class="sxs-lookup"><span data-stu-id="95792-123">The size of the bookmark buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="95792-124">actualBookmarkSize</span><span class="sxs-lookup"><span data-stu-id="95792-124">actualBookmarkSize</span></span>  
    <span data-ttu-id="95792-125">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="95792-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="95792-126">Retourne la taille réelle du signet.</span><span class="sxs-lookup"><span data-stu-id="95792-126">Returns the actual size of the bookmark.</span></span>

<!-- end list -->

  - <span data-ttu-id="95792-127">grbit</span><span class="sxs-lookup"><span data-stu-id="95792-127">grbit</span></span>  
    <span data-ttu-id="95792-128">Type : [Microsoft. ISAM. esent. Interop. Server2003. UpdateGrbit](./updategrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="95792-128">Type: [Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit](./updategrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="95792-129">Options de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="95792-129">Update options.</span></span>

## <a name="remarks"></a><span data-ttu-id="95792-130">Notes</span><span class="sxs-lookup"><span data-stu-id="95792-130">Remarks</span></span>

<span data-ttu-id="95792-131">JetUpdate est la dernière étape de l’exécution d’une instruction INSERT ou Update.</span><span class="sxs-lookup"><span data-stu-id="95792-131">JetUpdate is the final step in performing an insert or an update.</span></span> <span data-ttu-id="95792-132">La mise à jour commence par appeler [JetPrepareUpdate (JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) , puis en appelant [JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) une ou plusieurs fois pour définir l’état de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="95792-132">The update is begun by calling [JetPrepareUpdate(JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) and then by calling [JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, \[\], Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) one or more times to set the record state.</span></span> <span data-ttu-id="95792-133">Enfin, JetUpdate2 (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32, UpdateGrbit) est appelé pour terminer l’opération de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="95792-133">Finally, JetUpdate2(JET_SESID, JET_TABLEID, \[\], Int32, Int32, UpdateGrbit) is called to complete the update operation.</span></span> <span data-ttu-id="95792-134">Les index sont mis à jour uniquement par JetUpdate ou et non pendant JetSetColumn.</span><span class="sxs-lookup"><span data-stu-id="95792-134">Indexes are updated only by JetUpdate or and not during JetSetColumn.</span></span>

## <a name="see-also"></a><span data-ttu-id="95792-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95792-135">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="95792-136">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="95792-136">Reference</span></span>

[<span data-ttu-id="95792-137">Server2003Api, classe</span><span class="sxs-lookup"><span data-stu-id="95792-137">Server2003Api class</span></span>](./server2003api-class.md)

[<span data-ttu-id="95792-138">Membres Server2003Api</span><span class="sxs-lookup"><span data-stu-id="95792-138">Server2003Api members</span></span>](./server2003api-members.md)

[<span data-ttu-id="95792-139">Espace de noms Microsoft. ISAM. esent. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="95792-139">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
