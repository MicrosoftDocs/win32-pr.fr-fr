---
description: 'En savoir plus sur : JET_TABLEID. Opérateur d’inégalité'
title: JET_TABLEID. Opérateur d’inégalité
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_TABLEID.op_Inequality(Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tableid.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39510333
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TABLEID.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLEID.Inequality
- Microsoft.Isam.Esent.Interop.JET_TABLEID.op_Inequality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7e1cfc9a43beb8478be287e1659883d49f62239
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529296"
---
# <a name="jet_tableidinequality-operator"></a><span data-ttu-id="9d649-103">JET_TABLEID. Opérateur d’inégalité</span><span class="sxs-lookup"><span data-stu-id="9d649-103">JET_TABLEID.Inequality operator</span></span>

<span data-ttu-id="9d649-104">Détermine si deux instances spécifiées de JET_TABLEID ne sont pas égales.</span><span class="sxs-lookup"><span data-stu-id="9d649-104">Determines whether two specified instances of JET_TABLEID are not equal.</span></span>

<span data-ttu-id="9d649-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9d649-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9d649-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9d649-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9d649-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d649-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_TABLEID, _
    rhs As JET_TABLEID _
) As Boolean
'Usage
Dim lhs As JET_TABLEID
Dim rhs As JET_TABLEID
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_TABLEID lhs,
    JET_TABLEID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="9d649-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d649-108">Parameters</span></span>

  - <span data-ttu-id="9d649-109">LHS</span><span class="sxs-lookup"><span data-stu-id="9d649-109">lhs</span></span>  
    <span data-ttu-id="9d649-110">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9d649-110">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="9d649-111">Première instance à comparer.</span><span class="sxs-lookup"><span data-stu-id="9d649-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="9d649-112">rhs</span><span class="sxs-lookup"><span data-stu-id="9d649-112">rhs</span></span>  
    <span data-ttu-id="9d649-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9d649-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="9d649-114">Deuxième instance à comparer.</span><span class="sxs-lookup"><span data-stu-id="9d649-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="9d649-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9d649-115">Return value</span></span>

<span data-ttu-id="9d649-116">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="9d649-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="9d649-117">True si les deux instances ne sont pas égales.</span><span class="sxs-lookup"><span data-stu-id="9d649-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9d649-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d649-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9d649-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="9d649-119">Reference</span></span>

[<span data-ttu-id="9d649-120">Structure JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="9d649-120">JET_TABLEID structure</span></span>](./jet-tableid-structure.md)

[<span data-ttu-id="9d649-121">Membres JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="9d649-121">JET_TABLEID members</span></span>](./jet-tableid-members.md)

[<span data-ttu-id="9d649-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="9d649-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
