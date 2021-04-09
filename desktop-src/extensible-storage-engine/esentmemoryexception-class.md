---
description: 'En savoir plus sur : classe EsentMemoryException'
title: Classe EsentMemoryException
TOCTitle: EsentMemoryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMemoryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55102197
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMemoryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMemoryException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6a7090fdedee2969e5dd3658b7068fd8739e9365
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103869374"
---
# <a name="esentmemoryexception-class"></a><span data-ttu-id="ef850-103">Classe EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="ef850-103">EsentMemoryException class</span></span>

<span data-ttu-id="ef850-104">Classe de base pour les exceptions de mémoire.</span><span class="sxs-lookup"><span data-stu-id="ef850-104">Base class for Memory exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ef850-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="ef850-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ef850-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ef850-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ef850-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="ef850-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ef850-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="ef850-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ef850-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="ef850-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ef850-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="ef850-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="ef850-111">Microsoft. ISAM. esent. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="ef850-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            <span data-ttu-id="ef850-112">Microsoft. ISAM. esent. Interop. EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="ef850-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>  
              

<span data-ttu-id="ef850-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ef850-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ef850-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ef850-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ef850-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef850-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentMemoryException _
    Inherits EsentResourceException
'Usage
Dim instance As EsentMemoryException
```

``` csharp
[SerializableAttribute]
public abstract class EsentMemoryException : EsentResourceException
```

## <a name="thread-safety"></a><span data-ttu-id="ef850-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="ef850-116">Thread safety</span></span>

<span data-ttu-id="ef850-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="ef850-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ef850-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="ef850-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ef850-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef850-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ef850-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="ef850-120">Reference</span></span>

[<span data-ttu-id="ef850-121">Membres EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="ef850-121">EsentMemoryException members</span></span>](./esentmemoryexception-members.md)

[<span data-ttu-id="ef850-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ef850-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="ef850-123">Types dérivés</span><span class="sxs-lookup"><span data-stu-id="ef850-123">Derived types</span></span>

[<span data-ttu-id="ef850-124">System.Object</span><span class="sxs-lookup"><span data-stu-id="ef850-124">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ef850-125">System.Exception</span><span class="sxs-lookup"><span data-stu-id="ef850-125">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ef850-126">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="ef850-126">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ef850-127">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="ef850-127">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ef850-128">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="ef850-128">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="ef850-129">Microsoft. ISAM. esent. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="ef850-129">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            <span data-ttu-id="ef850-130">Microsoft. ISAM. esent. Interop. EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="ef850-130">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>  
              [<span data-ttu-id="ef850-131">Microsoft. ISAM. esent. Interop. EsentOutOfBuffersException</span><span class="sxs-lookup"><span data-stu-id="ef850-131">Microsoft.Isam.Esent.Interop.EsentOutOfBuffersException</span></span>](./esentoutofbuffersexception-class.md)  
              [<span data-ttu-id="ef850-132">Microsoft. ISAM. esent. Interop. EsentOutOfCursorsException</span><span class="sxs-lookup"><span data-stu-id="ef850-132">Microsoft.Isam.Esent.Interop.EsentOutOfCursorsException</span></span>](./esentoutofcursorsexception-class.md)  
              [<span data-ttu-id="ef850-133">Microsoft. ISAM. esent. Interop. EsentOutOfFileHandlesException</span><span class="sxs-lookup"><span data-stu-id="ef850-133">Microsoft.Isam.Esent.Interop.EsentOutOfFileHandlesException</span></span>](./esentoutoffilehandlesexception-class.md)  
              [<span data-ttu-id="ef850-134">Microsoft. ISAM. esent. Interop. EsentOutOfMemoryException</span><span class="sxs-lookup"><span data-stu-id="ef850-134">Microsoft.Isam.Esent.Interop.EsentOutOfMemoryException</span></span>](./esentoutofmemoryexception-class.md)  
              [<span data-ttu-id="ef850-135">Microsoft. ISAM. esent. Interop. EsentOutOfSessionsException</span><span class="sxs-lookup"><span data-stu-id="ef850-135">Microsoft.Isam.Esent.Interop.EsentOutOfSessionsException</span></span>](./esentoutofsessionsexception-class.md)  
              [<span data-ttu-id="ef850-136">Microsoft. ISAM. esent. Interop. EsentOutOfThreadsException</span><span class="sxs-lookup"><span data-stu-id="ef850-136">Microsoft.Isam.Esent.Interop.EsentOutOfThreadsException</span></span>](./esentoutofthreadsexception-class.md)  
              [<span data-ttu-id="ef850-137">Microsoft. ISAM. esent. Interop. EsentTooManyMempoolEntriesException</span><span class="sxs-lookup"><span data-stu-id="ef850-137">Microsoft.Isam.Esent.Interop.EsentTooManyMempoolEntriesException</span></span>](./esenttoomanymempoolentriesexception-class.md)  
              [<span data-ttu-id="ef850-138">Microsoft. ISAM. esent. Interop. EsentTooManyOpenIndexesException</span><span class="sxs-lookup"><span data-stu-id="ef850-138">Microsoft.Isam.Esent.Interop.EsentTooManyOpenIndexesException</span></span>](./esenttoomanyopenindexesexception-class.md)  
              [<span data-ttu-id="ef850-139">Microsoft. ISAM. esent. Interop. EsentTooManySortsException</span><span class="sxs-lookup"><span data-stu-id="ef850-139">Microsoft.Isam.Esent.Interop.EsentTooManySortsException</span></span>](./esenttoomanysortsexception-class.md)