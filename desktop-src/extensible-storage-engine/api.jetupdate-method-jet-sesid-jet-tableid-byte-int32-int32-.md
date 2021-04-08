---
description: 'En savoir plus sur : méthode API. JetUpdate (JET_SESID, JET_TABLEID, Byte, Int32, Int32)'
title: Méthode API. JetUpdate (JET_SESID, JET_TABLEID, Byte, Int32, Int32)
TOCTitle: JetUpdate method (JET_SESID, JET_TABLEID, Byte , Int32, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetupdate(v=EXCHG.10)
ms:contentKeyID: 55100814
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetUpdate
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2c85e424fc9b672944801da3d03cbaff0ca48017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863218"
---
# <a name="apijetupdate-method-jet_sesid-jet_tableid-byte--int32-int32"></a><span data-ttu-id="bc3e3-103">Méthode API. JetUpdate (JET_SESID, JET_TABLEID, Byte, Int32, Int32)</span><span class="sxs-lookup"><span data-stu-id="bc3e3-103">Api.JetUpdate method (JET_SESID, JET_TABLEID, Byte , Int32, Int32)</span></span>

<span data-ttu-id="bc3e3-104">La fonction JetUpdate effectue une opération de mise à jour, notamment l’insertion d’une nouvelle ligne dans une table ou la mise à jour d’une ligne existante.</span><span class="sxs-lookup"><span data-stu-id="bc3e3-104">The JetUpdate function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="bc3e3-105">La suppression d’une ligne de table s’effectue en appelant [JetDelete (JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span><span class="sxs-lookup"><span data-stu-id="bc3e3-105">Deleting a table row is performed by calling [JetDelete(JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span></span>

<span data-ttu-id="bc3e3-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bc3e3-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bc3e3-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bc3e3-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bc3e3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc3e3-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As IntegerApi.JetUpdate(sesid, tableid, bookmark, _
    bookmarkSize, actualBookmarkSize)
```

``` csharp
public static void JetUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
)
```

#### <a name="parameters"></a><span data-ttu-id="bc3e3-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bc3e3-109">Parameters</span></span>

  - <span data-ttu-id="bc3e3-110">sesid</span><span class="sxs-lookup"><span data-stu-id="bc3e3-110">sesid</span></span>  
    <span data-ttu-id="bc3e3-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bc3e3-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="bc3e3-112">Session qui a démarré la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="bc3e3-112">The session which started the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="bc3e3-113">TableID</span><span class="sxs-lookup"><span data-stu-id="bc3e3-113">tableid</span></span>  
    <span data-ttu-id="bc3e3-114">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bc3e3-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="bc3e3-115">Curseur à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="bc3e3-115">The cursor to update.</span></span> <span data-ttu-id="bc3e3-116">Une mise à jour doit être préparée.</span><span class="sxs-lookup"><span data-stu-id="bc3e3-116">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="bc3e3-117">signet</span><span class="sxs-lookup"><span data-stu-id="bc3e3-117">bookmark</span></span>  
    <span data-ttu-id="bc3e3-118">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="bc3e3-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="bc3e3-119">Retourne le signet de l’enregistrement mis à jour.</span><span class="sxs-lookup"><span data-stu-id="bc3e3-119">Returns the bookmark of the updated record.</span></span> <span data-ttu-id="bc3e3-120">Peut être Null.</span><span class="sxs-lookup"><span data-stu-id="bc3e3-120">This can be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="bc3e3-121">bookmarkSize</span><span class="sxs-lookup"><span data-stu-id="bc3e3-121">bookmarkSize</span></span>  
    <span data-ttu-id="bc3e3-122">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="bc3e3-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="bc3e3-123">Taille de la mémoire tampon du signet.</span><span class="sxs-lookup"><span data-stu-id="bc3e3-123">The size of the bookmark buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="bc3e3-124">actualBookmarkSize</span><span class="sxs-lookup"><span data-stu-id="bc3e3-124">actualBookmarkSize</span></span>  
    <span data-ttu-id="bc3e3-125">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="bc3e3-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="bc3e3-126">Retourne la taille réelle du signet.</span><span class="sxs-lookup"><span data-stu-id="bc3e3-126">Returns the actual size of the bookmark.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc3e3-127">Notes</span><span class="sxs-lookup"><span data-stu-id="bc3e3-127">Remarks</span></span>

<span data-ttu-id="bc3e3-128">JetUpdate est la dernière étape de l’exécution d’une instruction INSERT ou Update.</span><span class="sxs-lookup"><span data-stu-id="bc3e3-128">JetUpdate is the final step in performing an insert or an update.</span></span> <span data-ttu-id="bc3e3-129">La mise à jour commence par appeler [JetPrepareUpdate (JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) , puis en appelant [JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) une ou plusieurs fois pour définir l’état de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="bc3e3-129">The update is begun by calling [JetPrepareUpdate(JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) and then by calling [JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, \[\], Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) one or more times to set the record state.</span></span> <span data-ttu-id="bc3e3-130">Enfin, JetUpdate (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32) est appelé pour terminer l’opération de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="bc3e3-130">Finally, JetUpdate(JET_SESID, JET_TABLEID, \[\], Int32, Int32) is called to complete the update operation.</span></span> <span data-ttu-id="bc3e3-131">Les index sont mis à jour uniquement par JetUpdate ou et non pendant JetSetColumn.</span><span class="sxs-lookup"><span data-stu-id="bc3e3-131">Indexes are updated only by JetUpdate or and not during JetSetColumn.</span></span>

## <a name="see-also"></a><span data-ttu-id="bc3e3-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc3e3-132">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bc3e3-133">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="bc3e3-133">Reference</span></span>

[<span data-ttu-id="bc3e3-134">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="bc3e3-134">Api class</span></span>](./api-class.md)

[<span data-ttu-id="bc3e3-135">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="bc3e3-135">Api members</span></span>](./api-members.md)

[<span data-ttu-id="bc3e3-136">Surcharge JetUpdate</span><span class="sxs-lookup"><span data-stu-id="bc3e3-136">JetUpdate overload</span></span>](./api.jetupdate-method.md)

[<span data-ttu-id="bc3e3-137">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="bc3e3-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
