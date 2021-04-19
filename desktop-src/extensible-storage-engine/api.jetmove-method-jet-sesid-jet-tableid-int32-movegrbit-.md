---
description: 'En savoir plus sur : méthode API. JetMove (JET_SESID, JET_TABLEID, Int32, MoveGrbit)'
title: Méthode API. JetMove (JET_SESID, JET_TABLEID, Int32, MoveGrbit)
TOCTitle: JetMove method (JET_SESID, JET_TABLEID, Int32, MoveGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetMove(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32,Microsoft.Isam.Esent.Interop.MoveGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetmove(v=EXCHG.10)
ms:contentKeyID: 55100765
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetMove
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f6d77914a3dc4728626db8e4ffe271851099e5e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536648"
---
# <a name="apijetmove-method-jet_sesid-jet_tableid-int32-movegrbit"></a><span data-ttu-id="5cc40-103">Méthode API. JetMove (JET_SESID, JET_TABLEID, Int32, MoveGrbit)</span><span class="sxs-lookup"><span data-stu-id="5cc40-103">Api.JetMove method (JET_SESID, JET_TABLEID, Int32, MoveGrbit)</span></span>

<span data-ttu-id="5cc40-104">Naviguer dans un index.</span><span class="sxs-lookup"><span data-stu-id="5cc40-104">Navigate through an index.</span></span> <span data-ttu-id="5cc40-105">Le curseur peut être positionné au début ou à la fin de l’index et déplacé vers l’arrière et vers l’avant par un nombre spécifié d’entrées d’index.</span><span class="sxs-lookup"><span data-stu-id="5cc40-105">The cursor can be positioned at the start or end of the index and moved backwards and forwards by a specified number of index entries.</span></span> <span data-ttu-id="5cc40-106">Consultez également [TryMoveFirst (JET_SESID, JET_TABLEID)](./api.trymovefirst-method.md), [TryMoveLast (JET_SESID, JET_TABLEID)](./api.trymovelast-method.md), [TryMoveNext (JET_SESID, JET_TABLEID)](./api.trymovenext-method.md), [TryMovePrevious (JET_SESID, JET_TABLEID)](./api.trymoveprevious-method.md).</span><span class="sxs-lookup"><span data-stu-id="5cc40-106">Also see [TryMoveFirst(JET_SESID, JET_TABLEID)](./api.trymovefirst-method.md), [TryMoveLast(JET_SESID, JET_TABLEID)](./api.trymovelast-method.md), [TryMoveNext(JET_SESID, JET_TABLEID)](./api.trymovenext-method.md), [TryMovePrevious(JET_SESID, JET_TABLEID)](./api.trymoveprevious-method.md).</span></span>

<span data-ttu-id="5cc40-107">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5cc40-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5cc40-108">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5cc40-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5cc40-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5cc40-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetMove ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    numRows As Integer, _
    grbit As MoveGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numRows As Integer
Dim grbit As MoveGrbitApi.JetMove(sesid, tableid, numRows, _
    grbit)
```

``` csharp
public static void JetMove(
    JET_SESID sesid,
    JET_TABLEID tableid,
    int numRows,
    MoveGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="5cc40-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5cc40-110">Parameters</span></span>

  - <span data-ttu-id="5cc40-111">sesid</span><span class="sxs-lookup"><span data-stu-id="5cc40-111">sesid</span></span>  
    <span data-ttu-id="5cc40-112">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5cc40-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5cc40-113">Session à utiliser pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="5cc40-113">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="5cc40-114">TableID</span><span class="sxs-lookup"><span data-stu-id="5cc40-114">tableid</span></span>  
    <span data-ttu-id="5cc40-115">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5cc40-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="5cc40-116">Curseur à positionner.</span><span class="sxs-lookup"><span data-stu-id="5cc40-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="5cc40-117">numRows</span><span class="sxs-lookup"><span data-stu-id="5cc40-117">numRows</span></span>  
    <span data-ttu-id="5cc40-118">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5cc40-118">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="5cc40-119">Décalage qui indique la distance de déplacement du curseur.</span><span class="sxs-lookup"><span data-stu-id="5cc40-119">An offset which indicates how far to move the cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="5cc40-120">grbit</span><span class="sxs-lookup"><span data-stu-id="5cc40-120">grbit</span></span>  
    <span data-ttu-id="5cc40-121">Type : [Microsoft. ISAM. esent. Interop. MoveGrbit](./movegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="5cc40-121">Type: [Microsoft.Isam.Esent.Interop.MoveGrbit](./movegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="5cc40-122">Options de déplacement.</span><span class="sxs-lookup"><span data-stu-id="5cc40-122">Move options.</span></span>

## <a name="see-also"></a><span data-ttu-id="5cc40-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5cc40-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5cc40-124">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="5cc40-124">Reference</span></span>

[<span data-ttu-id="5cc40-125">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="5cc40-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="5cc40-126">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="5cc40-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="5cc40-127">Surcharge JetMove</span><span class="sxs-lookup"><span data-stu-id="5cc40-127">JetMove overload</span></span>](./api.jetmove-method.md)

[<span data-ttu-id="5cc40-128">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="5cc40-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
