---
description: 'En savoir plus sur : JET_COLUMNID. LessThan, opérateur'
title: JET_COLUMNID. LessThan, opérateur
TOCTitle: 'LessThan operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_LessThan(Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.op_lessthan(v=EXCHG.10)
ms:contentKeyID: 39512911
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.LessThan
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.LessThan
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_LessThan
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 263cb7be0377da007e6294b29701613628ec692d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517441"
---
# <a name="jet_columnidlessthan-operator"></a><span data-ttu-id="beadd-103">JET_COLUMNID. LessThan, opérateur</span><span class="sxs-lookup"><span data-stu-id="beadd-103">JET_COLUMNID.LessThan operator</span></span>

<span data-ttu-id="beadd-104">Détermine si un ColumnID est antérieur à un autre ColumnID.</span><span class="sxs-lookup"><span data-stu-id="beadd-104">Determine whether one columnid is before another columnid.</span></span>

<span data-ttu-id="beadd-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="beadd-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="beadd-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="beadd-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="beadd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="beadd-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator < ( _
    lhs As JET_COLUMNID, _
    rhs As JET_COLUMNID _
) As Boolean
'Usage
Dim lhs As JET_COLUMNID
Dim rhs As JET_COLUMNID
Dim returnValue As Boolean

returnValue = (lhs < rhs)
```

``` csharp
public static bool operator <(
    JET_COLUMNID lhs,
    JET_COLUMNID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="beadd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="beadd-108">Parameters</span></span>

  - <span data-ttu-id="beadd-109">LHS</span><span class="sxs-lookup"><span data-stu-id="beadd-109">lhs</span></span>  
    <span data-ttu-id="beadd-110">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="beadd-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="beadd-111">Premier ColumnID à comparer.</span><span class="sxs-lookup"><span data-stu-id="beadd-111">The first columnid to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="beadd-112">rhs</span><span class="sxs-lookup"><span data-stu-id="beadd-112">rhs</span></span>  
    <span data-ttu-id="beadd-113">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="beadd-113">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="beadd-114">Deuxième ColumnID à comparer.</span><span class="sxs-lookup"><span data-stu-id="beadd-114">The second columnid to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="beadd-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="beadd-115">Return value</span></span>

<span data-ttu-id="beadd-116">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="beadd-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="beadd-117">True si LHS vient avant RHS.</span><span class="sxs-lookup"><span data-stu-id="beadd-117">True if lhs comes before rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="beadd-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="beadd-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="beadd-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="beadd-119">Reference</span></span>

[<span data-ttu-id="beadd-120">Structure JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="beadd-120">JET_COLUMNID structure</span></span>](./jet-columnid-structure.md)

[<span data-ttu-id="beadd-121">Membres JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="beadd-121">JET_COLUMNID members</span></span>](./jet-columnid-members.md)

[<span data-ttu-id="beadd-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="beadd-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
