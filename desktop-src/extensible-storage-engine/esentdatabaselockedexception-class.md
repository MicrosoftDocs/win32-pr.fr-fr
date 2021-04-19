---
description: 'En savoir plus sur : classe EsentDatabaseLockedException'
title: EsentDatabaseLockedException, classe
TOCTitle: EsentDatabaseLockedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseLockedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaselockedexception(v=EXCHG.10)
ms:contentKeyID: 55101527
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseLockedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseLockedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 97001b234c845d6453818aeeb5a930d090382278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516680"
---
# <a name="esentdatabaselockedexception-class"></a><span data-ttu-id="acc02-103">EsentDatabaseLockedException, classe</span><span class="sxs-lookup"><span data-stu-id="acc02-103">EsentDatabaseLockedException class</span></span>

<span data-ttu-id="acc02-104">Classe de base pour JET_err. Exceptions DatabaseLocked.</span><span class="sxs-lookup"><span data-stu-id="acc02-104">Base class for JET_err.DatabaseLocked exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="acc02-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="acc02-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="acc02-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="acc02-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="acc02-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="acc02-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="acc02-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="acc02-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="acc02-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="acc02-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="acc02-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="acc02-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="acc02-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="acc02-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="acc02-112">Microsoft. ISAM. esent. Interop. EsentDatabaseLockedException</span><span class="sxs-lookup"><span data-stu-id="acc02-112">Microsoft.Isam.Esent.Interop.EsentDatabaseLockedException</span></span>  

<span data-ttu-id="acc02-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="acc02-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="acc02-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="acc02-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="acc02-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="acc02-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseLockedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentDatabaseLockedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseLockedException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="acc02-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="acc02-116">Thread safety</span></span>

<span data-ttu-id="acc02-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="acc02-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="acc02-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="acc02-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="acc02-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="acc02-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="acc02-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="acc02-120">Reference</span></span>

[<span data-ttu-id="acc02-121">Membres EsentDatabaseLockedException</span><span class="sxs-lookup"><span data-stu-id="acc02-121">EsentDatabaseLockedException members</span></span>](./esentdatabaselockedexception-members.md)

[<span data-ttu-id="acc02-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="acc02-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
