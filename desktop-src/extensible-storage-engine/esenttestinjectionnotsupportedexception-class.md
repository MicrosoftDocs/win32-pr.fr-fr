---
description: 'En savoir plus sur : classe EsentTestInjectionNotSupportedException'
title: EsentTestInjectionNotSupportedException, classe
TOCTitle: EsentTestInjectionNotSupportedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTestInjectionNotSupportedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttestinjectionnotsupportedexception(v=EXCHG.10)
ms:contentKeyID: 55103041
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTestInjectionNotSupportedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTestInjectionNotSupportedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 07d640aa0429ac6fce63b07f873a26ea536a6261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210638"
---
# <a name="esenttestinjectionnotsupportedexception-class"></a><span data-ttu-id="b22ec-103">EsentTestInjectionNotSupportedException, classe</span><span class="sxs-lookup"><span data-stu-id="b22ec-103">EsentTestInjectionNotSupportedException class</span></span>

<span data-ttu-id="b22ec-104">Classe de base pour JET_err. Exceptions TestInjectionNotSupported.</span><span class="sxs-lookup"><span data-stu-id="b22ec-104">Base class for JET_err.TestInjectionNotSupported exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b22ec-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="b22ec-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b22ec-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b22ec-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b22ec-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="b22ec-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b22ec-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="b22ec-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b22ec-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="b22ec-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="b22ec-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="b22ec-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="b22ec-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="b22ec-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="b22ec-112">Microsoft. ISAM. esent. Interop. EsentTestInjectionNotSupportedException</span><span class="sxs-lookup"><span data-stu-id="b22ec-112">Microsoft.Isam.Esent.Interop.EsentTestInjectionNotSupportedException</span></span>  

<span data-ttu-id="b22ec-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b22ec-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b22ec-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b22ec-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b22ec-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b22ec-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTestInjectionNotSupportedException _
    Inherits EsentStateException
'Usage
Dim instance As EsentTestInjectionNotSupportedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTestInjectionNotSupportedException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="b22ec-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="b22ec-116">Thread safety</span></span>

<span data-ttu-id="b22ec-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="b22ec-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b22ec-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="b22ec-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b22ec-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b22ec-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b22ec-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="b22ec-120">Reference</span></span>

[<span data-ttu-id="b22ec-121">Membres EsentTestInjectionNotSupportedException</span><span class="sxs-lookup"><span data-stu-id="b22ec-121">EsentTestInjectionNotSupportedException members</span></span>](./esenttestinjectionnotsupportedexception-members.md)

[<span data-ttu-id="b22ec-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b22ec-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
