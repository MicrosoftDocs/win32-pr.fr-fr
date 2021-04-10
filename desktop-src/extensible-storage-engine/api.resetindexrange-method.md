---
description: 'En savoir plus sur : méthode API. ResetIndexRange'
title: API. ResetIndexRange, méthode
TOCTitle: 'ResetIndexRange method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.ResetIndexRange(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.resetindexrange(v=EXCHG.10)
ms:contentKeyID: 55100832
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.ResetIndexRange
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.ResetIndexRange
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 434740a549fa83d4601bf88ab09f307f4d19f189
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210901"
---
# <a name="apiresetindexrange-method"></a><span data-ttu-id="9c415-103">API. ResetIndexRange, méthode</span><span class="sxs-lookup"><span data-stu-id="9c415-103">Api.ResetIndexRange method</span></span>

<span data-ttu-id="9c415-104">Supprime une plage d’index créée avec [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) ou [TrySetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.trysetindexrange-method.md).</span><span class="sxs-lookup"><span data-stu-id="9c415-104">Removes an index range created with [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) or [TrySetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.trysetindexrange-method.md).</span></span> <span data-ttu-id="9c415-105">Si aucune plage d’index n’est présente, cette méthode n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="9c415-105">If no index range is present this method does nothing.</span></span>

<span data-ttu-id="9c415-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9c415-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9c415-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9c415-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9c415-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c415-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub ResetIndexRange ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.ResetIndexRange(sesid, tableid)
```

``` csharp
public static void ResetIndexRange(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="9c415-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9c415-109">Parameters</span></span>

  - <span data-ttu-id="9c415-110">sesid</span><span class="sxs-lookup"><span data-stu-id="9c415-110">sesid</span></span>  
    <span data-ttu-id="9c415-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9c415-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9c415-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="9c415-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="9c415-113">TableID</span><span class="sxs-lookup"><span data-stu-id="9c415-113">tableid</span></span>  
    <span data-ttu-id="9c415-114">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9c415-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="9c415-115">Curseur sur lequel supprimer la plage d’index.</span><span class="sxs-lookup"><span data-stu-id="9c415-115">The cursor to remove the index range on.</span></span>

## <a name="see-also"></a><span data-ttu-id="9c415-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c415-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9c415-117">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="9c415-117">Reference</span></span>

[<span data-ttu-id="9c415-118">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="9c415-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9c415-119">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="9c415-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9c415-120">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="9c415-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
