---
description: 'En savoir plus sur : JET_INSTANCE. Equals, méthode (JET_INSTANCE)'
title: JET_INSTANCE. Equals, méthode (JET_INSTANCE)
TOCTitle: Equals method (JET_INSTANCE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE.Equals(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance.equals(v=EXCHG.10)
ms:contentKeyID: 39512490
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be4f2a172da5fc0d7670e7e87464eac04df3cfa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204092"
---
# <a name="jet_instanceequals-method-jet_instance"></a><span data-ttu-id="843c8-103">JET_INSTANCE. Equals, méthode (JET_INSTANCE)</span><span class="sxs-lookup"><span data-stu-id="843c8-103">JET_INSTANCE.Equals method (JET_INSTANCE)</span></span>

<span data-ttu-id="843c8-104">Retourne une valeur indiquant si cette instance est égale à une autre instance.</span><span class="sxs-lookup"><span data-stu-id="843c8-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="843c8-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="843c8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="843c8-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="843c8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="843c8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="843c8-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_INSTANCE _
) As Boolean
'Usage
Dim instance As JET_INSTANCE
Dim other As JET_INSTANCE
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_INSTANCE other
)
```

#### <a name="parameters"></a><span data-ttu-id="843c8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="843c8-108">Parameters</span></span>

  - <span data-ttu-id="843c8-109">autre</span><span class="sxs-lookup"><span data-stu-id="843c8-109">other</span></span>  
    <span data-ttu-id="843c8-110">Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="843c8-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="843c8-111">Instance de à comparer à cette instance.</span><span class="sxs-lookup"><span data-stu-id="843c8-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="843c8-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="843c8-112">Return value</span></span>

<span data-ttu-id="843c8-113">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="843c8-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="843c8-114">True si les deux instances sont égales.</span><span class="sxs-lookup"><span data-stu-id="843c8-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="843c8-115">Implémente</span><span class="sxs-lookup"><span data-stu-id="843c8-115">Implements</span></span>

[<span data-ttu-id="843c8-116">IEquatable \<T\> . Égal à (T)</span><span class="sxs-lookup"><span data-stu-id="843c8-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="843c8-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="843c8-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="843c8-118">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="843c8-118">Reference</span></span>

[<span data-ttu-id="843c8-119">Structure JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="843c8-119">JET_INSTANCE structure</span></span>](./jet-instance-structure.md)

[<span data-ttu-id="843c8-120">Membres JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="843c8-120">JET_INSTANCE members</span></span>](./jet-instance-members.md)

[<span data-ttu-id="843c8-121">Est égal à la surcharge</span><span class="sxs-lookup"><span data-stu-id="843c8-121">Equals overload</span></span>](./jet-instance.equals-method.md)

[<span data-ttu-id="843c8-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="843c8-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
