---
description: 'En savoir plus sur : JET_INSTANCE. Opérateur d’égalité'
title: JET_INSTANCE. Opérateur d’égalité
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE.op_Equality(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance.op_equality(v=EXCHG.10)
ms:contentKeyID: 39512671
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.Equality
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.op_Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 41a3ffe2eebeb7566d431c655a27360c9380413c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536163"
---
# <a name="jet_instanceequality-operator"></a><span data-ttu-id="b4169-103">JET_INSTANCE. Opérateur d’égalité</span><span class="sxs-lookup"><span data-stu-id="b4169-103">JET_INSTANCE.Equality operator</span></span>

<span data-ttu-id="b4169-104">Détermine si deux instances spécifiées de JET_INSTANCE sont égales.</span><span class="sxs-lookup"><span data-stu-id="b4169-104">Determines whether two specified instances of JET_INSTANCE are equal.</span></span>

<span data-ttu-id="b4169-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b4169-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b4169-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b4169-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b4169-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4169-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_INSTANCE, _
    rhs As JET_INSTANCE _
) As Boolean
'Usage
Dim lhs As JET_INSTANCE
Dim rhs As JET_INSTANCE
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_INSTANCE lhs,
    JET_INSTANCE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="b4169-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4169-108">Parameters</span></span>

  - <span data-ttu-id="b4169-109">LHS</span><span class="sxs-lookup"><span data-stu-id="b4169-109">lhs</span></span>  
    <span data-ttu-id="b4169-110">Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b4169-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="b4169-111">Première instance à comparer.</span><span class="sxs-lookup"><span data-stu-id="b4169-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="b4169-112">rhs</span><span class="sxs-lookup"><span data-stu-id="b4169-112">rhs</span></span>  
    <span data-ttu-id="b4169-113">Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b4169-113">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="b4169-114">Deuxième instance à comparer.</span><span class="sxs-lookup"><span data-stu-id="b4169-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b4169-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b4169-115">Return value</span></span>

<span data-ttu-id="b4169-116">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="b4169-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="b4169-117">True si les deux instances sont égales.</span><span class="sxs-lookup"><span data-stu-id="b4169-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b4169-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4169-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b4169-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="b4169-119">Reference</span></span>

[<span data-ttu-id="b4169-120">Structure JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="b4169-120">JET_INSTANCE structure</span></span>](./jet-instance-structure.md)

[<span data-ttu-id="b4169-121">Membres JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="b4169-121">JET_INSTANCE members</span></span>](./jet-instance-members.md)

[<span data-ttu-id="b4169-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b4169-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
