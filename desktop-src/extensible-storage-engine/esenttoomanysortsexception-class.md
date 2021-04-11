---
description: 'En savoir plus sur : classe EsentTooManySortsException'
title: EsentTooManySortsException, classe
TOCTitle: EsentTooManySortsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManySortsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanysortsexception(v=EXCHG.10)
ms:contentKeyID: 55103099
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManySortsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManySortsException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b9048d2c7c65906ba6f093f21c604f25adfcf16c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318753"
---
# <a name="esenttoomanysortsexception-class"></a><span data-ttu-id="39c6e-103">EsentTooManySortsException, classe</span><span class="sxs-lookup"><span data-stu-id="39c6e-103">EsentTooManySortsException class</span></span>

<span data-ttu-id="39c6e-104">Classe de base pour JET_err. Exceptions TooManySorts.</span><span class="sxs-lookup"><span data-stu-id="39c6e-104">Base class for JET_err.TooManySorts exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="39c6e-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="39c6e-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="39c6e-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="39c6e-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="39c6e-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="39c6e-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="39c6e-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="39c6e-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="39c6e-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="39c6e-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="39c6e-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="39c6e-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="39c6e-111">Microsoft. ISAM. esent. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="39c6e-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="39c6e-112">Microsoft. ISAM. esent. Interop. EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="39c6e-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
              <span data-ttu-id="39c6e-113">Microsoft. ISAM. esent. Interop. EsentTooManySortsException</span><span class="sxs-lookup"><span data-stu-id="39c6e-113">Microsoft.Isam.Esent.Interop.EsentTooManySortsException</span></span>  

<span data-ttu-id="39c6e-114">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="39c6e-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="39c6e-115">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="39c6e-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="39c6e-116">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39c6e-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManySortsException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentTooManySortsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManySortsException : EsentMemoryException
```

## <a name="thread-safety"></a><span data-ttu-id="39c6e-117">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="39c6e-117">Thread safety</span></span>

<span data-ttu-id="39c6e-118">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="39c6e-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="39c6e-119">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="39c6e-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="39c6e-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39c6e-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="39c6e-121">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="39c6e-121">Reference</span></span>

[<span data-ttu-id="39c6e-122">Membres EsentTooManySortsException</span><span class="sxs-lookup"><span data-stu-id="39c6e-122">EsentTooManySortsException members</span></span>](./esenttoomanysortsexception-members.md)

[<span data-ttu-id="39c6e-123">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="39c6e-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
