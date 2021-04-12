---
description: 'En savoir plus sur : JET_THREADSTATS. Soustraction (opérateur)'
title: JET_THREADSTATS. Opérateur de soustraction (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'Subtraction operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Subtraction(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.op_subtraction(v=EXCHG.10)
ms:contentKeyID: 39512217
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtraction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Subtraction
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtraction
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5a41455f05b91a582a1d8aae824ca5b426628cf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201225"
---
# <a name="jet_threadstatssubtraction-operator"></a><span data-ttu-id="75a40-103">JET_THREADSTATS. Soustraction (opérateur)</span><span class="sxs-lookup"><span data-stu-id="75a40-103">JET_THREADSTATS.Subtraction operator</span></span>

<span data-ttu-id="75a40-104">Calcule la différence de statistiques entre deux structures de JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="75a40-104">Calculate the difference in stats between two JET_THREADSTATS structures.</span></span>

<span data-ttu-id="75a40-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="75a40-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="75a40-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="75a40-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="75a40-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75a40-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator - ( _
    t1 As JET_THREADSTATS, _
    t2 As JET_THREADSTATS _
) As JET_THREADSTATS
'Usage
Dim t1 As JET_THREADSTATS
Dim t2 As JET_THREADSTATS
Dim returnValue As JET_THREADSTATS

returnValue = (t1 - t2)
```

``` csharp
public static JET_THREADSTATS operator -(
    JET_THREADSTATS t1,
    JET_THREADSTATS t2
)
```

#### <a name="parameters"></a><span data-ttu-id="75a40-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75a40-108">Parameters</span></span>

  - <span data-ttu-id="75a40-109">t1</span><span class="sxs-lookup"><span data-stu-id="75a40-109">t1</span></span>  
    <span data-ttu-id="75a40-110">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="75a40-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="75a40-111">Premier JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="75a40-111">The first JET_THREADSTATS.</span></span>

<!-- end list -->

  - <span data-ttu-id="75a40-112">H2</span><span class="sxs-lookup"><span data-stu-id="75a40-112">t2</span></span>  
    <span data-ttu-id="75a40-113">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="75a40-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="75a40-114">Deuxième JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="75a40-114">The second JET_THREADSTATS.</span></span>

#### <a name="return-value"></a><span data-ttu-id="75a40-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="75a40-115">Return value</span></span>

<span data-ttu-id="75a40-116">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="75a40-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
<span data-ttu-id="75a40-117">JET_THREADSTATS contenant la différence des statistiques entre T1 et T2.</span><span class="sxs-lookup"><span data-stu-id="75a40-117">A JET_THREADSTATS containing the difference in stats between t1 and t2.</span></span>  

## <a name="see-also"></a><span data-ttu-id="75a40-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75a40-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="75a40-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="75a40-119">Reference</span></span>

[<span data-ttu-id="75a40-120">Structure JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="75a40-120">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="75a40-121">Membres JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="75a40-121">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="75a40-122">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="75a40-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
