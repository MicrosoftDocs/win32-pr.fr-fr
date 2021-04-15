---
description: 'En savoir plus sur : classe EsentInvalidLoggedOperationException'
title: EsentInvalidLoggedOperationException, classe
TOCTitle: EsentInvalidLoggedOperationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidLoggedOperationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidloggedoperationexception(v=EXCHG.10)
ms:contentKeyID: 55101979
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidLoggedOperationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidLoggedOperationException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d75ef32f471fcdae7e520844c4df8ef55260f682
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485425"
---
# <a name="esentinvalidloggedoperationexception-class"></a><span data-ttu-id="1daa8-103">EsentInvalidLoggedOperationException, classe</span><span class="sxs-lookup"><span data-stu-id="1daa8-103">EsentInvalidLoggedOperationException class</span></span>

<span data-ttu-id="1daa8-104">Classe de base pour JET_err. Exceptions InvalidLoggedOperation.</span><span class="sxs-lookup"><span data-stu-id="1daa8-104">Base class for JET_err.InvalidLoggedOperation exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="1daa8-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="1daa8-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="1daa8-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="1daa8-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="1daa8-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="1daa8-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="1daa8-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="1daa8-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="1daa8-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="1daa8-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="1daa8-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="1daa8-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="1daa8-111">Microsoft. ISAM. esent. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="1daa8-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="1daa8-112">Microsoft. ISAM. esent. Interop. EsentInvalidLoggedOperationException</span><span class="sxs-lookup"><span data-stu-id="1daa8-112">Microsoft.Isam.Esent.Interop.EsentInvalidLoggedOperationException</span></span>  

<span data-ttu-id="1daa8-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1daa8-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1daa8-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1daa8-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1daa8-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1daa8-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidLoggedOperationException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentInvalidLoggedOperationException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidLoggedOperationException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="1daa8-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="1daa8-116">Thread safety</span></span>

<span data-ttu-id="1daa8-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="1daa8-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="1daa8-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="1daa8-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="1daa8-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1daa8-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1daa8-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="1daa8-120">Reference</span></span>

[<span data-ttu-id="1daa8-121">Membres EsentInvalidLoggedOperationException</span><span class="sxs-lookup"><span data-stu-id="1daa8-121">EsentInvalidLoggedOperationException members</span></span>](./esentinvalidloggedoperationexception-members.md)

[<span data-ttu-id="1daa8-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1daa8-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
