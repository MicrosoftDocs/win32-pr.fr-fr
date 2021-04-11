---
description: 'En savoir plus sur : classe EsentOutOfThreadsException'
title: EsentOutOfThreadsException, classe
TOCTitle: EsentOutOfThreadsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfThreadsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofthreadsexception(v=EXCHG.10)
ms:contentKeyID: 55102450
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfThreadsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfThreadsException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 05a1427383a12c286ba37eee6f4ddfcd0b655350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953132"
---
# <a name="esentoutofthreadsexception-class"></a><span data-ttu-id="07d83-103">EsentOutOfThreadsException, classe</span><span class="sxs-lookup"><span data-stu-id="07d83-103">EsentOutOfThreadsException class</span></span>

<span data-ttu-id="07d83-104">Classe de base pour JET_err. Exceptions OutOfThreads.</span><span class="sxs-lookup"><span data-stu-id="07d83-104">Base class for JET_err.OutOfThreads exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="07d83-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="07d83-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="07d83-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="07d83-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="07d83-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="07d83-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="07d83-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="07d83-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="07d83-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="07d83-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="07d83-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="07d83-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="07d83-111">Microsoft. ISAM. esent. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="07d83-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="07d83-112">Microsoft. ISAM. esent. Interop. EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="07d83-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
              <span data-ttu-id="07d83-113">Microsoft. ISAM. esent. Interop. EsentOutOfThreadsException</span><span class="sxs-lookup"><span data-stu-id="07d83-113">Microsoft.Isam.Esent.Interop.EsentOutOfThreadsException</span></span>  

<span data-ttu-id="07d83-114">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="07d83-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="07d83-115">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="07d83-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="07d83-116">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="07d83-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfThreadsException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentOutOfThreadsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfThreadsException : EsentMemoryException
```

## <a name="thread-safety"></a><span data-ttu-id="07d83-117">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="07d83-117">Thread safety</span></span>

<span data-ttu-id="07d83-118">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="07d83-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="07d83-119">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="07d83-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="07d83-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07d83-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="07d83-121">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="07d83-121">Reference</span></span>

[<span data-ttu-id="07d83-122">Membres EsentOutOfThreadsException</span><span class="sxs-lookup"><span data-stu-id="07d83-122">EsentOutOfThreadsException members</span></span>](./esentoutofthreadsexception-members.md)

[<span data-ttu-id="07d83-123">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="07d83-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
