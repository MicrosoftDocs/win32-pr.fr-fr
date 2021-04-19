---
description: 'En savoir plus sur : JET_THREADSTATS. Opérateur d’addition'
title: JET_THREADSTATS. Opérateur d’addition (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'Addition operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Addition(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.op_addition(v=EXCHG.10)
ms:contentKeyID: 39516195
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Addition
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Addition
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Addition
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 829bf96b3c7095b95644db220a5d18c7e987e44b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538216"
---
# <a name="jet_threadstatsaddition-operator"></a><span data-ttu-id="e6cac-103">JET_THREADSTATS. Opérateur d’addition</span><span class="sxs-lookup"><span data-stu-id="e6cac-103">JET_THREADSTATS.Addition operator</span></span>

<span data-ttu-id="e6cac-104">Ajoutez les statistiques dans deux structures JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="e6cac-104">Add the stats in two JET_THREADSTATS structures.</span></span>

<span data-ttu-id="e6cac-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e6cac-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="e6cac-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e6cac-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e6cac-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6cac-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator + ( _
    t1 As JET_THREADSTATS, _
    t2 As JET_THREADSTATS _
) As JET_THREADSTATS
'Usage
Dim t1 As JET_THREADSTATS
Dim t2 As JET_THREADSTATS
Dim returnValue As JET_THREADSTATS

returnValue = (t1 + t2)
```

``` csharp
public static JET_THREADSTATS operator +(
    JET_THREADSTATS t1,
    JET_THREADSTATS t2
)
```

#### <a name="parameters"></a><span data-ttu-id="e6cac-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6cac-108">Parameters</span></span>

  - <span data-ttu-id="e6cac-109">t1</span><span class="sxs-lookup"><span data-stu-id="e6cac-109">t1</span></span>  
    <span data-ttu-id="e6cac-110">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="e6cac-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="e6cac-111">Premier JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="e6cac-111">The first JET_THREADSTATS.</span></span>

<!-- end list -->

  - <span data-ttu-id="e6cac-112">H2</span><span class="sxs-lookup"><span data-stu-id="e6cac-112">t2</span></span>  
    <span data-ttu-id="e6cac-113">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="e6cac-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="e6cac-114">Deuxième JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="e6cac-114">The second JET_THREADSTATS.</span></span>

#### <a name="return-value"></a><span data-ttu-id="e6cac-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e6cac-115">Return value</span></span>

<span data-ttu-id="e6cac-116">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="e6cac-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
<span data-ttu-id="e6cac-117">JET_THREADSTATS contenant le résultat de l’ajout des statistiques dans T1 et T2.</span><span class="sxs-lookup"><span data-stu-id="e6cac-117">A JET_THREADSTATS containing the result of adding the stats in t1 and t2.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e6cac-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6cac-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e6cac-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="e6cac-119">Reference</span></span>

[<span data-ttu-id="e6cac-120">Structure JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="e6cac-120">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="e6cac-121">Membres JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="e6cac-121">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="e6cac-122">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="e6cac-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
