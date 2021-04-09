---
description: 'En savoir plus sur : méthode API. JetSetIndexRange'
title: API. JetSetIndexRange, méthode
TOCTitle: 'JetSetIndexRange method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetIndexRange(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetindexrange(v=EXCHG.10)
ms:contentKeyID: 55100817
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetIndexRange
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetIndexRange
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3ad13e04674de60aa1c0f55cf4cd4570f8b7ddaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033904"
---
# <a name="apijetsetindexrange-method"></a><span data-ttu-id="dac72-103">API. JetSetIndexRange, méthode</span><span class="sxs-lookup"><span data-stu-id="dac72-103">Api.JetSetIndexRange method</span></span>

<span data-ttu-id="dac72-104">Limite temporairement l’ensemble d’entrées d’index que le curseur peut suivre à l’aide de [JetMove (JET_SESID, JET_TABLEID, Int32, MoveGrbit)](./api.jetmove-method-jet-sesid-jet-tableid-int32-movegrbit-.md) à ceux qui démarrent à partir de l’entrée d’index actuelle et se terminent à l’entrée d’index qui correspond aux critères de recherche spécifiés par la clé de recherche dans ce curseur et les critères liés spécifiés.</span><span class="sxs-lookup"><span data-stu-id="dac72-104">Temporarily limits the set of index entries that the cursor can walk using [JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)](./api.jetmove-method-jet-sesid-jet-tableid-int32-movegrbit-.md) to those starting from the current index entry and ending at the index entry that matches the search criteria specified by the search key in that cursor and the specified bound criteria.</span></span> <span data-ttu-id="dac72-105">Une clé de recherche doit avoir été préalablement construite à l’aide de [JetMakeKey (JET_SESID, JET_TABLEID, \[ \] , Int32, MakeKeyGrbit)](./api.jetmakekey-method.md).</span><span class="sxs-lookup"><span data-stu-id="dac72-105">A search key must have been previously constructed using [JetMakeKey(JET_SESID, JET_TABLEID, \[\], Int32, MakeKeyGrbit)](./api.jetmakekey-method.md).</span></span> <span data-ttu-id="dac72-106">Consultez également [TrySetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.trysetindexrange-method.md).</span><span class="sxs-lookup"><span data-stu-id="dac72-106">Also see [TrySetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.trysetindexrange-method.md).</span></span>

<span data-ttu-id="dac72-107">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dac72-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="dac72-108">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="dac72-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dac72-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dac72-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetIndexRange ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SetIndexRangeGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SetIndexRangeGrbitApi.JetSetIndexRange(sesid, tableid, _
    grbit)
```

``` csharp
public static void JetSetIndexRange(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SetIndexRangeGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="dac72-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dac72-110">Parameters</span></span>

  - <span data-ttu-id="dac72-111">sesid</span><span class="sxs-lookup"><span data-stu-id="dac72-111">sesid</span></span>  
    <span data-ttu-id="dac72-112">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="dac72-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="dac72-113">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="dac72-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="dac72-114">TableID</span><span class="sxs-lookup"><span data-stu-id="dac72-114">tableid</span></span>  
    <span data-ttu-id="dac72-115">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="dac72-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="dac72-116">Curseur sur lequel définir la plage d’index.</span><span class="sxs-lookup"><span data-stu-id="dac72-116">The cursor to set the index range on.</span></span>

<!-- end list -->

  - <span data-ttu-id="dac72-117">grbit</span><span class="sxs-lookup"><span data-stu-id="dac72-117">grbit</span></span>  
    <span data-ttu-id="dac72-118">Type : [Microsoft. ISAM. esent. Interop. SetIndexRangeGrbit](./setindexrangegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="dac72-118">Type: [Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit](./setindexrangegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="dac72-119">Options de la plage d’index.</span><span class="sxs-lookup"><span data-stu-id="dac72-119">Index range options.</span></span>

## <a name="see-also"></a><span data-ttu-id="dac72-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dac72-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dac72-121">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="dac72-121">Reference</span></span>

[<span data-ttu-id="dac72-122">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="dac72-122">Api class</span></span>](./api-class.md)

[<span data-ttu-id="dac72-123">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="dac72-123">Api members</span></span>](./api-members.md)

[<span data-ttu-id="dac72-124">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="dac72-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
