---
description: 'En savoir plus sur : méthode JET_LGPOS. CompareTo'
title: JET_LGPOS. CompareTo, méthode
TOCTitle: 'CompareTo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.CompareTo(Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.compareto(v=EXCHG.10)
ms:contentKeyID: 39514516
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.CompareTo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.CompareTo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 83012ed755ab876618147c013e99868927e16f1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519426"
---
# <a name="jet_lgposcompareto-method"></a><span data-ttu-id="97d0a-103">JET_LGPOS. CompareTo, méthode</span><span class="sxs-lookup"><span data-stu-id="97d0a-103">JET_LGPOS.CompareTo method</span></span>

<span data-ttu-id="97d0a-104">Compare cette position du journal à une autre position du journal et détermine si cette instance est antérieure, identique ou postérieure à l’autre instance.</span><span class="sxs-lookup"><span data-stu-id="97d0a-104">Compares this log position to another log position and determines whether this instance is before, the same as or after the other instance.</span></span>

<span data-ttu-id="97d0a-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="97d0a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="97d0a-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="97d0a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="97d0a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97d0a-107">Syntax</span></span>

``` vb
'Declaration
Public Function CompareTo ( _
    other As JET_LGPOS _
) As Integer
'Usage
Dim instance As JET_LGPOS
Dim other As JET_LGPOS
Dim returnValue As Integer

returnValue = instance.CompareTo(other)
```

``` csharp
public int CompareTo(
    JET_LGPOS other
)
```

#### <a name="parameters"></a><span data-ttu-id="97d0a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97d0a-108">Parameters</span></span>

  - <span data-ttu-id="97d0a-109">autre</span><span class="sxs-lookup"><span data-stu-id="97d0a-109">other</span></span>  
    <span data-ttu-id="97d0a-110">Type : [Microsoft.ISAM.esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="97d0a-110">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="97d0a-111">Position du journal à comparer à l’instance actuelle.</span><span class="sxs-lookup"><span data-stu-id="97d0a-111">The log position to compare to the current instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="97d0a-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="97d0a-112">Return value</span></span>

<span data-ttu-id="97d0a-113">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="97d0a-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
<span data-ttu-id="97d0a-114">Nombre signé indiquant les positions relatives de cette instance et du paramètre de valeur.</span><span class="sxs-lookup"><span data-stu-id="97d0a-114">A signed number indicating the relative positions of this instance and the value parameter.</span></span>  

#### <a name="implements"></a><span data-ttu-id="97d0a-115">Implémente</span><span class="sxs-lookup"><span data-stu-id="97d0a-115">Implements</span></span>

[<span data-ttu-id="97d0a-116">IComparable \<T\> . CompareTo (T)</span><span class="sxs-lookup"><span data-stu-id="97d0a-116">IComparable\<T\>.CompareTo(T)</span></span>](/dotnet/api/system.icomparable-1.compareto#System_IComparable_1_CompareTo__0_)  

## <a name="see-also"></a><span data-ttu-id="97d0a-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97d0a-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="97d0a-118">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="97d0a-118">Reference</span></span>

[<span data-ttu-id="97d0a-119">Structure JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="97d0a-119">JET_LGPOS structure</span></span>](./jet-lgpos-structure2.md)

[<span data-ttu-id="97d0a-120">Membres JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="97d0a-120">JET_LGPOS members</span></span>](./jet-lgpos-members.md)

[<span data-ttu-id="97d0a-121">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="97d0a-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
