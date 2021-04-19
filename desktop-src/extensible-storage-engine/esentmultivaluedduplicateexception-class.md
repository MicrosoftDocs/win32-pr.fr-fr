---
description: 'En savoir plus sur : classe EsentMultiValuedDuplicateException'
title: EsentMultiValuedDuplicateException, classe
TOCTitle: EsentMultiValuedDuplicateException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmultivaluedduplicateexception(v=EXCHG.10)
ms:contentKeyID: 55102340
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fddfac316bb8ad13ff5c42abc8041e4a18c85321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544802"
---
# <a name="esentmultivaluedduplicateexception-class"></a><span data-ttu-id="d9f07-103">EsentMultiValuedDuplicateException, classe</span><span class="sxs-lookup"><span data-stu-id="d9f07-103">EsentMultiValuedDuplicateException class</span></span>

<span data-ttu-id="d9f07-104">Classe de base pour JET_err. Exceptions MultiValuedDuplicate.</span><span class="sxs-lookup"><span data-stu-id="d9f07-104">Base class for JET_err.MultiValuedDuplicate exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="d9f07-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="d9f07-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="d9f07-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="d9f07-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="d9f07-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="d9f07-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="d9f07-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="d9f07-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="d9f07-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="d9f07-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="d9f07-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="d9f07-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="d9f07-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="d9f07-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="d9f07-112">Microsoft. ISAM. esent. Interop. EsentMultiValuedDuplicateException</span><span class="sxs-lookup"><span data-stu-id="d9f07-112">Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateException</span></span>  

<span data-ttu-id="d9f07-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d9f07-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d9f07-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d9f07-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d9f07-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9f07-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMultiValuedDuplicateException _
    Inherits EsentStateException
'Usage
Dim instance As EsentMultiValuedDuplicateException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMultiValuedDuplicateException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="d9f07-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="d9f07-116">Thread safety</span></span>

<span data-ttu-id="d9f07-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="d9f07-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="d9f07-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="d9f07-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="d9f07-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9f07-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d9f07-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="d9f07-120">Reference</span></span>

[<span data-ttu-id="d9f07-121">Membres EsentMultiValuedDuplicateException</span><span class="sxs-lookup"><span data-stu-id="d9f07-121">EsentMultiValuedDuplicateException members</span></span>](./esentmultivaluedduplicateexception-members.md)

[<span data-ttu-id="d9f07-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d9f07-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
