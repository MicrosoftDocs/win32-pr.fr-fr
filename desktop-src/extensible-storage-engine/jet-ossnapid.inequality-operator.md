---
description: 'En savoir plus sur : JET_OSSNAPID. Opérateur d’inégalité'
title: JET_OSSNAPID. Opérateur d’inégalité
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_OSSNAPID.op_Inequality(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.JET_OSSNAPID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ossnapid.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39510705
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID.Inequality
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID.op_Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bb19425b9f4ce9a3d404c5b5019adf1b3a84d28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760215"
---
# <a name="jet_ossnapidinequality-operator"></a><span data-ttu-id="a2f8f-103">JET_OSSNAPID. Opérateur d’inégalité</span><span class="sxs-lookup"><span data-stu-id="a2f8f-103">JET_OSSNAPID.Inequality operator</span></span>

<span data-ttu-id="a2f8f-104">Détermine si deux instances spécifiées de JET_OSSNAPID ne sont pas égales.</span><span class="sxs-lookup"><span data-stu-id="a2f8f-104">Determines whether two specified instances of JET_OSSNAPID are not equal.</span></span>

<span data-ttu-id="a2f8f-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a2f8f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a2f8f-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a2f8f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a2f8f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2f8f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_OSSNAPID, _
    rhs As JET_OSSNAPID _
) As Boolean
'Usage
Dim lhs As JET_OSSNAPID
Dim rhs As JET_OSSNAPID
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_OSSNAPID lhs,
    JET_OSSNAPID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="a2f8f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2f8f-108">Parameters</span></span>

  - <span data-ttu-id="a2f8f-109">LHS</span><span class="sxs-lookup"><span data-stu-id="a2f8f-109">lhs</span></span>  
    <span data-ttu-id="a2f8f-110">Type : [Microsoft.ISAM.esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a2f8f-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="a2f8f-111">Première instance à comparer.</span><span class="sxs-lookup"><span data-stu-id="a2f8f-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="a2f8f-112">rhs</span><span class="sxs-lookup"><span data-stu-id="a2f8f-112">rhs</span></span>  
    <span data-ttu-id="a2f8f-113">Type : [Microsoft.ISAM.esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a2f8f-113">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="a2f8f-114">Deuxième instance à comparer.</span><span class="sxs-lookup"><span data-stu-id="a2f8f-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="a2f8f-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a2f8f-115">Return value</span></span>

<span data-ttu-id="a2f8f-116">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="a2f8f-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="a2f8f-117">True si les deux instances ne sont pas égales.</span><span class="sxs-lookup"><span data-stu-id="a2f8f-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a2f8f-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2f8f-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a2f8f-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="a2f8f-119">Reference</span></span>

[<span data-ttu-id="a2f8f-120">Structure JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="a2f8f-120">JET_OSSNAPID structure</span></span>](./jet-ossnapid-structure.md)

[<span data-ttu-id="a2f8f-121">Membres JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="a2f8f-121">JET_OSSNAPID members</span></span>](./jet-ossnapid-members.md)

[<span data-ttu-id="a2f8f-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a2f8f-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
