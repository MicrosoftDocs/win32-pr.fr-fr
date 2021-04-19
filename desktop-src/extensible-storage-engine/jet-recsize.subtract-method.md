---
description: 'En savoir plus sur : JET_RECSIZE. Soustraire la méthode'
title: JET_RECSIZE. Subtract, méthode (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'Subtract method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtract(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.subtract(v=EXCHG.10)
ms:contentKeyID: 39514591
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtract
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtract
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9789dac524e57ea762243ed47d513d262d7ebb0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522123"
---
# <a name="jet_recsizesubtract-method"></a><span data-ttu-id="17c9e-103">JET_RECSIZE. Soustraire la méthode</span><span class="sxs-lookup"><span data-stu-id="17c9e-103">JET_RECSIZE.Subtract method</span></span>

<span data-ttu-id="17c9e-104">Calculez la différence de tailles entre deux structures de JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="17c9e-104">Calculate the difference in sizes between two JET_RECSIZE structures.</span></span>

<span data-ttu-id="17c9e-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="17c9e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="17c9e-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="17c9e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="17c9e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17c9e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function Subtract ( _
    s1 As JET_RECSIZE, _
    s2 As JET_RECSIZE _
) As JET_RECSIZE
'Usage
Dim s1 As JET_RECSIZE
Dim s2 As JET_RECSIZE
Dim returnValue As JET_RECSIZE

returnValue = JET_RECSIZE.Subtract(s1, s2)
```

``` csharp
public static JET_RECSIZE Subtract(
    JET_RECSIZE s1,
    JET_RECSIZE s2
)
```

#### <a name="parameters"></a><span data-ttu-id="17c9e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17c9e-108">Parameters</span></span>

  - <span data-ttu-id="17c9e-109">s1</span><span class="sxs-lookup"><span data-stu-id="17c9e-109">s1</span></span>  
    <span data-ttu-id="17c9e-110">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="17c9e-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="17c9e-111">Premier JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="17c9e-111">The first JET_RECSIZE.</span></span>

<!-- end list -->

  - <span data-ttu-id="17c9e-112">s2</span><span class="sxs-lookup"><span data-stu-id="17c9e-112">s2</span></span>  
    <span data-ttu-id="17c9e-113">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="17c9e-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="17c9e-114">Deuxième JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="17c9e-114">The second JET_RECSIZE.</span></span>

#### <a name="return-value"></a><span data-ttu-id="17c9e-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="17c9e-115">Return value</span></span>

<span data-ttu-id="17c9e-116">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="17c9e-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
<span data-ttu-id="17c9e-117">JET_RECSIZE contenant la différence de tailles comprises entre S1 et S2.</span><span class="sxs-lookup"><span data-stu-id="17c9e-117">A JET_RECSIZE containing the difference in sizes between s1 and s2.</span></span>  

## <a name="see-also"></a><span data-ttu-id="17c9e-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17c9e-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="17c9e-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="17c9e-119">Reference</span></span>

[<span data-ttu-id="17c9e-120">Structure JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="17c9e-120">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="17c9e-121">Membres JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="17c9e-121">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="17c9e-122">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="17c9e-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
