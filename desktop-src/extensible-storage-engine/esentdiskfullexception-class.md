---
description: 'En savoir plus sur : classe EsentDiskFullException'
title: EsentDiskFullException, classe
TOCTitle: EsentDiskFullException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDiskFullException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdiskfullexception(v=EXCHG.10)
ms:contentKeyID: 55101513
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDiskFullException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDiskFullException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 28c3fb4fa06a6526cf06d0f4822ce3dcb835bad6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320789"
---
# <a name="esentdiskfullexception-class"></a><span data-ttu-id="2efd3-103">EsentDiskFullException, classe</span><span class="sxs-lookup"><span data-stu-id="2efd3-103">EsentDiskFullException class</span></span>

<span data-ttu-id="2efd3-104">Classe de base pour JET_err. Exceptions DiskFull.</span><span class="sxs-lookup"><span data-stu-id="2efd3-104">Base class for JET_err.DiskFull exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="2efd3-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="2efd3-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="2efd3-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="2efd3-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="2efd3-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="2efd3-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="2efd3-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="2efd3-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="2efd3-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="2efd3-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="2efd3-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="2efd3-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="2efd3-111">Microsoft. ISAM. esent. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="2efd3-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="2efd3-112">Microsoft. ISAM. esent. Interop. EsentDiskException</span><span class="sxs-lookup"><span data-stu-id="2efd3-112">Microsoft.Isam.Esent.Interop.EsentDiskException</span></span>](./esentdiskexception-class.md)  
              <span data-ttu-id="2efd3-113">Microsoft. ISAM. esent. Interop. EsentDiskFullException</span><span class="sxs-lookup"><span data-stu-id="2efd3-113">Microsoft.Isam.Esent.Interop.EsentDiskFullException</span></span>  

<span data-ttu-id="2efd3-114">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2efd3-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2efd3-115">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2efd3-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2efd3-116">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2efd3-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDiskFullException _
    Inherits EsentDiskException
'Usage
Dim instance As EsentDiskFullException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDiskFullException : EsentDiskException
```

## <a name="thread-safety"></a><span data-ttu-id="2efd3-117">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="2efd3-117">Thread safety</span></span>

<span data-ttu-id="2efd3-118">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="2efd3-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="2efd3-119">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="2efd3-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="2efd3-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2efd3-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2efd3-121">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="2efd3-121">Reference</span></span>

[<span data-ttu-id="2efd3-122">Membres EsentDiskFullException</span><span class="sxs-lookup"><span data-stu-id="2efd3-122">EsentDiskFullException members</span></span>](./esentdiskfullexception-members.md)

[<span data-ttu-id="2efd3-123">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2efd3-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
