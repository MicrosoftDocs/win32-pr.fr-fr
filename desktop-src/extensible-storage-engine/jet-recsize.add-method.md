---
description: 'En savoir plus sur : JET_RECSIZE. Ajouter une méthode'
title: JET_RECSIZE. Add, méthode (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'Add method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Add(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.add(v=EXCHG.10)
ms:contentKeyID: 39509872
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Add
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Add
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e12a78a0a32bcca02afec100b0b238f4444a6ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525023"
---
# <a name="jet_recsizeadd-method"></a><span data-ttu-id="42d0f-103">JET_RECSIZE. Ajouter une méthode</span><span class="sxs-lookup"><span data-stu-id="42d0f-103">JET_RECSIZE.Add method</span></span>

<span data-ttu-id="42d0f-104">Ajoutez les tailles dans deux structures de JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="42d0f-104">Add the sizes in two JET_RECSIZE structures.</span></span>

<span data-ttu-id="42d0f-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="42d0f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="42d0f-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="42d0f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="42d0f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42d0f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function Add ( _
    s1 As JET_RECSIZE, _
    s2 As JET_RECSIZE _
) As JET_RECSIZE
'Usage
Dim s1 As JET_RECSIZE
Dim s2 As JET_RECSIZE
Dim returnValue As JET_RECSIZE

returnValue = JET_RECSIZE.Add(s1, s2)
```

``` csharp
public static JET_RECSIZE Add(
    JET_RECSIZE s1,
    JET_RECSIZE s2
)
```

#### <a name="parameters"></a><span data-ttu-id="42d0f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42d0f-108">Parameters</span></span>

  - <span data-ttu-id="42d0f-109">s1</span><span class="sxs-lookup"><span data-stu-id="42d0f-109">s1</span></span>  
    <span data-ttu-id="42d0f-110">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="42d0f-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="42d0f-111">Premier JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="42d0f-111">The first JET_RECSIZE.</span></span>

<!-- end list -->

  - <span data-ttu-id="42d0f-112">s2</span><span class="sxs-lookup"><span data-stu-id="42d0f-112">s2</span></span>  
    <span data-ttu-id="42d0f-113">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="42d0f-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="42d0f-114">Deuxième JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="42d0f-114">The second JET_RECSIZE.</span></span>

#### <a name="return-value"></a><span data-ttu-id="42d0f-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="42d0f-115">Return value</span></span>

<span data-ttu-id="42d0f-116">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="42d0f-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
<span data-ttu-id="42d0f-117">JET_RECSIZE contenant le résultat de l’ajout de tailles dans S1 et S2.</span><span class="sxs-lookup"><span data-stu-id="42d0f-117">A JET_RECSIZE containing the result of adding the sizes in s1 and s2.</span></span>  

## <a name="see-also"></a><span data-ttu-id="42d0f-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42d0f-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="42d0f-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="42d0f-119">Reference</span></span>

[<span data-ttu-id="42d0f-120">Structure JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="42d0f-120">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="42d0f-121">Membres JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="42d0f-121">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="42d0f-122">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="42d0f-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
