---
description: 'En savoir plus sur : JET_THREADSTATS. Ajouter une méthode'
title: JET_THREADSTATS. Add, méthode (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'Add method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Add(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.add(v=EXCHG.10)
ms:contentKeyID: 39514259
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Add
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Add
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2a824249fde43de92c65d64d02fbab4097b7dc34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513969"
---
# <a name="jet_threadstatsadd-method"></a><span data-ttu-id="8f017-103">JET_THREADSTATS. Ajouter une méthode</span><span class="sxs-lookup"><span data-stu-id="8f017-103">JET_THREADSTATS.Add method</span></span>

<span data-ttu-id="8f017-104">Ajoutez les statistiques dans deux structures JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="8f017-104">Add the stats in two JET_THREADSTATS structures.</span></span>

<span data-ttu-id="8f017-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8f017-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="8f017-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8f017-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8f017-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8f017-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function Add ( _
    t1 As JET_THREADSTATS, _
    t2 As JET_THREADSTATS _
) As JET_THREADSTATS
'Usage
Dim t1 As JET_THREADSTATS
Dim t2 As JET_THREADSTATS
Dim returnValue As JET_THREADSTATS

returnValue = JET_THREADSTATS.Add(t1, t2)
```

``` csharp
public static JET_THREADSTATS Add(
    JET_THREADSTATS t1,
    JET_THREADSTATS t2
)
```

#### <a name="parameters"></a><span data-ttu-id="8f017-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8f017-108">Parameters</span></span>

  - <span data-ttu-id="8f017-109">t1</span><span class="sxs-lookup"><span data-stu-id="8f017-109">t1</span></span>  
    <span data-ttu-id="8f017-110">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="8f017-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="8f017-111">Premier JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="8f017-111">The first JET_THREADSTATS.</span></span>

<!-- end list -->

  - <span data-ttu-id="8f017-112">H2</span><span class="sxs-lookup"><span data-stu-id="8f017-112">t2</span></span>  
    <span data-ttu-id="8f017-113">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="8f017-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="8f017-114">Deuxième JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="8f017-114">The second JET_THREADSTATS.</span></span>

#### <a name="return-value"></a><span data-ttu-id="8f017-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8f017-115">Return value</span></span>

<span data-ttu-id="8f017-116">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="8f017-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
<span data-ttu-id="8f017-117">JET_THREADSTATS contenant le résultat de l’ajout des statistiques dans T1 et T2.</span><span class="sxs-lookup"><span data-stu-id="8f017-117">A JET_THREADSTATS containing the result of adding the stats in t1 and t2.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8f017-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f017-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8f017-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="8f017-119">Reference</span></span>

[<span data-ttu-id="8f017-120">Structure JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="8f017-120">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="8f017-121">Membres JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="8f017-121">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="8f017-122">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="8f017-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
