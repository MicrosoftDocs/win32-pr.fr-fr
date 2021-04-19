---
description: 'En savoir plus sur : classe EsentTooManyColumnsException'
title: EsentTooManyColumnsException, classe
TOCTitle: EsentTooManyColumnsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyColumnsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanycolumnsexception(v=EXCHG.10)
ms:contentKeyID: 55103051
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyColumnsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyColumnsException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2191abd07aea85dac6275f3c42f34acd13376035
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530213"
---
# <a name="esenttoomanycolumnsexception-class"></a><span data-ttu-id="1b7bd-103">EsentTooManyColumnsException, classe</span><span class="sxs-lookup"><span data-stu-id="1b7bd-103">EsentTooManyColumnsException class</span></span>

<span data-ttu-id="1b7bd-104">Classe de base pour JET_err. Exceptions TooManyColumns.</span><span class="sxs-lookup"><span data-stu-id="1b7bd-104">Base class for JET_err.TooManyColumns exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="1b7bd-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="1b7bd-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="1b7bd-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="1b7bd-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="1b7bd-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="1b7bd-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="1b7bd-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="1b7bd-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="1b7bd-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="1b7bd-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="1b7bd-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="1b7bd-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="1b7bd-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="1b7bd-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="1b7bd-112">Microsoft. ISAM. esent. Interop. EsentTooManyColumnsException</span><span class="sxs-lookup"><span data-stu-id="1b7bd-112">Microsoft.Isam.Esent.Interop.EsentTooManyColumnsException</span></span>  

<span data-ttu-id="1b7bd-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1b7bd-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1b7bd-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1b7bd-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1b7bd-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b7bd-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyColumnsException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentTooManyColumnsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyColumnsException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="1b7bd-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="1b7bd-116">Thread safety</span></span>

<span data-ttu-id="1b7bd-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="1b7bd-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="1b7bd-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="1b7bd-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="1b7bd-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b7bd-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1b7bd-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="1b7bd-120">Reference</span></span>

[<span data-ttu-id="1b7bd-121">Membres EsentTooManyColumnsException</span><span class="sxs-lookup"><span data-stu-id="1b7bd-121">EsentTooManyColumnsException members</span></span>](./esenttoomanycolumnsexception-members.md)

[<span data-ttu-id="1b7bd-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1b7bd-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
