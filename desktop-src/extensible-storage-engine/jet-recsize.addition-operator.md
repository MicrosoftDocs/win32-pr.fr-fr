---
description: 'En savoir plus sur : JET_RECSIZE. Opérateur d’addition'
title: JET_RECSIZE. Opérateur d’addition (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'Addition operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Addition(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.op_addition(v=EXCHG.10)
ms:contentKeyID: 39512451
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Addition
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Addition
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Addition
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c41fae92f6177bf0c39138ad33988a74c482e0ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749828"
---
# <a name="jet_recsizeaddition-operator"></a><span data-ttu-id="eb5f8-103">JET_RECSIZE. Opérateur d’addition</span><span class="sxs-lookup"><span data-stu-id="eb5f8-103">JET_RECSIZE.Addition operator</span></span>

<span data-ttu-id="eb5f8-104">Ajoutez les tailles dans deux structures de JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="eb5f8-104">Add the sizes in two JET_RECSIZE structures.</span></span>

<span data-ttu-id="eb5f8-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="eb5f8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="eb5f8-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="eb5f8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="eb5f8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb5f8-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator + ( _
    left As JET_RECSIZE, _
    right As JET_RECSIZE _
) As JET_RECSIZE
'Usage
Dim left As JET_RECSIZE
Dim right As JET_RECSIZE
Dim returnValue As JET_RECSIZE

returnValue = (left + right)
```

``` csharp
public static JET_RECSIZE operator +(
    JET_RECSIZE left,
    JET_RECSIZE right
)
```

#### <a name="parameters"></a><span data-ttu-id="eb5f8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb5f8-108">Parameters</span></span>

  - <span data-ttu-id="eb5f8-109">gauche</span><span class="sxs-lookup"><span data-stu-id="eb5f8-109">left</span></span>  
    <span data-ttu-id="eb5f8-110">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="eb5f8-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="eb5f8-111">Premier JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="eb5f8-111">The first JET_RECSIZE.</span></span>

<!-- end list -->

  - <span data-ttu-id="eb5f8-112">droite</span><span class="sxs-lookup"><span data-stu-id="eb5f8-112">right</span></span>  
    <span data-ttu-id="eb5f8-113">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="eb5f8-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="eb5f8-114">Deuxième JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="eb5f8-114">The second JET_RECSIZE.</span></span>

#### <a name="return-value"></a><span data-ttu-id="eb5f8-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb5f8-115">Return value</span></span>

<span data-ttu-id="eb5f8-116">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="eb5f8-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
<span data-ttu-id="eb5f8-117">JET_RECSIZE contenant le résultat de l’ajout de tailles à gauche et à droite.</span><span class="sxs-lookup"><span data-stu-id="eb5f8-117">A JET_RECSIZE containing the result of adding the sizes in left and right.</span></span>  

## <a name="see-also"></a><span data-ttu-id="eb5f8-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb5f8-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="eb5f8-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="eb5f8-119">Reference</span></span>

[<span data-ttu-id="eb5f8-120">Structure JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="eb5f8-120">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="eb5f8-121">Membres JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="eb5f8-121">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="eb5f8-122">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="eb5f8-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
