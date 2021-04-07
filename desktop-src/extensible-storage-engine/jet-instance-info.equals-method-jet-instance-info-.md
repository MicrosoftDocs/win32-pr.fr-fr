---
description: 'En savoir plus sur : JET_INSTANCE_INFO. Equals, méthode (JET_INSTANCE_INFO)'
title: JET_INSTANCE_INFO. Equals, méthode (JET_INSTANCE_INFO)
TOCTitle: Equals method (JET_INSTANCE_INFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.Equals(Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance_info.equals(v=EXCHG.10)
ms:contentKeyID: 55103697
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b601e018b51e6e95162478ff6c5fe12e77f7b469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952149"
---
# <a name="jet_instance_infoequals-method-jet_instance_info"></a><span data-ttu-id="ae65e-103">JET_INSTANCE_INFO. Equals, méthode (JET_INSTANCE_INFO)</span><span class="sxs-lookup"><span data-stu-id="ae65e-103">JET_INSTANCE_INFO.Equals method (JET_INSTANCE_INFO)</span></span>

<span data-ttu-id="ae65e-104">Retourne une valeur indiquant si cette instance est égale à une autre instance.</span><span class="sxs-lookup"><span data-stu-id="ae65e-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="ae65e-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ae65e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ae65e-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ae65e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ae65e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae65e-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_INSTANCE_INFO _
) As Boolean
'Usage
Dim instance As JET_INSTANCE_INFO
Dim other As JET_INSTANCE_INFO
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_INSTANCE_INFO other
)
```

#### <a name="parameters"></a><span data-ttu-id="ae65e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae65e-108">Parameters</span></span>

  - <span data-ttu-id="ae65e-109">autre</span><span class="sxs-lookup"><span data-stu-id="ae65e-109">other</span></span>  
    <span data-ttu-id="ae65e-110">Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE_INFO](./jet-instance-info-class.md)</span><span class="sxs-lookup"><span data-stu-id="ae65e-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO](./jet-instance-info-class.md)</span></span>  
    
    <span data-ttu-id="ae65e-111">Instance de à comparer à cette instance.</span><span class="sxs-lookup"><span data-stu-id="ae65e-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ae65e-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ae65e-112">Return value</span></span>

<span data-ttu-id="ae65e-113">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="ae65e-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="ae65e-114">True si les deux instances sont égales.</span><span class="sxs-lookup"><span data-stu-id="ae65e-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="ae65e-115">Implémente</span><span class="sxs-lookup"><span data-stu-id="ae65e-115">Implements</span></span>

[<span data-ttu-id="ae65e-116">IEquatable \<T\> . Égal à (T)</span><span class="sxs-lookup"><span data-stu-id="ae65e-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="ae65e-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae65e-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ae65e-118">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="ae65e-118">Reference</span></span>

[<span data-ttu-id="ae65e-119">Classe JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="ae65e-119">JET_INSTANCE_INFO class</span></span>](./jet-instance-info-class.md)

[<span data-ttu-id="ae65e-120">Membres JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="ae65e-120">JET_INSTANCE_INFO members</span></span>](./jet-instance-info-members.md)

[<span data-ttu-id="ae65e-121">Est égal à la surcharge</span><span class="sxs-lookup"><span data-stu-id="ae65e-121">Equals overload</span></span>](./jet-instance-info.equals-method.md)

[<span data-ttu-id="ae65e-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ae65e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
