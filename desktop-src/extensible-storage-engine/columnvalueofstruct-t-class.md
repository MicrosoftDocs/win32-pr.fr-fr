---
description: 'En savoir plus sur : <T> classe ColumnValueOfStruct'
title: ColumnValueOfStruct(T), classe
TOCTitle: ColumnValueOfStruct(T) class
ms:assetid: T:Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
ms:mtpsurl: https://msdn.microsoft.com/library/Dn334171(v=EXCHG.10)
ms:contentKeyID: 55100962
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 82083adcaaf0d9f5b4f2a720da83e95cd4b39401
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104321413"
---
# <a name="columnvalueofstructt-class"></a><span data-ttu-id="42388-103">ColumnValueOfStruct, \<T\> classe</span><span class="sxs-lookup"><span data-stu-id="42388-103">ColumnValueOfStruct\<T\> class</span></span>

<span data-ttu-id="42388-104">Définissez une colonne d’un type struct (par exemple, Int32/GUID).</span><span class="sxs-lookup"><span data-stu-id="42388-104">Set a column of a struct type (e.g. Int32/Guid).</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="42388-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="42388-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="42388-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="42388-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="42388-107">Microsoft. ISAM. esent. Interop. ColumnValue</span><span class="sxs-lookup"><span data-stu-id="42388-107">Microsoft.Isam.Esent.Interop.ColumnValue</span></span>](./columnvalue-class.md)  
    <span data-ttu-id="42388-108">Microsoft. ISAM. esent. Interop. ColumnValueOfStruct\<T\></span><span class="sxs-lookup"><span data-stu-id="42388-108">Microsoft.Isam.Esent.Interop.ColumnValueOfStruct\<T\></span></span>  
      

<span data-ttu-id="42388-109">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="42388-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="42388-110">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="42388-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="42388-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42388-111">Syntax</span></span>

``` vb
'Declaration
Public MustInherit Class ColumnValueOfStruct(Of T As {Structure, New, IEquatable(Of T)}) _
    Inherits ColumnValue
'Usage
Dim instance As ColumnValueOfStruct(Of T)
```

``` csharp
public abstract class ColumnValueOfStruct<T> : ColumnValue
where T : struct, new(), IEquatable<T>
```

#### <a name="type-parameters"></a><span data-ttu-id="42388-112">Paramètres de type</span><span class="sxs-lookup"><span data-stu-id="42388-112">Type parameters</span></span>

  - <span data-ttu-id="42388-113">T</span><span class="sxs-lookup"><span data-stu-id="42388-113">T</span></span>  
    <span data-ttu-id="42388-114">Type à définir.</span><span class="sxs-lookup"><span data-stu-id="42388-114">Type to set.</span></span>

## <a name="thread-safety"></a><span data-ttu-id="42388-115">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="42388-115">Thread safety</span></span>

<span data-ttu-id="42388-116">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="42388-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="42388-117">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="42388-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="42388-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42388-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="42388-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="42388-119">Reference</span></span>

[<span data-ttu-id="42388-120">\<T\>Membres ColumnValueOfStruct</span><span class="sxs-lookup"><span data-stu-id="42388-120">ColumnValueOfStruct\<T\> members</span></span>](./columnvalueofstruct-t-members.md)

[<span data-ttu-id="42388-121">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="42388-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="42388-122">Types dérivés</span><span class="sxs-lookup"><span data-stu-id="42388-122">Derived types</span></span>

[<span data-ttu-id="42388-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="42388-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="42388-124">Microsoft. ISAM. esent. Interop. ColumnValue</span><span class="sxs-lookup"><span data-stu-id="42388-124">Microsoft.Isam.Esent.Interop.ColumnValue</span></span>](./columnvalue-class.md)  
    <span data-ttu-id="42388-125">Microsoft. ISAM. esent. Interop. ColumnValueOfStruct\<T\></span><span class="sxs-lookup"><span data-stu-id="42388-125">Microsoft.Isam.Esent.Interop.ColumnValueOfStruct\<T\></span></span>  
      [<span data-ttu-id="42388-126">Microsoft. ISAM. esent. Interop. BoolColumnValue</span><span class="sxs-lookup"><span data-stu-id="42388-126">Microsoft.Isam.Esent.Interop.BoolColumnValue</span></span>](./boolcolumnvalue-class.md)  
      [<span data-ttu-id="42388-127">Microsoft. ISAM. esent. Interop. ByteColumnValue</span><span class="sxs-lookup"><span data-stu-id="42388-127">Microsoft.Isam.Esent.Interop.ByteColumnValue</span></span>](./bytecolumnvalue-class.md)  
      [<span data-ttu-id="42388-128">Microsoft. ISAM. esent. Interop. DateTimeColumnValue</span><span class="sxs-lookup"><span data-stu-id="42388-128">Microsoft.Isam.Esent.Interop.DateTimeColumnValue</span></span>](./datetimecolumnvalue-class.md)  
      [<span data-ttu-id="42388-129">Microsoft. ISAM. esent. Interop. DoubleColumnValue</span><span class="sxs-lookup"><span data-stu-id="42388-129">Microsoft.Isam.Esent.Interop.DoubleColumnValue</span></span>](./doublecolumnvalue-class.md)  
      [<span data-ttu-id="42388-130">Microsoft. ISAM. esent. Interop. FloatColumnValue</span><span class="sxs-lookup"><span data-stu-id="42388-130">Microsoft.Isam.Esent.Interop.FloatColumnValue</span></span>](./floatcolumnvalue-class.md)  
      [<span data-ttu-id="42388-131">Microsoft. ISAM. esent. Interop. GuidColumnValue</span><span class="sxs-lookup"><span data-stu-id="42388-131">Microsoft.Isam.Esent.Interop.GuidColumnValue</span></span>](./guidcolumnvalue-class.md)  
      [<span data-ttu-id="42388-132">Microsoft. ISAM. esent. Interop. Int16ColumnValue</span><span class="sxs-lookup"><span data-stu-id="42388-132">Microsoft.Isam.Esent.Interop.Int16ColumnValue</span></span>](./int16columnvalue-class.md)  
      [<span data-ttu-id="42388-133">Microsoft. ISAM. esent. Interop. Int32ColumnValue</span><span class="sxs-lookup"><span data-stu-id="42388-133">Microsoft.Isam.Esent.Interop.Int32ColumnValue</span></span>](./int32columnvalue-class.md)  
      [<span data-ttu-id="42388-134">Microsoft. ISAM. esent. Interop. Int64ColumnValue</span><span class="sxs-lookup"><span data-stu-id="42388-134">Microsoft.Isam.Esent.Interop.Int64ColumnValue</span></span>](./int64columnvalue-class.md)  
      [<span data-ttu-id="42388-135">Microsoft. ISAM. esent. Interop. UInt16ColumnValue</span><span class="sxs-lookup"><span data-stu-id="42388-135">Microsoft.Isam.Esent.Interop.UInt16ColumnValue</span></span>](./uint16columnvalue-class.md)  
      [<span data-ttu-id="42388-136">Microsoft. ISAM. esent. Interop. UInt32ColumnValue</span><span class="sxs-lookup"><span data-stu-id="42388-136">Microsoft.Isam.Esent.Interop.UInt32ColumnValue</span></span>](./uint32columnvalue-class.md)  
      [<span data-ttu-id="42388-137">Microsoft. ISAM. esent. Interop. UInt64ColumnValue</span><span class="sxs-lookup"><span data-stu-id="42388-137">Microsoft.Isam.Esent.Interop.UInt64ColumnValue</span></span>](./uint64columnvalue-class.md)