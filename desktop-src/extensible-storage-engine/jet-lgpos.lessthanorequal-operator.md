---
description: 'En savoir plus sur : JET_LGPOS. Opérateur LessThanOrEqual'
title: JET_LGPOS. Opérateur LessThanOrEqual
TOCTitle: 'LessThanOrEqual operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.op_LessThanOrEqual(Microsoft.Isam.Esent.Interop.JET_LGPOS,Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.op_lessthanorequal(v=EXCHG.10)
ms:contentKeyID: 39510104
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.LessThanOrEqual
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.LessThanOrEqual
- Microsoft.Isam.Esent.Interop.JET_LGPOS.op_LessThanOrEqual
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 57eb2f9383b218409ebee927cc4d6ad1283f3e8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536183"
---
# <a name="jet_lgposlessthanorequal-operator"></a><span data-ttu-id="b1e99-103">JET_LGPOS. Opérateur LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="b1e99-103">JET_LGPOS.LessThanOrEqual operator</span></span>

<span data-ttu-id="b1e99-104">Détermine si une position de journal est antérieure ou égale à une autre position de journal.</span><span class="sxs-lookup"><span data-stu-id="b1e99-104">Determine whether one log position is before or equal to another log position.</span></span>

<span data-ttu-id="b1e99-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b1e99-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b1e99-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b1e99-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b1e99-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1e99-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <= ( _
    lhs As JET_LGPOS, _
    rhs As JET_LGPOS _
) As Boolean
'Usage
Dim lhs As JET_LGPOS
Dim rhs As JET_LGPOS
Dim returnValue As Boolean

returnValue = (lhs <= rhs)
```

``` csharp
public static bool operator <=(
    JET_LGPOS lhs,
    JET_LGPOS rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="b1e99-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1e99-108">Parameters</span></span>

  - <span data-ttu-id="b1e99-109">LHS</span><span class="sxs-lookup"><span data-stu-id="b1e99-109">lhs</span></span>  
    <span data-ttu-id="b1e99-110">Type : [Microsoft.ISAM.esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="b1e99-110">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="b1e99-111">Première position du journal à comparer.</span><span class="sxs-lookup"><span data-stu-id="b1e99-111">The first log position to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="b1e99-112">rhs</span><span class="sxs-lookup"><span data-stu-id="b1e99-112">rhs</span></span>  
    <span data-ttu-id="b1e99-113">Type : [Microsoft.ISAM.esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="b1e99-113">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="b1e99-114">Deuxième position du journal à comparer.</span><span class="sxs-lookup"><span data-stu-id="b1e99-114">The second log position to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b1e99-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b1e99-115">Return value</span></span>

<span data-ttu-id="b1e99-116">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="b1e99-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="b1e99-117">True si LHS précède ou est égal à RHS.</span><span class="sxs-lookup"><span data-stu-id="b1e99-117">True if lhs comes before or is equal to rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b1e99-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1e99-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b1e99-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="b1e99-119">Reference</span></span>

[<span data-ttu-id="b1e99-120">Structure JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="b1e99-120">JET_LGPOS structure</span></span>](./jet-lgpos-structure2.md)

[<span data-ttu-id="b1e99-121">Membres JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="b1e99-121">JET_LGPOS members</span></span>](./jet-lgpos-members.md)

[<span data-ttu-id="b1e99-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b1e99-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
