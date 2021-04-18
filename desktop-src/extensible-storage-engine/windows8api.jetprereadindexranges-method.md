---
description: 'En savoir plus sur : méthode Windows8Api. JetPrereadIndexRanges'
title: Méthode Windows8Api. JetPrereadIndexRanges (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'JetPrereadIndexRanges method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetPrereadIndexRanges(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[],Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetprereadindexranges(v=EXCHG.10)
ms:contentKeyID: 55104451
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetPrereadIndexRanges
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetPrereadIndexRanges
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 986213a054dec54e92e4ecfe6fb0abd541b451ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519783"
---
# <a name="windows8apijetprereadindexranges-method"></a><span data-ttu-id="8178f-103">Méthode Windows8Api. JetPrereadIndexRanges</span><span class="sxs-lookup"><span data-stu-id="8178f-103">Windows8Api.JetPrereadIndexRanges method</span></span>

<span data-ttu-id="8178f-104">Si les enregistrements avec les plages de clés spécifiées ne se trouvent pas dans le cache des tampons, lancez des lectures asynchrones pour placer les enregistrements dans le cache des tampons de la base de données.</span><span class="sxs-lookup"><span data-stu-id="8178f-104">If the records with the specified key ranges are not in the buffer cache, then start asynchronous reads to bring the records into the database buffer cache.</span></span>

<span data-ttu-id="8178f-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8178f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="8178f-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8178f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8178f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8178f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetPrereadIndexRanges ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexRanges As JET_INDEX_RANGE(), _
    rangeIndex As Integer, _
    rangeCount As Integer, _
    <OutAttribute> ByRef rangesPreread As Integer, _
    columnsPreread As JET_COLUMNID(), _
    grbit As PrereadIndexRangesGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexRanges As JET_INDEX_RANGE()
Dim rangeIndex As Integer
Dim rangeCount As Integer
Dim rangesPreread As Integer
Dim columnsPreread As JET_COLUMNID()
Dim grbit As PrereadIndexRangesGrbitWindows8Api.JetPrereadIndexRanges(sesid, _
    tableid, indexRanges, rangeIndex, _
    rangeCount, rangesPreread, columnsPreread, _
    grbit)
```

``` csharp
public static void JetPrereadIndexRanges(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_INDEX_RANGE[] indexRanges,
    int rangeIndex,
    int rangeCount,
    out int rangesPreread,
    JET_COLUMNID[] columnsPreread,
    PrereadIndexRangesGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="8178f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8178f-108">Parameters</span></span>

  - <span data-ttu-id="8178f-109">sesid</span><span class="sxs-lookup"><span data-stu-id="8178f-109">sesid</span></span>  
    <span data-ttu-id="8178f-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8178f-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="8178f-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="8178f-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="8178f-112">TableID</span><span class="sxs-lookup"><span data-stu-id="8178f-112">tableid</span></span>  
    <span data-ttu-id="8178f-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8178f-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="8178f-114">Table avec laquelle émettre les prélectures.</span><span class="sxs-lookup"><span data-stu-id="8178f-114">The table to issue the prereads against.</span></span>

<!-- end list -->

  - <span data-ttu-id="8178f-115">indexRanges</span><span class="sxs-lookup"><span data-stu-id="8178f-115">indexRanges</span></span>  
    <span data-ttu-id="8178f-116">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="8178f-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="8178f-117">Plages de clés à prélire.</span><span class="sxs-lookup"><span data-stu-id="8178f-117">The key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="8178f-118">rangeIndex</span><span class="sxs-lookup"><span data-stu-id="8178f-118">rangeIndex</span></span>  
    <span data-ttu-id="8178f-119">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8178f-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="8178f-120">Index de la première plage de clés dans le tableau à lire.</span><span class="sxs-lookup"><span data-stu-id="8178f-120">The index of the first key range in the array to read.</span></span>

<!-- end list -->

  - <span data-ttu-id="8178f-121">rangeCount</span><span class="sxs-lookup"><span data-stu-id="8178f-121">rangeCount</span></span>  
    <span data-ttu-id="8178f-122">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8178f-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="8178f-123">Nombre maximal de plages de clés à prélire.</span><span class="sxs-lookup"><span data-stu-id="8178f-123">The maximum number of key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="8178f-124">rangesPreread</span><span class="sxs-lookup"><span data-stu-id="8178f-124">rangesPreread</span></span>  
    <span data-ttu-id="8178f-125">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8178f-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="8178f-126">Retourne le nombre de clés réellement prélues.</span><span class="sxs-lookup"><span data-stu-id="8178f-126">Returns the number of keys actually preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="8178f-127">columnsPreread</span><span class="sxs-lookup"><span data-stu-id="8178f-127">columnsPreread</span></span>  
    <span data-ttu-id="8178f-128">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="8178f-128">Type: \[\]</span></span>  
    
    <span data-ttu-id="8178f-129">Liste des ID de colonne pour les colonnes de valeur longue à prélire.</span><span class="sxs-lookup"><span data-stu-id="8178f-129">List of column ids for long value columns to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="8178f-130">grbit</span><span class="sxs-lookup"><span data-stu-id="8178f-130">grbit</span></span>  
    <span data-ttu-id="8178f-131">Tapez : [Microsoft. ISAM. esent. Interop. Windows8. PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="8178f-131">Type: [Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="8178f-132">Options de prélecture.</span><span class="sxs-lookup"><span data-stu-id="8178f-132">Preread options.</span></span> <span data-ttu-id="8178f-133">Utilisé pour spécifier la direction de la prélecture.</span><span class="sxs-lookup"><span data-stu-id="8178f-133">Used to specify the direction of the preread.</span></span>

## <a name="see-also"></a><span data-ttu-id="8178f-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8178f-134">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8178f-135">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="8178f-135">Reference</span></span>

[<span data-ttu-id="8178f-136">Windows8Api, classe</span><span class="sxs-lookup"><span data-stu-id="8178f-136">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="8178f-137">Membres Windows8Api</span><span class="sxs-lookup"><span data-stu-id="8178f-137">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="8178f-138">Espace de noms Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="8178f-138">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
