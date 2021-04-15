---
description: 'En savoir plus sur : classe EsentDatabaseIncompleteIncrementalReseedException'
title: EsentDatabaseIncompleteIncrementalReseedException, classe
TOCTitle: EsentDatabaseIncompleteIncrementalReseedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteIncrementalReseedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaseincompleteincrementalreseedexception(v=EXCHG.10)
ms:contentKeyID: 55101478
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteIncrementalReseedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteIncrementalReseedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 65d660c28f9b876e0cb2016631a4a8108a52b6dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526643"
---
# <a name="esentdatabaseincompleteincrementalreseedexception-class"></a><span data-ttu-id="4e8ef-103">EsentDatabaseIncompleteIncrementalReseedException, classe</span><span class="sxs-lookup"><span data-stu-id="4e8ef-103">EsentDatabaseIncompleteIncrementalReseedException class</span></span>

<span data-ttu-id="4e8ef-104">Classe de base pour JET_err. Exceptions DatabaseIncompleteIncrementalReseed.</span><span class="sxs-lookup"><span data-stu-id="4e8ef-104">Base class for JET_err.DatabaseIncompleteIncrementalReseed exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="4e8ef-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="4e8ef-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="4e8ef-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="4e8ef-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="4e8ef-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="4e8ef-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="4e8ef-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="4e8ef-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="4e8ef-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="4e8ef-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="4e8ef-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="4e8ef-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="4e8ef-111">Microsoft. ISAM. esent. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="4e8ef-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="4e8ef-112">Microsoft. ISAM. esent. Interop. EsentDatabaseIncompleteIncrementalReseedException</span><span class="sxs-lookup"><span data-stu-id="4e8ef-112">Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteIncrementalReseedException</span></span>  

<span data-ttu-id="4e8ef-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4e8ef-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4e8ef-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4e8ef-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4e8ef-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e8ef-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseIncompleteIncrementalReseedException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentDatabaseIncompleteIncrementalReseedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseIncompleteIncrementalReseedException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="4e8ef-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="4e8ef-116">Thread safety</span></span>

<span data-ttu-id="4e8ef-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="4e8ef-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="4e8ef-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="4e8ef-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="4e8ef-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e8ef-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4e8ef-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="4e8ef-120">Reference</span></span>

[<span data-ttu-id="4e8ef-121">Membres EsentDatabaseIncompleteIncrementalReseedException</span><span class="sxs-lookup"><span data-stu-id="4e8ef-121">EsentDatabaseIncompleteIncrementalReseedException members</span></span>](./esentdatabaseincompleteincrementalreseedexception-members.md)

[<span data-ttu-id="4e8ef-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4e8ef-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
