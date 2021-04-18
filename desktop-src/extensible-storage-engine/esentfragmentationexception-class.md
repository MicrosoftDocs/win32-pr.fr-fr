---
description: 'En savoir plus sur : classe EsentFragmentationException'
title: EsentFragmentationException, classe
TOCTitle: EsentFragmentationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFragmentationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfragmentationexception(v=EXCHG.10)
ms:contentKeyID: 55101771
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 081198a696be9982e1fd8a7e4f1468e6d63d1c97
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106520221"
---
# <a name="esentfragmentationexception-class"></a><span data-ttu-id="8332e-103">EsentFragmentationException, classe</span><span class="sxs-lookup"><span data-stu-id="8332e-103">EsentFragmentationException class</span></span>

<span data-ttu-id="8332e-104">Classe de base pour les exceptions de fragmentation.</span><span class="sxs-lookup"><span data-stu-id="8332e-104">Base class for Fragmentation exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="8332e-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="8332e-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="8332e-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="8332e-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="8332e-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="8332e-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="8332e-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="8332e-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="8332e-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="8332e-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="8332e-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="8332e-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="8332e-111">Microsoft. ISAM. esent. Interop. EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="8332e-111">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>  
            

<span data-ttu-id="8332e-112">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8332e-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8332e-113">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8332e-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8332e-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8332e-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentFragmentationException _
    Inherits EsentDataException
'Usage
Dim instance As EsentFragmentationException
```

``` csharp
[SerializableAttribute]
public abstract class EsentFragmentationException : EsentDataException
```

## <a name="thread-safety"></a><span data-ttu-id="8332e-115">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="8332e-115">Thread safety</span></span>

<span data-ttu-id="8332e-116">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="8332e-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="8332e-117">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="8332e-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="8332e-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8332e-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8332e-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="8332e-119">Reference</span></span>

[<span data-ttu-id="8332e-120">Membres EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="8332e-120">EsentFragmentationException members</span></span>](./esentfragmentationexception-members.md)

[<span data-ttu-id="8332e-121">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8332e-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="8332e-122">Types dérivés</span><span class="sxs-lookup"><span data-stu-id="8332e-122">Derived types</span></span>

[<span data-ttu-id="8332e-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="8332e-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="8332e-124">System.Exception</span><span class="sxs-lookup"><span data-stu-id="8332e-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="8332e-125">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="8332e-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="8332e-126">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="8332e-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="8332e-127">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="8332e-127">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="8332e-128">Microsoft. ISAM. esent. Interop. EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="8332e-128">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>  
            [<span data-ttu-id="8332e-129">Microsoft. ISAM. esent. Interop. EsentLogSectorSizeMismatchException</span><span class="sxs-lookup"><span data-stu-id="8332e-129">Microsoft.Isam.Esent.Interop.EsentLogSectorSizeMismatchException</span></span>](./esentlogsectorsizemismatchexception-class.md)  
            [<span data-ttu-id="8332e-130">Microsoft. ISAM. esent. Interop. EsentLogSequenceEndDatabasesConsistentException</span><span class="sxs-lookup"><span data-stu-id="8332e-130">Microsoft.Isam.Esent.Interop.EsentLogSequenceEndDatabasesConsistentException</span></span>](./esentlogsequenceenddatabasesconsistentexception-class.md)  
            [<span data-ttu-id="8332e-131">Microsoft. ISAM. esent. Interop. EsentLogSequenceEndException</span><span class="sxs-lookup"><span data-stu-id="8332e-131">Microsoft.Isam.Esent.Interop.EsentLogSequenceEndException</span></span>](./esentlogsequenceendexception-class.md)  
            [<span data-ttu-id="8332e-132">Microsoft. ISAM. esent. Interop. EsentOutOfAutoincrementValuesException</span><span class="sxs-lookup"><span data-stu-id="8332e-132">Microsoft.Isam.Esent.Interop.EsentOutOfAutoincrementValuesException</span></span>](./esentoutofautoincrementvaluesexception-class.md)  
            [<span data-ttu-id="8332e-133">Microsoft. ISAM. esent. Interop. EsentOutOfDbtimeValuesException</span><span class="sxs-lookup"><span data-stu-id="8332e-133">Microsoft.Isam.Esent.Interop.EsentOutOfDbtimeValuesException</span></span>](./esentoutofdbtimevaluesexception-class.md)  
            [<span data-ttu-id="8332e-134">Microsoft. ISAM. esent. Interop. EsentOutOfLongValueIDsException</span><span class="sxs-lookup"><span data-stu-id="8332e-134">Microsoft.Isam.Esent.Interop.EsentOutOfLongValueIDsException</span></span>](./esentoutoflongvalueidsexception-class.md)  
            [<span data-ttu-id="8332e-135">Microsoft. ISAM. esent. Interop. EsentOutOfObjectIDsException</span><span class="sxs-lookup"><span data-stu-id="8332e-135">Microsoft.Isam.Esent.Interop.EsentOutOfObjectIDsException</span></span>](./esentoutofobjectidsexception-class.md)  
            [<span data-ttu-id="8332e-136">Microsoft. ISAM. esent. Interop. EsentOutOfSequentialIndexValuesException</span><span class="sxs-lookup"><span data-stu-id="8332e-136">Microsoft.Isam.Esent.Interop.EsentOutOfSequentialIndexValuesException</span></span>](./esentoutofsequentialindexvaluesexception-class.md)