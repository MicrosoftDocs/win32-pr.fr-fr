---
description: 'En savoir plus sur : classe EsentMultiValuedIndexViolationException'
title: EsentMultiValuedIndexViolationException, classe
TOCTitle: EsentMultiValuedIndexViolationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMultiValuedIndexViolationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmultivaluedindexviolationexception(v=EXCHG.10)
ms:contentKeyID: 55102266
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMultiValuedIndexViolationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMultiValuedIndexViolationException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cafb4ce44f3b0600997e9d715f882e95869f65b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536981"
---
# <a name="esentmultivaluedindexviolationexception-class"></a><span data-ttu-id="da1bc-103">EsentMultiValuedIndexViolationException, classe</span><span class="sxs-lookup"><span data-stu-id="da1bc-103">EsentMultiValuedIndexViolationException class</span></span>

<span data-ttu-id="da1bc-104">Classe de base pour JET_err. Exceptions MultiValuedIndexViolation.</span><span class="sxs-lookup"><span data-stu-id="da1bc-104">Base class for JET_err.MultiValuedIndexViolation exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="da1bc-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="da1bc-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="da1bc-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="da1bc-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="da1bc-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="da1bc-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="da1bc-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="da1bc-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="da1bc-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="da1bc-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="da1bc-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="da1bc-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="da1bc-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="da1bc-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="da1bc-112">Microsoft. ISAM. esent. Interop. EsentMultiValuedIndexViolationException</span><span class="sxs-lookup"><span data-stu-id="da1bc-112">Microsoft.Isam.Esent.Interop.EsentMultiValuedIndexViolationException</span></span>  

<span data-ttu-id="da1bc-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="da1bc-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="da1bc-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="da1bc-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="da1bc-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da1bc-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMultiValuedIndexViolationException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentMultiValuedIndexViolationException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMultiValuedIndexViolationException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="da1bc-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="da1bc-116">Thread safety</span></span>

<span data-ttu-id="da1bc-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="da1bc-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="da1bc-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="da1bc-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="da1bc-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da1bc-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="da1bc-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="da1bc-120">Reference</span></span>

[<span data-ttu-id="da1bc-121">Membres EsentMultiValuedIndexViolationException</span><span class="sxs-lookup"><span data-stu-id="da1bc-121">EsentMultiValuedIndexViolationException members</span></span>](./esentmultivaluedindexviolationexception-members.md)

[<span data-ttu-id="da1bc-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="da1bc-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
