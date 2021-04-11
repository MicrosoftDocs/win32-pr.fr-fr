---
description: 'En savoir plus sur : JET_SESID. Opérateur d’inégalité'
title: JET_SESID. Opérateur d’inégalité
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SESID.op_Inequality(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_sesid.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39514305
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SESID.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SESID.Inequality
- Microsoft.Isam.Esent.Interop.JET_SESID.op_Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e42b5e21937ae8af4ccd04708520ece40558c5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112542"
---
# <a name="jet_sesidinequality-operator"></a><span data-ttu-id="b0f46-103">JET_SESID. Opérateur d’inégalité</span><span class="sxs-lookup"><span data-stu-id="b0f46-103">JET_SESID.Inequality operator</span></span>

<span data-ttu-id="b0f46-104">Détermine si deux instances spécifiées de JET_SESID ne sont pas égales.</span><span class="sxs-lookup"><span data-stu-id="b0f46-104">Determines whether two specified instances of JET_SESID are not equal.</span></span>

<span data-ttu-id="b0f46-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b0f46-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b0f46-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b0f46-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b0f46-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0f46-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_SESID, _
    rhs As JET_SESID _
) As Boolean
'Usage
Dim lhs As JET_SESID
Dim rhs As JET_SESID
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_SESID lhs,
    JET_SESID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="b0f46-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0f46-108">Parameters</span></span>

  - <span data-ttu-id="b0f46-109">LHS</span><span class="sxs-lookup"><span data-stu-id="b0f46-109">lhs</span></span>  
    <span data-ttu-id="b0f46-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b0f46-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b0f46-111">Première instance à comparer.</span><span class="sxs-lookup"><span data-stu-id="b0f46-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="b0f46-112">rhs</span><span class="sxs-lookup"><span data-stu-id="b0f46-112">rhs</span></span>  
    <span data-ttu-id="b0f46-113">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b0f46-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b0f46-114">Deuxième instance à comparer.</span><span class="sxs-lookup"><span data-stu-id="b0f46-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b0f46-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b0f46-115">Return value</span></span>

<span data-ttu-id="b0f46-116">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="b0f46-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="b0f46-117">True si les deux instances ne sont pas égales.</span><span class="sxs-lookup"><span data-stu-id="b0f46-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b0f46-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0f46-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b0f46-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="b0f46-119">Reference</span></span>

[<span data-ttu-id="b0f46-120">Structure JET_SESID</span><span class="sxs-lookup"><span data-stu-id="b0f46-120">JET_SESID structure</span></span>](./jet-sesid-structure.md)

[<span data-ttu-id="b0f46-121">Membres JET_SESID</span><span class="sxs-lookup"><span data-stu-id="b0f46-121">JET_SESID members</span></span>](./jet-sesid-members.md)

[<span data-ttu-id="b0f46-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b0f46-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
