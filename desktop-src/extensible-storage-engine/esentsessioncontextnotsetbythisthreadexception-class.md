---
description: 'En savoir plus sur : classe EsentSessionContextNotSetByThisThreadException'
title: EsentSessionContextNotSetByThisThreadException, classe
TOCTitle: EsentSessionContextNotSetByThisThreadException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSessionContextNotSetByThisThreadException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsessioncontextnotsetbythisthreadexception(v=EXCHG.10)
ms:contentKeyID: 55102698
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSessionContextNotSetByThisThreadException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSessionContextNotSetByThisThreadException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 097712353336a9a412dd4255781a42c74eac1782
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523392"
---
# <a name="esentsessioncontextnotsetbythisthreadexception-class"></a><span data-ttu-id="742ca-103">EsentSessionContextNotSetByThisThreadException, classe</span><span class="sxs-lookup"><span data-stu-id="742ca-103">EsentSessionContextNotSetByThisThreadException class</span></span>

<span data-ttu-id="742ca-104">Classe de base pour JET_err. Exceptions SessionContextNotSetByThisThread.</span><span class="sxs-lookup"><span data-stu-id="742ca-104">Base class for JET_err.SessionContextNotSetByThisThread exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="742ca-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="742ca-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="742ca-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="742ca-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="742ca-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="742ca-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="742ca-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="742ca-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="742ca-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="742ca-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="742ca-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="742ca-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="742ca-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="742ca-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="742ca-112">Microsoft. ISAM. esent. Interop. EsentSessionContextNotSetByThisThreadException</span><span class="sxs-lookup"><span data-stu-id="742ca-112">Microsoft.Isam.Esent.Interop.EsentSessionContextNotSetByThisThreadException</span></span>  

<span data-ttu-id="742ca-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="742ca-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="742ca-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="742ca-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="742ca-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="742ca-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSessionContextNotSetByThisThreadException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentSessionContextNotSetByThisThreadException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSessionContextNotSetByThisThreadException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="742ca-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="742ca-116">Thread safety</span></span>

<span data-ttu-id="742ca-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="742ca-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="742ca-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="742ca-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="742ca-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="742ca-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="742ca-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="742ca-120">Reference</span></span>

[<span data-ttu-id="742ca-121">Membres EsentSessionContextNotSetByThisThreadException</span><span class="sxs-lookup"><span data-stu-id="742ca-121">EsentSessionContextNotSetByThisThreadException members</span></span>](./esentsessioncontextnotsetbythisthreadexception-members.md)

[<span data-ttu-id="742ca-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="742ca-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
