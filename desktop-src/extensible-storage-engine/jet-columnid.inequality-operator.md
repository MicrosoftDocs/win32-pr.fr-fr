---
description: 'En savoir plus sur : JET_COLUMNID. Opérateur d’inégalité'
title: JET_COLUMNID. Opérateur d’inégalité
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_Inequality(Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39516136
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.Inequality
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b6b0856a5c551be06dd7f4b55f8f144c0e509f1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527533"
---
# <a name="jet_columnidinequality-operator"></a><span data-ttu-id="62f08-103">JET_COLUMNID. Opérateur d’inégalité</span><span class="sxs-lookup"><span data-stu-id="62f08-103">JET_COLUMNID.Inequality operator</span></span>

<span data-ttu-id="62f08-104">Détermine si deux instances spécifiées de JET_COLUMNID ne sont pas égales.</span><span class="sxs-lookup"><span data-stu-id="62f08-104">Determines whether two specified instances of JET_COLUMNID are not equal.</span></span>

<span data-ttu-id="62f08-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="62f08-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="62f08-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="62f08-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="62f08-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62f08-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_COLUMNID, _
    rhs As JET_COLUMNID _
) As Boolean
'Usage
Dim lhs As JET_COLUMNID
Dim rhs As JET_COLUMNID
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_COLUMNID lhs,
    JET_COLUMNID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="62f08-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="62f08-108">Parameters</span></span>

  - <span data-ttu-id="62f08-109">LHS</span><span class="sxs-lookup"><span data-stu-id="62f08-109">lhs</span></span>  
    <span data-ttu-id="62f08-110">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="62f08-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="62f08-111">Première instance à comparer.</span><span class="sxs-lookup"><span data-stu-id="62f08-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="62f08-112">rhs</span><span class="sxs-lookup"><span data-stu-id="62f08-112">rhs</span></span>  
    <span data-ttu-id="62f08-113">Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="62f08-113">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="62f08-114">Deuxième instance à comparer.</span><span class="sxs-lookup"><span data-stu-id="62f08-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="62f08-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="62f08-115">Return value</span></span>

<span data-ttu-id="62f08-116">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="62f08-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="62f08-117">True si les deux instances ne sont pas égales.</span><span class="sxs-lookup"><span data-stu-id="62f08-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="62f08-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62f08-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="62f08-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="62f08-119">Reference</span></span>

[<span data-ttu-id="62f08-120">Structure JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="62f08-120">JET_COLUMNID structure</span></span>](./jet-columnid-structure.md)

[<span data-ttu-id="62f08-121">Membres JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="62f08-121">JET_COLUMNID members</span></span>](./jet-columnid-members.md)

[<span data-ttu-id="62f08-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="62f08-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
