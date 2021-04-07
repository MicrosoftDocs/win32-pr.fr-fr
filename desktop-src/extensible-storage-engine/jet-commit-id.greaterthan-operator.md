---
description: 'En savoir plus sur : opérateur JET_COMMIT_ID. GreaterThan'
title: JET_COMMIT_ID. GreaterThan, opérateur (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'GreaterThan operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_GreaterThan(Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_commit_id.op_greaterthan(v=EXCHG.10)
ms:contentKeyID: 55104406
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.GreaterThan
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.GreaterThan
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_GreaterThan
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bfcb6cdc5a07cd4c114d5f61aaf597711636526b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757947"
---
# <a name="jet_commit_idgreaterthan-operator"></a><span data-ttu-id="a7960-103">JET_COMMIT_ID. GreaterThan (opérateur)</span><span class="sxs-lookup"><span data-stu-id="a7960-103">JET_COMMIT_ID.GreaterThan operator</span></span>

<span data-ttu-id="a7960-104">Déterminez si un commitid est avant un autre commitid.</span><span class="sxs-lookup"><span data-stu-id="a7960-104">Determine whether one commitid is before another commitid.</span></span>

<span data-ttu-id="a7960-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a7960-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="a7960-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a7960-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a7960-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a7960-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator > ( _
    lhs As JET_COMMIT_ID, _
    rhs As JET_COMMIT_ID _
) As Boolean
'Usage
Dim lhs As JET_COMMIT_ID
Dim rhs As JET_COMMIT_ID
Dim returnValue As Boolean

returnValue = (lhs > rhs)
```

``` csharp
public static bool operator >(
    JET_COMMIT_ID lhs,
    JET_COMMIT_ID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="a7960-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a7960-108">Parameters</span></span>

  - <span data-ttu-id="a7960-109">LHS</span><span class="sxs-lookup"><span data-stu-id="a7960-109">lhs</span></span>  
    <span data-ttu-id="a7960-110">Type : [Microsoft.ISAM.esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="a7960-110">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="a7960-111">Premier commitid à comparer.</span><span class="sxs-lookup"><span data-stu-id="a7960-111">The first commitid to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="a7960-112">rhs</span><span class="sxs-lookup"><span data-stu-id="a7960-112">rhs</span></span>  
    <span data-ttu-id="a7960-113">Type : [Microsoft.ISAM.esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="a7960-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="a7960-114">Deuxième commitid à comparer.</span><span class="sxs-lookup"><span data-stu-id="a7960-114">The second commitid to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="a7960-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a7960-115">Return value</span></span>

<span data-ttu-id="a7960-116">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="a7960-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="a7960-117">True si LHS vient après RHS.</span><span class="sxs-lookup"><span data-stu-id="a7960-117">True if lhs comes after rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a7960-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7960-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a7960-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="a7960-119">Reference</span></span>

[<span data-ttu-id="a7960-120">Classe JET_COMMIT_ID</span><span class="sxs-lookup"><span data-stu-id="a7960-120">JET_COMMIT_ID class</span></span>](./jet-commit-id-class.md)

[<span data-ttu-id="a7960-121">Membres JET_COMMIT_ID</span><span class="sxs-lookup"><span data-stu-id="a7960-121">JET_COMMIT_ID members</span></span>](./jet-commit-id-members.md)

[<span data-ttu-id="a7960-122">Espace de noms Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="a7960-122">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
