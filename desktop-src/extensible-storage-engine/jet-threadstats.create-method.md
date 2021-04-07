---
description: 'En savoir plus sur : JET_THREADSTATS. Créer une méthode'
title: JET_THREADSTATS. Create, méthode (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'Create method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create(System.Int32,System.Int32,System.Int32,System.Int32,System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.create(v=EXCHG.10)
ms:contentKeyID: 39509886
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: beaaee85fc0f6c331db1d813280d4b900e39fb54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758493"
---
# <a name="jet_threadstatscreate-method"></a><span data-ttu-id="fad74-103">JET_THREADSTATS. Créer une méthode</span><span class="sxs-lookup"><span data-stu-id="fad74-103">JET_THREADSTATS.Create method</span></span>

<span data-ttu-id="fad74-104">Crée un nouveau [JET_THREADSTATS](./jet-threadstats-structure2.md) structure avec la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="fad74-104">Create a new [JET_THREADSTATS](./jet-threadstats-structure2.md) struct with the specified valued.</span></span>

<span data-ttu-id="fad74-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fad74-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="fad74-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fad74-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fad74-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fad74-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function Create ( _
    cPageReferenced As Integer, _
    cPageRead As Integer, _
    cPagePreread As Integer, _
    cPageDirtied As Integer, _
    cPageRedirtied As Integer, _
    cLogRecord As Integer, _
    cbLogRecord As Integer _
) As JET_THREADSTATS
'Usage
Dim cPageReferenced As Integer
Dim cPageRead As Integer
Dim cPagePreread As Integer
Dim cPageDirtied As Integer
Dim cPageRedirtied As Integer
Dim cLogRecord As Integer
Dim cbLogRecord As Integer
Dim returnValue As JET_THREADSTATS

returnValue = JET_THREADSTATS.Create(cPageReferenced, _
    cPageRead, cPagePreread, cPageDirtied, _
    cPageRedirtied, cLogRecord, cbLogRecord)
```

``` csharp
public static JET_THREADSTATS Create(
    int cPageReferenced,
    int cPageRead,
    int cPagePreread,
    int cPageDirtied,
    int cPageRedirtied,
    int cLogRecord,
    int cbLogRecord
)
```

#### <a name="parameters"></a><span data-ttu-id="fad74-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fad74-108">Parameters</span></span>

  - <span data-ttu-id="fad74-109">cPageReferenced</span><span class="sxs-lookup"><span data-stu-id="fad74-109">cPageReferenced</span></span>  
    <span data-ttu-id="fad74-110">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="fad74-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="fad74-111">Nombre de pages visitées.</span><span class="sxs-lookup"><span data-stu-id="fad74-111">Number of pages visited.</span></span>

<!-- end list -->

  - <span data-ttu-id="fad74-112">cPageRead</span><span class="sxs-lookup"><span data-stu-id="fad74-112">cPageRead</span></span>  
    <span data-ttu-id="fad74-113">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="fad74-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="fad74-114">Nombre de pages lues.</span><span class="sxs-lookup"><span data-stu-id="fad74-114">Number of pages read.</span></span>

<!-- end list -->

  - <span data-ttu-id="fad74-115">cPagePreread</span><span class="sxs-lookup"><span data-stu-id="fad74-115">cPagePreread</span></span>  
    <span data-ttu-id="fad74-116">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="fad74-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="fad74-117">Nombre de pages prélues.</span><span class="sxs-lookup"><span data-stu-id="fad74-117">Number of pages preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="fad74-118">cPageDirtied</span><span class="sxs-lookup"><span data-stu-id="fad74-118">cPageDirtied</span></span>  
    <span data-ttu-id="fad74-119">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="fad74-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="fad74-120">TNumber de pages modifiées.</span><span class="sxs-lookup"><span data-stu-id="fad74-120">TNumber of pages dirtied.</span></span>

<!-- end list -->

  - <span data-ttu-id="fad74-121">cPageRedirtied</span><span class="sxs-lookup"><span data-stu-id="fad74-121">cPageRedirtied</span></span>  
    <span data-ttu-id="fad74-122">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="fad74-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="fad74-123">Nombre de pages Remodifiées.</span><span class="sxs-lookup"><span data-stu-id="fad74-123">Number of pages redirtied.</span></span>

<!-- end list -->

  - <span data-ttu-id="fad74-124">cLogRecord</span><span class="sxs-lookup"><span data-stu-id="fad74-124">cLogRecord</span></span>  
    <span data-ttu-id="fad74-125">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="fad74-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="fad74-126">Nombre d’enregistrements de journal générés.</span><span class="sxs-lookup"><span data-stu-id="fad74-126">Number of log records generated.</span></span>

<!-- end list -->

  - <span data-ttu-id="fad74-127">cbLogRecord</span><span class="sxs-lookup"><span data-stu-id="fad74-127">cbLogRecord</span></span>  
    <span data-ttu-id="fad74-128">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="fad74-128">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="fad74-129">Octets des enregistrements de journal écrits.</span><span class="sxs-lookup"><span data-stu-id="fad74-129">Bytes of log records written.</span></span>

#### <a name="return-value"></a><span data-ttu-id="fad74-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fad74-130">Return value</span></span>

<span data-ttu-id="fad74-131">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="fad74-131">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
<span data-ttu-id="fad74-132">Nouvelle [JET_THREADSTATS](./jet-threadstats-structure2.md) structure avec les valeurs spécifiées.</span><span class="sxs-lookup"><span data-stu-id="fad74-132">A new [JET_THREADSTATS](./jet-threadstats-structure2.md) struct with the specified values.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fad74-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fad74-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fad74-134">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="fad74-134">Reference</span></span>

[<span data-ttu-id="fad74-135">Structure JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="fad74-135">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="fad74-136">Membres JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="fad74-136">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="fad74-137">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="fad74-137">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
