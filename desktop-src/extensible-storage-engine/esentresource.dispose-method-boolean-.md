---
description: 'En savoir plus sur : méthode EsentResource. Dispose (Boolean)'
title: EsentResource. dispose, méthode (Boolean)
TOCTitle: Dispose method (Boolean)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentResource.Dispose(System.Boolean)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresource.dispose(v=EXCHG.10)
ms:contentKeyID: 55102624
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentResource.Dispose
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf74291bf4c54ffa1d61c28bf7caff1e8c2b231b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210875"
---
# <a name="esentresourcedispose-method-boolean"></a><span data-ttu-id="090a6-103">EsentResource. dispose, méthode (Boolean)</span><span class="sxs-lookup"><span data-stu-id="090a6-103">EsentResource.Dispose method (Boolean)</span></span>

<span data-ttu-id="090a6-104">Appelée par dispose et le finaliseur.</span><span class="sxs-lookup"><span data-stu-id="090a6-104">Called by Dispose and the finalizer.</span></span>

<span data-ttu-id="090a6-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="090a6-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="090a6-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="090a6-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="090a6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="090a6-107">Syntax</span></span>

``` vb
'Declaration
Protected Overridable Sub Dispose ( _
    isDisposing As Boolean _
)
'Usage
Dim isDisposing As Boolean

Me.Dispose(isDisposing)
```

``` csharp
protected virtual void Dispose(
    bool isDisposing
)
```

#### <a name="parameters"></a><span data-ttu-id="090a6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="090a6-108">Parameters</span></span>

  - <span data-ttu-id="090a6-109">isDisposing</span><span class="sxs-lookup"><span data-stu-id="090a6-109">isDisposing</span></span>  
    <span data-ttu-id="090a6-110">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="090a6-110">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
    
    <span data-ttu-id="090a6-111">True si la méthode est appelée à partir de dispose.</span><span class="sxs-lookup"><span data-stu-id="090a6-111">True if called from Dispose.</span></span>

## <a name="see-also"></a><span data-ttu-id="090a6-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="090a6-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="090a6-113">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="090a6-113">Reference</span></span>

[<span data-ttu-id="090a6-114">EsentResource, classe</span><span class="sxs-lookup"><span data-stu-id="090a6-114">EsentResource class</span></span>](./esentresource-class.md)

[<span data-ttu-id="090a6-115">Membres EsentResource</span><span class="sxs-lookup"><span data-stu-id="090a6-115">EsentResource members</span></span>](./esentresource-members.md)

[<span data-ttu-id="090a6-116">Dispose de la surcharge</span><span class="sxs-lookup"><span data-stu-id="090a6-116">Dispose overload</span></span>](./esentresource.dispose-method.md)

[<span data-ttu-id="090a6-117">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="090a6-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
