---
description: 'En savoir plus sur : JET_HANDLE. Opérateur d’égalité'
title: JET_HANDLE. Opérateur d’égalité
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_HANDLE.op_Equality(Microsoft.Isam.Esent.Interop.JET_HANDLE,Microsoft.Isam.Esent.Interop.JET_HANDLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_handle.op_equality(v=EXCHG.10)
ms:contentKeyID: 39512271
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_HANDLE.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_HANDLE.Equality
- Microsoft.Isam.Esent.Interop.JET_HANDLE.op_Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37f0a7f10dd757a51dcdd450db2d2f0e863ab043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759598"
---
# <a name="jet_handleequality-operator"></a><span data-ttu-id="8dfb9-103">JET_HANDLE. Opérateur d’égalité</span><span class="sxs-lookup"><span data-stu-id="8dfb9-103">JET_HANDLE.Equality operator</span></span>

<span data-ttu-id="8dfb9-104">Détermine si deux instances spécifiées de JET_HANDLE sont égales.</span><span class="sxs-lookup"><span data-stu-id="8dfb9-104">Determines whether two specified instances of JET_HANDLE are equal.</span></span>

<span data-ttu-id="8dfb9-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8dfb9-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8dfb9-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8dfb9-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8dfb9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8dfb9-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_HANDLE, _
    rhs As JET_HANDLE _
) As Boolean
'Usage
Dim lhs As JET_HANDLE
Dim rhs As JET_HANDLE
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_HANDLE lhs,
    JET_HANDLE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="8dfb9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8dfb9-108">Parameters</span></span>

  - <span data-ttu-id="8dfb9-109">LHS</span><span class="sxs-lookup"><span data-stu-id="8dfb9-109">lhs</span></span>  
    <span data-ttu-id="8dfb9-110">Type : [Microsoft.ISAM.esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8dfb9-110">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="8dfb9-111">Première instance à comparer.</span><span class="sxs-lookup"><span data-stu-id="8dfb9-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="8dfb9-112">rhs</span><span class="sxs-lookup"><span data-stu-id="8dfb9-112">rhs</span></span>  
    <span data-ttu-id="8dfb9-113">Type : [Microsoft.ISAM.esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8dfb9-113">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="8dfb9-114">Deuxième instance à comparer.</span><span class="sxs-lookup"><span data-stu-id="8dfb9-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="8dfb9-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8dfb9-115">Return value</span></span>

<span data-ttu-id="8dfb9-116">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="8dfb9-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="8dfb9-117">True si les deux instances sont égales.</span><span class="sxs-lookup"><span data-stu-id="8dfb9-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8dfb9-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8dfb9-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8dfb9-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="8dfb9-119">Reference</span></span>

[<span data-ttu-id="8dfb9-120">Structure JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="8dfb9-120">JET_HANDLE structure</span></span>](./jet-handle-structure.md)

[<span data-ttu-id="8dfb9-121">Membres JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="8dfb9-121">JET_HANDLE members</span></span>](./jet-handle-members.md)

[<span data-ttu-id="8dfb9-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8dfb9-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
