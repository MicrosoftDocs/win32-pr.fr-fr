---
description: 'En savoir plus sur : méthode API. JetUpdate (JET_SESID, JET_TABLEID)'
title: Méthode API. JetUpdate (JET_SESID, JET_TABLEID)
TOCTitle: JetUpdate method (JET_SESID, JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetupdate(v=EXCHG.10)
ms:contentKeyID: 55100831
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
ms.openlocfilehash: f1875353e8a5b4a23302a5f008af2cfa42a89b11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320810"
---
# <a name="apijetupdate-method-jet_sesid-jet_tableid"></a><span data-ttu-id="df993-103">Méthode API. JetUpdate (JET_SESID, JET_TABLEID)</span><span class="sxs-lookup"><span data-stu-id="df993-103">Api.JetUpdate method (JET_SESID, JET_TABLEID)</span></span>

<span data-ttu-id="df993-104">La fonction JetUpdate effectue une opération de mise à jour, notamment l’insertion d’une nouvelle ligne dans une table ou la mise à jour d’une ligne existante.</span><span class="sxs-lookup"><span data-stu-id="df993-104">The JetUpdate function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="df993-105">La suppression d’une ligne de table s’effectue en appelant [JetDelete (JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span><span class="sxs-lookup"><span data-stu-id="df993-105">Deleting a table row is performed by calling [JetDelete(JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span></span>

<span data-ttu-id="df993-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="df993-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="df993-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="df993-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="df993-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df993-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetUpdate(sesid, tableid)
```

``` csharp
public static void JetUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="df993-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df993-109">Parameters</span></span>

  - <span data-ttu-id="df993-110">sesid</span><span class="sxs-lookup"><span data-stu-id="df993-110">sesid</span></span>  
    <span data-ttu-id="df993-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="df993-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="df993-112">Session qui a démarré la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="df993-112">The session which started the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="df993-113">TableID</span><span class="sxs-lookup"><span data-stu-id="df993-113">tableid</span></span>  
    <span data-ttu-id="df993-114">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="df993-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="df993-115">Curseur à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="df993-115">The cursor to update.</span></span> <span data-ttu-id="df993-116">Une mise à jour doit être préparée.</span><span class="sxs-lookup"><span data-stu-id="df993-116">An update should be prepared.</span></span>

## <a name="remarks"></a><span data-ttu-id="df993-117">Notes</span><span class="sxs-lookup"><span data-stu-id="df993-117">Remarks</span></span>

<span data-ttu-id="df993-118">JetUpdate est la dernière étape de l’exécution d’une instruction INSERT ou Update.</span><span class="sxs-lookup"><span data-stu-id="df993-118">JetUpdate is the final step in performing an insert or an update.</span></span> <span data-ttu-id="df993-119">La mise à jour commence par appeler [JetPrepareUpdate (JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) , puis en appelant [JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) une ou plusieurs fois pour définir l’état de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="df993-119">The update is begun by calling [JetPrepareUpdate(JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) and then by calling [JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, \[\], Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) one or more times to set the record state.</span></span> <span data-ttu-id="df993-120">Enfin, [JetUpdate (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32)](./api.jetupdate-method-jet-sesid-jet-tableid-byte-int32-int32-.md) est appelé pour terminer l’opération de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="df993-120">Finally, [JetUpdate(JET_SESID, JET_TABLEID, \[\], Int32, Int32)](./api.jetupdate-method-jet-sesid-jet-tableid-byte-int32-int32-.md) is called to complete the update operation.</span></span> <span data-ttu-id="df993-121">Les index sont mis à jour uniquement par JetUpdate ou et non pendant JetSetColumn.</span><span class="sxs-lookup"><span data-stu-id="df993-121">Indexes are updated only by JetUpdate or and not during JetSetColumn.</span></span>

## <a name="see-also"></a><span data-ttu-id="df993-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df993-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="df993-123">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="df993-123">Reference</span></span>

[<span data-ttu-id="df993-124">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="df993-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="df993-125">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="df993-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="df993-126">Surcharge JetUpdate</span><span class="sxs-lookup"><span data-stu-id="df993-126">JetUpdate overload</span></span>](./api.jetupdate-method.md)

[<span data-ttu-id="df993-127">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="df993-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
