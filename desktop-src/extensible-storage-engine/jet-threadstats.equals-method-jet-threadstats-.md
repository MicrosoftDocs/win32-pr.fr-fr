---
description: 'En savoir plus sur : JET_THREADSTATS. Equals, méthode (JET_THREADSTATS)'
title: JET_THREADSTATS. Equals, méthode (JET_THREADSTATS) (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: Equals method (JET_THREADSTATS)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Equals(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.equals(v=EXCHG.10)
ms:contentKeyID: 39515931
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 716b9d45002c0182fd4a629b018f9287aff812e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204081"
---
# <a name="jet_threadstatsequals-method-jet_threadstats"></a><span data-ttu-id="8c473-103">JET_THREADSTATS. Equals, méthode (JET_THREADSTATS)</span><span class="sxs-lookup"><span data-stu-id="8c473-103">JET_THREADSTATS.Equals method (JET_THREADSTATS)</span></span>

<span data-ttu-id="8c473-104">Retourne une valeur indiquant si cette instance est égale à une autre instance.</span><span class="sxs-lookup"><span data-stu-id="8c473-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="8c473-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8c473-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="8c473-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8c473-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8c473-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c473-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_THREADSTATS _
) As Boolean
'Usage
Dim instance As JET_THREADSTATS
Dim other As JET_THREADSTATS
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_THREADSTATS other
)
```

#### <a name="parameters"></a><span data-ttu-id="8c473-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c473-108">Parameters</span></span>

  - <span data-ttu-id="8c473-109">autre</span><span class="sxs-lookup"><span data-stu-id="8c473-109">other</span></span>  
    <span data-ttu-id="8c473-110">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="8c473-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="8c473-111">Instance de à comparer à cette instance.</span><span class="sxs-lookup"><span data-stu-id="8c473-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="8c473-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8c473-112">Return value</span></span>

<span data-ttu-id="8c473-113">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="8c473-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="8c473-114">True si les deux instances sont égales.</span><span class="sxs-lookup"><span data-stu-id="8c473-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="8c473-115">Implémente</span><span class="sxs-lookup"><span data-stu-id="8c473-115">Implements</span></span>

[<span data-ttu-id="8c473-116">IEquatable \<T\> . Égal à (T)</span><span class="sxs-lookup"><span data-stu-id="8c473-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="8c473-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c473-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8c473-118">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="8c473-118">Reference</span></span>

[<span data-ttu-id="8c473-119">Structure JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="8c473-119">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="8c473-120">Membres JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="8c473-120">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="8c473-121">Est égal à la surcharge</span><span class="sxs-lookup"><span data-stu-id="8c473-121">Equals overload</span></span>](./jet-threadstats.equals-method.md)

[<span data-ttu-id="8c473-122">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="8c473-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
