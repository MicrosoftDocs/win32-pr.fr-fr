---
description: 'En savoir plus sur : JET_INSTANCE. Equals, méthode (Object)'
title: JET_INSTANCE. Equals, méthode (Object)
TOCTitle: Equals method (Object)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE.Equals(System.Object)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance.equals(v=EXCHG.10)
ms:contentKeyID: 39515717
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
ms.openlocfilehash: 2b13393b487abb4de65360f5199ae1123d3f076e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034919"
---
# <a name="jet_instanceequals-method-object"></a><span data-ttu-id="46090-103">JET_INSTANCE. Equals, méthode (Object)</span><span class="sxs-lookup"><span data-stu-id="46090-103">JET_INSTANCE.Equals method (Object)</span></span>

<span data-ttu-id="46090-104">Retourne une valeur indiquant si cette instance est égale à une autre instance.</span><span class="sxs-lookup"><span data-stu-id="46090-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="46090-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="46090-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="46090-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="46090-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="46090-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46090-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides Function Equals ( _
    obj As Object _
) As Boolean
'Usage
Dim instance As JET_INSTANCE
Dim obj As Object
Dim returnValue As Boolean

returnValue = instance.Equals(obj)
```

``` csharp
public override bool Equals(
    Object obj
)
```

#### <a name="parameters"></a><span data-ttu-id="46090-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="46090-108">Parameters</span></span>

  - <span data-ttu-id="46090-109">obj</span><span class="sxs-lookup"><span data-stu-id="46090-109">obj</span></span>  
    <span data-ttu-id="46090-110">Type : [System. Object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="46090-110">Type: [System.Object](/dotnet/api/system.object)</span></span>  
    
    <span data-ttu-id="46090-111">Objet à comparer à cette instance.</span><span class="sxs-lookup"><span data-stu-id="46090-111">An object to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="46090-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="46090-112">Return value</span></span>

<span data-ttu-id="46090-113">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="46090-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="46090-114">True si les deux instances sont égales.</span><span class="sxs-lookup"><span data-stu-id="46090-114">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="46090-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46090-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="46090-116">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="46090-116">Reference</span></span>

[<span data-ttu-id="46090-117">Structure JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="46090-117">JET_INSTANCE structure</span></span>](./jet-instance-structure.md)

[<span data-ttu-id="46090-118">Membres JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="46090-118">JET_INSTANCE members</span></span>](./jet-instance-members.md)

[<span data-ttu-id="46090-119">Est égal à la surcharge</span><span class="sxs-lookup"><span data-stu-id="46090-119">Equals overload</span></span>](./jet-instance.equals-method.md)

[<span data-ttu-id="46090-120">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="46090-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
