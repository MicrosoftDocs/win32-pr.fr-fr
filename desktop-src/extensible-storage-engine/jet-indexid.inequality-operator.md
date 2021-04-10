---
description: 'En savoir plus sur : JET_INDEXID. Opérateur d’inégalité'
title: JET_INDEXID. Opérateur d’inégalité
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INDEXID.op_Inequality(Microsoft.Isam.Esent.Interop.JET_INDEXID,Microsoft.Isam.Esent.Interop.JET_INDEXID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexid.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39510422
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXID.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXID.op_Inequality
- Microsoft.Isam.Esent.Interop.JET_INDEXID.Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f08dc8d80a9d62a0cb837e4d4d1fd5e60e025c5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953115"
---
# <a name="jet_indexidinequality-operator"></a><span data-ttu-id="2d978-103">JET_INDEXID. Opérateur d’inégalité</span><span class="sxs-lookup"><span data-stu-id="2d978-103">JET_INDEXID.Inequality operator</span></span>

<span data-ttu-id="2d978-104">Détermine si deux instances spécifiées de JET_INDEXID ne sont pas égales.</span><span class="sxs-lookup"><span data-stu-id="2d978-104">Determines whether two specified instances of JET_INDEXID are not equal.</span></span>

<span data-ttu-id="2d978-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2d978-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2d978-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2d978-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2d978-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d978-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_INDEXID, _
    rhs As JET_INDEXID _
) As Boolean
'Usage
Dim lhs As JET_INDEXID
Dim rhs As JET_INDEXID
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_INDEXID lhs,
    JET_INDEXID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="2d978-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d978-108">Parameters</span></span>

  - <span data-ttu-id="2d978-109">LHS</span><span class="sxs-lookup"><span data-stu-id="2d978-109">lhs</span></span>  
    <span data-ttu-id="2d978-110">Type : [Microsoft.ISAM.esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="2d978-110">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span></span>  
    
    <span data-ttu-id="2d978-111">Première instance à comparer.</span><span class="sxs-lookup"><span data-stu-id="2d978-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="2d978-112">rhs</span><span class="sxs-lookup"><span data-stu-id="2d978-112">rhs</span></span>  
    <span data-ttu-id="2d978-113">Type : [Microsoft.ISAM.esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="2d978-113">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span></span>  
    
    <span data-ttu-id="2d978-114">Deuxième instance à comparer.</span><span class="sxs-lookup"><span data-stu-id="2d978-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="2d978-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2d978-115">Return value</span></span>

<span data-ttu-id="2d978-116">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="2d978-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="2d978-117">True si les deux instances ne sont pas égales.</span><span class="sxs-lookup"><span data-stu-id="2d978-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2d978-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d978-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2d978-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="2d978-119">Reference</span></span>

[<span data-ttu-id="2d978-120">Structure JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="2d978-120">JET_INDEXID structure</span></span>](./jet-indexid-structure2.md)

[<span data-ttu-id="2d978-121">Membres JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="2d978-121">JET_INDEXID members</span></span>](./jet-indexid-members.md)

[<span data-ttu-id="2d978-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2d978-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
