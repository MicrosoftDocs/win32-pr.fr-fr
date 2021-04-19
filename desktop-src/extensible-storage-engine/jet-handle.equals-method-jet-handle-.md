---
description: 'En savoir plus sur : JET_HANDLE. Equals, méthode (JET_HANDLE)'
title: JET_HANDLE. Equals, méthode (JET_HANDLE)
TOCTitle: Equals method (JET_HANDLE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_HANDLE.Equals(Microsoft.Isam.Esent.Interop.JET_HANDLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_handle.equals(v=EXCHG.10)
ms:contentKeyID: 39515292
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_HANDLE.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ab4ea5df734b626e54a70bc690301e755013ae59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106537072"
---
# <a name="jet_handleequals-method-jet_handle"></a><span data-ttu-id="6bdd6-103">JET_HANDLE. Equals, méthode (JET_HANDLE)</span><span class="sxs-lookup"><span data-stu-id="6bdd6-103">JET_HANDLE.Equals method (JET_HANDLE)</span></span>

<span data-ttu-id="6bdd6-104">Retourne une valeur indiquant si cette instance est égale à une autre instance.</span><span class="sxs-lookup"><span data-stu-id="6bdd6-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="6bdd6-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6bdd6-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6bdd6-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6bdd6-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6bdd6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6bdd6-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_HANDLE _
) As Boolean
'Usage
Dim instance As JET_HANDLE
Dim other As JET_HANDLE
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_HANDLE other
)
```

#### <a name="parameters"></a><span data-ttu-id="6bdd6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6bdd6-108">Parameters</span></span>

  - <span data-ttu-id="6bdd6-109">autre</span><span class="sxs-lookup"><span data-stu-id="6bdd6-109">other</span></span>  
    <span data-ttu-id="6bdd6-110">Type : [Microsoft.ISAM.esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6bdd6-110">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="6bdd6-111">Instance de à comparer à cette instance.</span><span class="sxs-lookup"><span data-stu-id="6bdd6-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="6bdd6-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6bdd6-112">Return value</span></span>

<span data-ttu-id="6bdd6-113">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="6bdd6-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="6bdd6-114">True si les deux instances sont égales.</span><span class="sxs-lookup"><span data-stu-id="6bdd6-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="6bdd6-115">Implémente</span><span class="sxs-lookup"><span data-stu-id="6bdd6-115">Implements</span></span>

[<span data-ttu-id="6bdd6-116">IEquatable \<T\> . Égal à (T)</span><span class="sxs-lookup"><span data-stu-id="6bdd6-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="6bdd6-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6bdd6-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6bdd6-118">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="6bdd6-118">Reference</span></span>

[<span data-ttu-id="6bdd6-119">Structure JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="6bdd6-119">JET_HANDLE structure</span></span>](./jet-handle-structure.md)

[<span data-ttu-id="6bdd6-120">Membres JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="6bdd6-120">JET_HANDLE members</span></span>](./jet-handle-members.md)

[<span data-ttu-id="6bdd6-121">Est égal à la surcharge</span><span class="sxs-lookup"><span data-stu-id="6bdd6-121">Equals overload</span></span>](./jet-handle.equals-method.md)

[<span data-ttu-id="6bdd6-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="6bdd6-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
