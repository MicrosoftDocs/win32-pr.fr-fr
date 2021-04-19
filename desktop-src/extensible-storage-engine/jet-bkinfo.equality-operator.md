---
description: 'En savoir plus sur : JET_BKINFO. Opérateur d’égalité'
title: JET_BKINFO. Opérateur d’égalité
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_BKINFO.op_Equality(Microsoft.Isam.Esent.Interop.JET_BKINFO,Microsoft.Isam.Esent.Interop.JET_BKINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bkinfo.op_equality(v=EXCHG.10)
ms:contentKeyID: 39510688
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKINFO.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKINFO.op_Equality
- Microsoft.Isam.Esent.Interop.JET_BKINFO.Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a20cc09e55ce2bbb194561d4e371b81f9bcb2a6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534725"
---
# <a name="jet_bkinfoequality-operator"></a><span data-ttu-id="eb8a6-103">JET_BKINFO. Opérateur d’égalité</span><span class="sxs-lookup"><span data-stu-id="eb8a6-103">JET_BKINFO.Equality operator</span></span>

<span data-ttu-id="eb8a6-104">Détermine si deux instances spécifiées de JET_BKINFO sont égales.</span><span class="sxs-lookup"><span data-stu-id="eb8a6-104">Determines whether two specified instances of JET_BKINFO are equal.</span></span>

<span data-ttu-id="eb8a6-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="eb8a6-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="eb8a6-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="eb8a6-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="eb8a6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb8a6-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_BKINFO, _
    rhs As JET_BKINFO _
) As Boolean
'Usage
Dim lhs As JET_BKINFO
Dim rhs As JET_BKINFO
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_BKINFO lhs,
    JET_BKINFO rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="eb8a6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb8a6-108">Parameters</span></span>

  - <span data-ttu-id="eb8a6-109">LHS</span><span class="sxs-lookup"><span data-stu-id="eb8a6-109">lhs</span></span>  
    <span data-ttu-id="eb8a6-110">Type : [Microsoft.ISAM.esent.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="eb8a6-110">Type: [Microsoft.Isam.Esent.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span></span>  
    
    <span data-ttu-id="eb8a6-111">Première instance à comparer.</span><span class="sxs-lookup"><span data-stu-id="eb8a6-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="eb8a6-112">rhs</span><span class="sxs-lookup"><span data-stu-id="eb8a6-112">rhs</span></span>  
    <span data-ttu-id="eb8a6-113">Type : [Microsoft.ISAM.esent.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="eb8a6-113">Type: [Microsoft.Isam.Esent.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span></span>  
    
    <span data-ttu-id="eb8a6-114">Deuxième instance à comparer.</span><span class="sxs-lookup"><span data-stu-id="eb8a6-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="eb8a6-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb8a6-115">Return value</span></span>

<span data-ttu-id="eb8a6-116">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="eb8a6-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="eb8a6-117">True si les deux instances sont égales.</span><span class="sxs-lookup"><span data-stu-id="eb8a6-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="eb8a6-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb8a6-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="eb8a6-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="eb8a6-119">Reference</span></span>

[<span data-ttu-id="eb8a6-120">Structure JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="eb8a6-120">JET_BKINFO structure</span></span>](./jet-bkinfo-structure2.md)

[<span data-ttu-id="eb8a6-121">Membres JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="eb8a6-121">JET_BKINFO members</span></span>](./jet-bkinfo-members.md)

[<span data-ttu-id="eb8a6-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="eb8a6-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
