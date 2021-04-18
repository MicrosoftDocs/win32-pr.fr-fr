---
description: 'En savoir plus sur : méthode API. TryMove'
title: API. TryMove, méthode
TOCTitle: 'TryMove method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryMove(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_Move,Microsoft.Isam.Esent.Interop.MoveGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trymove(v=EXCHG.10)
ms:contentKeyID: 55100883
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryMove
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryMove
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6d4b3aa596bb5e813d87dcc6f278112fe1e4cbdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512916"
---
# <a name="apitrymove-method"></a><span data-ttu-id="877bd-103">API. TryMove, méthode</span><span class="sxs-lookup"><span data-stu-id="877bd-103">Api.TryMove method</span></span>

<span data-ttu-id="877bd-104">Essayez de naviguer dans un index.</span><span class="sxs-lookup"><span data-stu-id="877bd-104">Try to navigate through an index.</span></span> <span data-ttu-id="877bd-105">Si la navigation réussie, cette méthode retourne true.</span><span class="sxs-lookup"><span data-stu-id="877bd-105">If the navigation succeeds this method returns true.</span></span> <span data-ttu-id="877bd-106">S’il n’existe aucun enregistrement pour accéder à cette méthode, retourne false. une exception est levée pour d’autres erreurs.</span><span class="sxs-lookup"><span data-stu-id="877bd-106">If there is no record to navigate to this method returns false; an exception will be thrown for other errors.</span></span>

<span data-ttu-id="877bd-107">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="877bd-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="877bd-108">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="877bd-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="877bd-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="877bd-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryMove ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    move As JET_Move, _
    grbit As MoveGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim move As JET_Move
Dim grbit As MoveGrbit
Dim returnValue As Boolean

returnValue = Api.TryMove(sesid, _
    tableid, move, grbit)
```

``` csharp
public static bool TryMove(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_Move move,
    MoveGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="877bd-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="877bd-110">Parameters</span></span>

  - <span data-ttu-id="877bd-111">sesid</span><span class="sxs-lookup"><span data-stu-id="877bd-111">sesid</span></span>  
    <span data-ttu-id="877bd-112">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="877bd-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="877bd-113">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="877bd-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="877bd-114">TableID</span><span class="sxs-lookup"><span data-stu-id="877bd-114">tableid</span></span>  
    <span data-ttu-id="877bd-115">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="877bd-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="877bd-116">Curseur à positionner.</span><span class="sxs-lookup"><span data-stu-id="877bd-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="877bd-117">déplacer</span><span class="sxs-lookup"><span data-stu-id="877bd-117">move</span></span>  
    <span data-ttu-id="877bd-118">Type : [Microsoft.ISAM.esent.Interop.JET_Move](./jet-move-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="877bd-118">Type: [Microsoft.Isam.Esent.Interop.JET_Move](./jet-move-enumeration.md)</span></span>  
    
    <span data-ttu-id="877bd-119">Direction dans laquelle se déplacer.</span><span class="sxs-lookup"><span data-stu-id="877bd-119">The direction to move in.</span></span>

<!-- end list -->

  - <span data-ttu-id="877bd-120">grbit</span><span class="sxs-lookup"><span data-stu-id="877bd-120">grbit</span></span>  
    <span data-ttu-id="877bd-121">Type : [Microsoft. ISAM. esent. Interop. MoveGrbit](./movegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="877bd-121">Type: [Microsoft.Isam.Esent.Interop.MoveGrbit](./movegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="877bd-122">Options de déplacement.</span><span class="sxs-lookup"><span data-stu-id="877bd-122">Move options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="877bd-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="877bd-123">Return value</span></span>

<span data-ttu-id="877bd-124">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="877bd-124">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="877bd-125">True si le déplacement a réussi.</span><span class="sxs-lookup"><span data-stu-id="877bd-125">True if the move was successful.</span></span>  

## <a name="see-also"></a><span data-ttu-id="877bd-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="877bd-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="877bd-127">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="877bd-127">Reference</span></span>

[<span data-ttu-id="877bd-128">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="877bd-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="877bd-129">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="877bd-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="877bd-130">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="877bd-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
