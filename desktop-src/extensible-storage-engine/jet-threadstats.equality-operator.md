---
description: 'En savoir plus sur : JET_THREADSTATS. Opérateur d’égalité'
title: JET_THREADSTATS. Opérateur d’égalité (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Equality(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.op_equality(v=EXCHG.10)
ms:contentKeyID: 39515069
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Equality
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 076ae2cfa25f446d8d6200fbee7f53ecf0edea5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528287"
---
# <a name="jet_threadstatsequality-operator"></a><span data-ttu-id="abb9e-103">JET_THREADSTATS. Opérateur d’égalité</span><span class="sxs-lookup"><span data-stu-id="abb9e-103">JET_THREADSTATS.Equality operator</span></span>

<span data-ttu-id="abb9e-104">Détermine si deux instances spécifiées de JET_THREADSTATS sont égales.</span><span class="sxs-lookup"><span data-stu-id="abb9e-104">Determines whether two specified instances of JET_THREADSTATS are equal.</span></span>

<span data-ttu-id="abb9e-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="abb9e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="abb9e-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="abb9e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="abb9e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="abb9e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_THREADSTATS, _
    rhs As JET_THREADSTATS _
) As Boolean
'Usage
Dim lhs As JET_THREADSTATS
Dim rhs As JET_THREADSTATS
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_THREADSTATS lhs,
    JET_THREADSTATS rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="abb9e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="abb9e-108">Parameters</span></span>

  - <span data-ttu-id="abb9e-109">LHS</span><span class="sxs-lookup"><span data-stu-id="abb9e-109">lhs</span></span>  
    <span data-ttu-id="abb9e-110">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="abb9e-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="abb9e-111">Première instance à comparer.</span><span class="sxs-lookup"><span data-stu-id="abb9e-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="abb9e-112">rhs</span><span class="sxs-lookup"><span data-stu-id="abb9e-112">rhs</span></span>  
    <span data-ttu-id="abb9e-113">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="abb9e-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="abb9e-114">Deuxième instance à comparer.</span><span class="sxs-lookup"><span data-stu-id="abb9e-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="abb9e-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="abb9e-115">Return value</span></span>

<span data-ttu-id="abb9e-116">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="abb9e-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="abb9e-117">True si les deux instances sont égales.</span><span class="sxs-lookup"><span data-stu-id="abb9e-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="abb9e-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abb9e-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="abb9e-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="abb9e-119">Reference</span></span>

[<span data-ttu-id="abb9e-120">Structure JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="abb9e-120">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="abb9e-121">Membres JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="abb9e-121">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="abb9e-122">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="abb9e-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
