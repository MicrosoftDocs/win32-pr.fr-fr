---
description: 'En savoir plus sur : classe EsentOutOfSessionsException'
title: EsentOutOfSessionsException, classe
TOCTitle: EsentOutOfSessionsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfSessionsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofsessionsexception(v=EXCHG.10)
ms:contentKeyID: 55102494
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfSessionsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfSessionsException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 70b3c466586551f67f451d8ecc6ad108da52089a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393648"
---
# <a name="esentoutofsessionsexception-class"></a><span data-ttu-id="f207f-103">EsentOutOfSessionsException, classe</span><span class="sxs-lookup"><span data-stu-id="f207f-103">EsentOutOfSessionsException class</span></span>

<span data-ttu-id="f207f-104">Classe de base pour JET_err. Exceptions OutOfSessions.</span><span class="sxs-lookup"><span data-stu-id="f207f-104">Base class for JET_err.OutOfSessions exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f207f-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="f207f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="f207f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="f207f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f207f-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="f207f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="f207f-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="f207f-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="f207f-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="f207f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="f207f-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="f207f-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="f207f-111">Microsoft. ISAM. esent. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="f207f-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="f207f-112">Microsoft. ISAM. esent. Interop. EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="f207f-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
              <span data-ttu-id="f207f-113">Microsoft. ISAM. esent. Interop. EsentOutOfSessionsException</span><span class="sxs-lookup"><span data-stu-id="f207f-113">Microsoft.Isam.Esent.Interop.EsentOutOfSessionsException</span></span>  

<span data-ttu-id="f207f-114">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f207f-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f207f-115">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f207f-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f207f-116">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f207f-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfSessionsException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentOutOfSessionsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfSessionsException : EsentMemoryException
```

## <a name="thread-safety"></a><span data-ttu-id="f207f-117">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="f207f-117">Thread safety</span></span>

<span data-ttu-id="f207f-118">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="f207f-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f207f-119">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="f207f-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f207f-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f207f-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f207f-121">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="f207f-121">Reference</span></span>

[<span data-ttu-id="f207f-122">Membres EsentOutOfSessionsException</span><span class="sxs-lookup"><span data-stu-id="f207f-122">EsentOutOfSessionsException members</span></span>](./esentoutofsessionsexception-members.md)

[<span data-ttu-id="f207f-123">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f207f-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
