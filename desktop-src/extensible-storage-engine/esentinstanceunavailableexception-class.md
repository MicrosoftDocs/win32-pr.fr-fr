---
description: 'En savoir plus sur : classe EsentInstanceUnavailableException'
title: EsentInstanceUnavailableException, classe
TOCTitle: EsentInstanceUnavailableException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinstanceunavailableexception(v=EXCHG.10)
ms:contentKeyID: 55101879
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c3761965a836182480ec934be344322f5b5c6a1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533807"
---
# <a name="esentinstanceunavailableexception-class"></a><span data-ttu-id="272d2-103">EsentInstanceUnavailableException, classe</span><span class="sxs-lookup"><span data-stu-id="272d2-103">EsentInstanceUnavailableException class</span></span>

<span data-ttu-id="272d2-104">Classe de base pour JET_err. Exceptions InstanceUnavailable.</span><span class="sxs-lookup"><span data-stu-id="272d2-104">Base class for JET_err.InstanceUnavailable exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="272d2-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="272d2-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="272d2-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="272d2-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="272d2-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="272d2-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="272d2-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="272d2-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="272d2-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="272d2-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="272d2-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="272d2-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="272d2-111">Microsoft. ISAM. esent. Interop. EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="272d2-111">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>](./esentfatalexception-class.md)  
            <span data-ttu-id="272d2-112">Microsoft. ISAM. esent. Interop. EsentInstanceUnavailableException</span><span class="sxs-lookup"><span data-stu-id="272d2-112">Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableException</span></span>  

<span data-ttu-id="272d2-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="272d2-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="272d2-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="272d2-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="272d2-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="272d2-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInstanceUnavailableException _
    Inherits EsentFatalException
'Usage
Dim instance As EsentInstanceUnavailableException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInstanceUnavailableException : EsentFatalException
```

## <a name="thread-safety"></a><span data-ttu-id="272d2-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="272d2-116">Thread safety</span></span>

<span data-ttu-id="272d2-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="272d2-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="272d2-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="272d2-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="272d2-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="272d2-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="272d2-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="272d2-120">Reference</span></span>

[<span data-ttu-id="272d2-121">Membres EsentInstanceUnavailableException</span><span class="sxs-lookup"><span data-stu-id="272d2-121">EsentInstanceUnavailableException members</span></span>](./esentinstanceunavailableexception-members.md)

[<span data-ttu-id="272d2-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="272d2-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
