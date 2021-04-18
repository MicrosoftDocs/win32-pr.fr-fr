---
description: 'En savoir plus sur : classe EsentTooManyInstancesException'
title: EsentTooManyInstancesException, classe
TOCTitle: EsentTooManyInstancesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanyinstancesexception(v=EXCHG.10)
ms:contentKeyID: 55103084
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ecd20f6a05a17d4bd21623732a4e716e82c9b1cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520101"
---
# <a name="esenttoomanyinstancesexception-class"></a><span data-ttu-id="0c855-103">EsentTooManyInstancesException, classe</span><span class="sxs-lookup"><span data-stu-id="0c855-103">EsentTooManyInstancesException class</span></span>

<span data-ttu-id="0c855-104">Classe de base pour JET_err. Exceptions TooManyInstances.</span><span class="sxs-lookup"><span data-stu-id="0c855-104">Base class for JET_err.TooManyInstances exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="0c855-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="0c855-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="0c855-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="0c855-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="0c855-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="0c855-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="0c855-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="0c855-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="0c855-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="0c855-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="0c855-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="0c855-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="0c855-111">Microsoft. ISAM. esent. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="0c855-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="0c855-112">Microsoft. ISAM. esent. Interop. EsentQuotaException</span><span class="sxs-lookup"><span data-stu-id="0c855-112">Microsoft.Isam.Esent.Interop.EsentQuotaException</span></span>](./esentquotaexception-class.md)  
              <span data-ttu-id="0c855-113">Microsoft. ISAM. esent. Interop. EsentTooManyInstancesException</span><span class="sxs-lookup"><span data-stu-id="0c855-113">Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException</span></span>  

<span data-ttu-id="0c855-114">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0c855-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0c855-115">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0c855-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0c855-116">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c855-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyInstancesException _
    Inherits EsentQuotaException
'Usage
Dim instance As EsentTooManyInstancesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyInstancesException : EsentQuotaException
```

## <a name="thread-safety"></a><span data-ttu-id="0c855-117">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="0c855-117">Thread safety</span></span>

<span data-ttu-id="0c855-118">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="0c855-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="0c855-119">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="0c855-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="0c855-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c855-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0c855-121">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="0c855-121">Reference</span></span>

[<span data-ttu-id="0c855-122">Membres EsentTooManyInstancesException</span><span class="sxs-lookup"><span data-stu-id="0c855-122">EsentTooManyInstancesException members</span></span>](./esenttoomanyinstancesexception-members.md)

[<span data-ttu-id="0c855-123">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0c855-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
