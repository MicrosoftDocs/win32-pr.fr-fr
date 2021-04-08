---
description: 'En savoir plus sur : JET_RECSIZE. Opérateur d’égalité'
title: JET_RECSIZE. Opérateur d’égalité (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Equality(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.op_equality(v=EXCHG.10)
ms:contentKeyID: 39515439
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Equality
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2f95ee6975a71e40d702b1f68c47ad6831881ffa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112083"
---
# <a name="jet_recsizeequality-operator"></a><span data-ttu-id="4234f-103">JET_RECSIZE. Opérateur d’égalité</span><span class="sxs-lookup"><span data-stu-id="4234f-103">JET_RECSIZE.Equality operator</span></span>

<span data-ttu-id="4234f-104">Détermine si deux instances spécifiées de JET_RECSIZE sont égales.</span><span class="sxs-lookup"><span data-stu-id="4234f-104">Determines whether two specified instances of JET_RECSIZE are equal.</span></span>

<span data-ttu-id="4234f-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4234f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="4234f-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4234f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4234f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4234f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_RECSIZE, _
    rhs As JET_RECSIZE _
) As Boolean
'Usage
Dim lhs As JET_RECSIZE
Dim rhs As JET_RECSIZE
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_RECSIZE lhs,
    JET_RECSIZE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="4234f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4234f-108">Parameters</span></span>

  - <span data-ttu-id="4234f-109">LHS</span><span class="sxs-lookup"><span data-stu-id="4234f-109">lhs</span></span>  
    <span data-ttu-id="4234f-110">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="4234f-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="4234f-111">Première instance à comparer.</span><span class="sxs-lookup"><span data-stu-id="4234f-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="4234f-112">rhs</span><span class="sxs-lookup"><span data-stu-id="4234f-112">rhs</span></span>  
    <span data-ttu-id="4234f-113">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="4234f-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="4234f-114">Deuxième instance à comparer.</span><span class="sxs-lookup"><span data-stu-id="4234f-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="4234f-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4234f-115">Return value</span></span>

<span data-ttu-id="4234f-116">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="4234f-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="4234f-117">True si les deux instances sont égales.</span><span class="sxs-lookup"><span data-stu-id="4234f-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4234f-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4234f-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4234f-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="4234f-119">Reference</span></span>

[<span data-ttu-id="4234f-120">Structure JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="4234f-120">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="4234f-121">Membres JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="4234f-121">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="4234f-122">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="4234f-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
