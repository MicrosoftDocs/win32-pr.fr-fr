---
description: 'En savoir plus sur : JET_LS. Opérateur d’inégalité'
title: JET_LS. Opérateur d’inégalité
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LS.op_Inequality(Microsoft.Isam.Esent.Interop.JET_LS,Microsoft.Isam.Esent.Interop.JET_LS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ls.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39512483
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LS.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LS.op_Inequality
- Microsoft.Isam.Esent.Interop.JET_LS.Inequality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: da167f0deda8254d279e7d81c7219b6e9920673f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034915"
---
# <a name="jet_lsinequality-operator"></a><span data-ttu-id="3715b-103">JET_LS. Opérateur d’inégalité</span><span class="sxs-lookup"><span data-stu-id="3715b-103">JET_LS.Inequality operator</span></span>

<span data-ttu-id="3715b-104">Détermine si deux instances spécifiées de JET_LS ne sont pas égales.</span><span class="sxs-lookup"><span data-stu-id="3715b-104">Determines whether two specified instances of JET_LS are not equal.</span></span>

<span data-ttu-id="3715b-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3715b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3715b-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3715b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3715b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3715b-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_LS, _
    rhs As JET_LS _
) As Boolean
'Usage
Dim lhs As JET_LS
Dim rhs As JET_LS
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_LS lhs,
    JET_LS rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="3715b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3715b-108">Parameters</span></span>

  - <span data-ttu-id="3715b-109">LHS</span><span class="sxs-lookup"><span data-stu-id="3715b-109">lhs</span></span>  
    <span data-ttu-id="3715b-110">Type : [Microsoft.ISAM.esent.Interop.JET_LS](./jet-ls-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3715b-110">Type: [Microsoft.Isam.Esent.Interop.JET_LS](./jet-ls-structure.md)</span></span>  
    
    <span data-ttu-id="3715b-111">Première instance à comparer.</span><span class="sxs-lookup"><span data-stu-id="3715b-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="3715b-112">rhs</span><span class="sxs-lookup"><span data-stu-id="3715b-112">rhs</span></span>  
    <span data-ttu-id="3715b-113">Type : [Microsoft.ISAM.esent.Interop.JET_LS](./jet-ls-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3715b-113">Type: [Microsoft.Isam.Esent.Interop.JET_LS](./jet-ls-structure.md)</span></span>  
    
    <span data-ttu-id="3715b-114">Deuxième instance à comparer.</span><span class="sxs-lookup"><span data-stu-id="3715b-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="3715b-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3715b-115">Return value</span></span>

<span data-ttu-id="3715b-116">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="3715b-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="3715b-117">True si les deux instances ne sont pas égales.</span><span class="sxs-lookup"><span data-stu-id="3715b-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3715b-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3715b-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3715b-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="3715b-119">Reference</span></span>

[<span data-ttu-id="3715b-120">Structure JET_LS</span><span class="sxs-lookup"><span data-stu-id="3715b-120">JET_LS structure</span></span>](./jet-ls-structure.md)

[<span data-ttu-id="3715b-121">Membres JET_LS</span><span class="sxs-lookup"><span data-stu-id="3715b-121">JET_LS members</span></span>](./jet-ls-members.md)

[<span data-ttu-id="3715b-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3715b-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
