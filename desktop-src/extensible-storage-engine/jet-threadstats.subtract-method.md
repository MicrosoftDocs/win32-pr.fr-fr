---
description: 'En savoir plus sur : JET_THREADSTATS. Soustraire la méthode'
title: JET_THREADSTATS. Subtract, méthode (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'Subtract method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtract(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.subtract(v=EXCHG.10)
ms:contentKeyID: 39514465
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtract
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtract
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf1f47258fe965c41b0a02ccbb32712b0a54c97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536812"
---
# <a name="jet_threadstatssubtract-method"></a><span data-ttu-id="55da3-103">JET_THREADSTATS. Soustraire la méthode</span><span class="sxs-lookup"><span data-stu-id="55da3-103">JET_THREADSTATS.Subtract method</span></span>

<span data-ttu-id="55da3-104">Calcule la différence de statistiques entre deux structures de JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="55da3-104">Calculate the difference in stats between two JET_THREADSTATS structures.</span></span>

<span data-ttu-id="55da3-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="55da3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="55da3-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="55da3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="55da3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55da3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function Subtract ( _
    t1 As JET_THREADSTATS, _
    t2 As JET_THREADSTATS _
) As JET_THREADSTATS
'Usage
Dim t1 As JET_THREADSTATS
Dim t2 As JET_THREADSTATS
Dim returnValue As JET_THREADSTATS

returnValue = JET_THREADSTATS.Subtract(t1, t2)
```

``` csharp
public static JET_THREADSTATS Subtract(
    JET_THREADSTATS t1,
    JET_THREADSTATS t2
)
```

#### <a name="parameters"></a><span data-ttu-id="55da3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="55da3-108">Parameters</span></span>

  - <span data-ttu-id="55da3-109">t1</span><span class="sxs-lookup"><span data-stu-id="55da3-109">t1</span></span>  
    <span data-ttu-id="55da3-110">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="55da3-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="55da3-111">Premier JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="55da3-111">The first JET_THREADSTATS.</span></span>

<!-- end list -->

  - <span data-ttu-id="55da3-112">H2</span><span class="sxs-lookup"><span data-stu-id="55da3-112">t2</span></span>  
    <span data-ttu-id="55da3-113">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="55da3-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="55da3-114">Deuxième JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="55da3-114">The second JET_THREADSTATS.</span></span>

#### <a name="return-value"></a><span data-ttu-id="55da3-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="55da3-115">Return value</span></span>

<span data-ttu-id="55da3-116">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="55da3-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
<span data-ttu-id="55da3-117">JET_THREADSTATS contenant la différence des statistiques entre T1 et T2.</span><span class="sxs-lookup"><span data-stu-id="55da3-117">A JET_THREADSTATS containing the difference in stats between t1 and t2.</span></span>  

## <a name="see-also"></a><span data-ttu-id="55da3-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55da3-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="55da3-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="55da3-119">Reference</span></span>

[<span data-ttu-id="55da3-120">Structure JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="55da3-120">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="55da3-121">Membres JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="55da3-121">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="55da3-122">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="55da3-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
