---
description: 'En savoir plus sur : JET_SIGNATURE. Opérateur d’égalité'
title: JET_SIGNATURE. Opérateur d’égalité
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SIGNATURE.op_Equality(Microsoft.Isam.Esent.Interop.JET_SIGNATURE,Microsoft.Isam.Esent.Interop.JET_SIGNATURE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_signature.op_equality(v=EXCHG.10)
ms:contentKeyID: 39512803
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.op_Equality
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 011510343f79724c2c529c2b6b18537b43facbef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752468"
---
# <a name="jet_signatureequality-operator"></a><span data-ttu-id="c93d1-103">JET_SIGNATURE. Opérateur d’égalité</span><span class="sxs-lookup"><span data-stu-id="c93d1-103">JET_SIGNATURE.Equality operator</span></span>

<span data-ttu-id="c93d1-104">Détermine si deux instances spécifiées de JET_SIGNATURE sont égales.</span><span class="sxs-lookup"><span data-stu-id="c93d1-104">Determines whether two specified instances of JET_SIGNATURE are equal.</span></span>

<span data-ttu-id="c93d1-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c93d1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c93d1-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c93d1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c93d1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c93d1-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_SIGNATURE, _
    rhs As JET_SIGNATURE _
) As Boolean
'Usage
Dim lhs As JET_SIGNATURE
Dim rhs As JET_SIGNATURE
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_SIGNATURE lhs,
    JET_SIGNATURE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="c93d1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c93d1-108">Parameters</span></span>

  - <span data-ttu-id="c93d1-109">LHS</span><span class="sxs-lookup"><span data-stu-id="c93d1-109">lhs</span></span>  
    <span data-ttu-id="c93d1-110">Type : [Microsoft.ISAM.esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="c93d1-110">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="c93d1-111">Première instance à comparer.</span><span class="sxs-lookup"><span data-stu-id="c93d1-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="c93d1-112">rhs</span><span class="sxs-lookup"><span data-stu-id="c93d1-112">rhs</span></span>  
    <span data-ttu-id="c93d1-113">Type : [Microsoft.ISAM.esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="c93d1-113">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="c93d1-114">Deuxième instance à comparer.</span><span class="sxs-lookup"><span data-stu-id="c93d1-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="c93d1-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c93d1-115">Return value</span></span>

<span data-ttu-id="c93d1-116">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="c93d1-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="c93d1-117">True si les deux instances sont égales.</span><span class="sxs-lookup"><span data-stu-id="c93d1-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c93d1-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c93d1-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c93d1-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="c93d1-119">Reference</span></span>

[<span data-ttu-id="c93d1-120">Structure JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="c93d1-120">JET_SIGNATURE structure</span></span>](./jet-signature-structure2.md)

[<span data-ttu-id="c93d1-121">Membres JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="c93d1-121">JET_SIGNATURE members</span></span>](./jet-signature-members.md)

[<span data-ttu-id="c93d1-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c93d1-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
