---
description: 'En savoir plus sur : JET_BKLOGTIME. Opérateur d’inégalité'
title: JET_BKLOGTIME. Opérateur d’inégalité
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.op_Inequality(Microsoft.Isam.Esent.Interop.JET_BKLOGTIME,Microsoft.Isam.Esent.Interop.JET_BKLOGTIME)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bklogtime.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39512908
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.Inequality
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.op_Inequality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 42f13a1068543caaa590015151b523c1a441c806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545081"
---
# <a name="jet_bklogtimeinequality-operator"></a><span data-ttu-id="f8759-103">JET_BKLOGTIME. Opérateur d’inégalité</span><span class="sxs-lookup"><span data-stu-id="f8759-103">JET_BKLOGTIME.Inequality operator</span></span>

<span data-ttu-id="f8759-104">Détermine si deux instances spécifiées de JET_BKLOGTIME ne sont pas égales.</span><span class="sxs-lookup"><span data-stu-id="f8759-104">Determines whether two specified instances of JET_BKLOGTIME are not equal.</span></span>

<span data-ttu-id="f8759-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f8759-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f8759-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f8759-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f8759-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8759-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_BKLOGTIME, _
    rhs As JET_BKLOGTIME _
) As Boolean
'Usage
Dim lhs As JET_BKLOGTIME
Dim rhs As JET_BKLOGTIME
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_BKLOGTIME lhs,
    JET_BKLOGTIME rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="f8759-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8759-108">Parameters</span></span>

  - <span data-ttu-id="f8759-109">LHS</span><span class="sxs-lookup"><span data-stu-id="f8759-109">lhs</span></span>  
    <span data-ttu-id="f8759-110">Type : [Microsoft.ISAM.esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="f8759-110">Type: [Microsoft.Isam.Esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span></span>  
    
    <span data-ttu-id="f8759-111">Première instance à comparer.</span><span class="sxs-lookup"><span data-stu-id="f8759-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="f8759-112">rhs</span><span class="sxs-lookup"><span data-stu-id="f8759-112">rhs</span></span>  
    <span data-ttu-id="f8759-113">Type : [Microsoft.ISAM.esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="f8759-113">Type: [Microsoft.Isam.Esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span></span>  
    
    <span data-ttu-id="f8759-114">Deuxième instance à comparer.</span><span class="sxs-lookup"><span data-stu-id="f8759-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f8759-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f8759-115">Return value</span></span>

<span data-ttu-id="f8759-116">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="f8759-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="f8759-117">True si les deux instances ne sont pas égales.</span><span class="sxs-lookup"><span data-stu-id="f8759-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f8759-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8759-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f8759-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="f8759-119">Reference</span></span>

[<span data-ttu-id="f8759-120">Structure JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="f8759-120">JET_BKLOGTIME structure</span></span>](./jet-bklogtime-structure2.md)

[<span data-ttu-id="f8759-121">Membres JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="f8759-121">JET_BKLOGTIME members</span></span>](./jet-bklogtime-members.md)

[<span data-ttu-id="f8759-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f8759-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
