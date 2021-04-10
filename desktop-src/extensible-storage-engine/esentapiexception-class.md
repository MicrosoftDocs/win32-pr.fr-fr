---
description: 'En savoir plus sur : classe EsentApiException'
title: EsentApiException, classe
TOCTitle: EsentApiException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentApiException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentapiexception(v=EXCHG.10)
ms:contentKeyID: 55101032
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentApiException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentApiException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b01747d2ecb197ce99617b8c9206d4fada8c2a81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210517"
---
# <a name="esentapiexception-class"></a><span data-ttu-id="ef19f-103">EsentApiException, classe</span><span class="sxs-lookup"><span data-stu-id="ef19f-103">EsentApiException class</span></span>

<span data-ttu-id="ef19f-104">Classe de base pour les exceptions d’API.</span><span class="sxs-lookup"><span data-stu-id="ef19f-104">Base class for API exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ef19f-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="ef19f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ef19f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ef19f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ef19f-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="ef19f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ef19f-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="ef19f-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ef19f-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="ef19f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        <span data-ttu-id="ef19f-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="ef19f-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>  
          [<span data-ttu-id="ef19f-111">Microsoft. ISAM. esent. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="ef19f-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
          [<span data-ttu-id="ef19f-112">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="ef19f-112">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
          [<span data-ttu-id="ef19f-113">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="ef19f-113">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  

<span data-ttu-id="ef19f-114">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ef19f-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ef19f-115">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ef19f-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ef19f-116">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef19f-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentApiException _
    Inherits EsentErrorException
'Usage
Dim instance As EsentApiException
```

``` csharp
[SerializableAttribute]
public abstract class EsentApiException : EsentErrorException
```

## <a name="thread-safety"></a><span data-ttu-id="ef19f-117">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="ef19f-117">Thread safety</span></span>

<span data-ttu-id="ef19f-118">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="ef19f-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ef19f-119">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="ef19f-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ef19f-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef19f-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ef19f-121">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="ef19f-121">Reference</span></span>

[<span data-ttu-id="ef19f-122">Membres EsentApiException</span><span class="sxs-lookup"><span data-stu-id="ef19f-122">EsentApiException members</span></span>](./esentapiexception-members.md)

[<span data-ttu-id="ef19f-123">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ef19f-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
