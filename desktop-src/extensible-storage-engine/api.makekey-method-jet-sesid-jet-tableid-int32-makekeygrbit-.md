---
description: 'En savoir plus sur : méthode API. MakeKey (JET_SESID, JET_TABLEID, Int32, MakeKeyGrbit)'
title: Méthode API. MakeKey (JET_SESID, JET_TABLEID, Int32, MakeKeyGrbit)
TOCTitle: MakeKey method (JET_SESID, JET_TABLEID, Int32, MakeKeyGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.makekey(v=EXCHG.10)
ms:contentKeyID: 55100824
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.MakeKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 75bef87c6981bfc6de90d3b1cfdd9fe4c4b020e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320809"
---
# <a name="apimakekey-method-jet_sesid-jet_tableid-int32-makekeygrbit"></a><span data-ttu-id="37bb3-103">Méthode API. MakeKey (JET_SESID, JET_TABLEID, Int32, MakeKeyGrbit)</span><span class="sxs-lookup"><span data-stu-id="37bb3-103">Api.MakeKey method (JET_SESID, JET_TABLEID, Int32, MakeKeyGrbit)</span></span>

<span data-ttu-id="37bb3-104">Construit une clé de recherche qui peut ensuite être utilisée par [JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) et [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span><span class="sxs-lookup"><span data-stu-id="37bb3-104">Constructs a search key that may then be used by [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) and [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span></span>

<span data-ttu-id="37bb3-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="37bb3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="37bb3-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="37bb3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="37bb3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37bb3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub MakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As Integer, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As Integer
Dim grbit As MakeKeyGrbitApi.MakeKey(sesid, tableid, data, _
    grbit)
```

``` csharp
public static void MakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    int data,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="37bb3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37bb3-108">Parameters</span></span>

  - <span data-ttu-id="37bb3-109">sesid</span><span class="sxs-lookup"><span data-stu-id="37bb3-109">sesid</span></span>  
    <span data-ttu-id="37bb3-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="37bb3-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="37bb3-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="37bb3-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="37bb3-112">TableID</span><span class="sxs-lookup"><span data-stu-id="37bb3-112">tableid</span></span>  
    <span data-ttu-id="37bb3-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="37bb3-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="37bb3-114">Curseur sur lequel créer la clé.</span><span class="sxs-lookup"><span data-stu-id="37bb3-114">The cursor to create the key on.</span></span>

<!-- end list -->

  - <span data-ttu-id="37bb3-115">data</span><span class="sxs-lookup"><span data-stu-id="37bb3-115">data</span></span>  
    <span data-ttu-id="37bb3-116">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="37bb3-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="37bb3-117">Données de colonne pour la colonne clé actuelle de l’index actuel.</span><span class="sxs-lookup"><span data-stu-id="37bb3-117">Column data for the current key column of the current index.</span></span>

<!-- end list -->

  - <span data-ttu-id="37bb3-118">grbit</span><span class="sxs-lookup"><span data-stu-id="37bb3-118">grbit</span></span>  
    <span data-ttu-id="37bb3-119">Type : [Microsoft. ISAM. esent. Interop. MakeKeyGrbit](./makekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="37bb3-119">Type: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="37bb3-120">Options de clé.</span><span class="sxs-lookup"><span data-stu-id="37bb3-120">Key options.</span></span>

## <a name="see-also"></a><span data-ttu-id="37bb3-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37bb3-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="37bb3-122">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="37bb3-122">Reference</span></span>

[<span data-ttu-id="37bb3-123">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="37bb3-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="37bb3-124">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="37bb3-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="37bb3-125">Surcharge MakeKey</span><span class="sxs-lookup"><span data-stu-id="37bb3-125">MakeKey overload</span></span>](./api.makekey-method.md)

[<span data-ttu-id="37bb3-126">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="37bb3-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
