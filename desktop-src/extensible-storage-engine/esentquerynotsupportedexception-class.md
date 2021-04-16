---
description: 'En savoir plus sur : classe EsentQueryNotSupportedException'
title: EsentQueryNotSupportedException, classe
TOCTitle: EsentQueryNotSupportedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentQueryNotSupportedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentquerynotsupportedexception(v=EXCHG.10)
ms:contentKeyID: 55107329
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentQueryNotSupportedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentQueryNotSupportedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f67b181d509335a94ebd5cdb1c6f4a18e57a4886
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393644"
---
# <a name="esentquerynotsupportedexception-class"></a><span data-ttu-id="44a9f-103">EsentQueryNotSupportedException, classe</span><span class="sxs-lookup"><span data-stu-id="44a9f-103">EsentQueryNotSupportedException class</span></span>

<span data-ttu-id="44a9f-104">Classe de base pour JET_err. Exceptions QueryNotSupported.</span><span class="sxs-lookup"><span data-stu-id="44a9f-104">Base class for JET_err.QueryNotSupported exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="44a9f-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="44a9f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="44a9f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="44a9f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="44a9f-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="44a9f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="44a9f-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="44a9f-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="44a9f-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="44a9f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="44a9f-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="44a9f-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="44a9f-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="44a9f-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="44a9f-112">Microsoft. ISAM. esent. Interop. EsentQueryNotSupportedException</span><span class="sxs-lookup"><span data-stu-id="44a9f-112">Microsoft.Isam.Esent.Interop.EsentQueryNotSupportedException</span></span>  

<span data-ttu-id="44a9f-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="44a9f-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="44a9f-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="44a9f-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="44a9f-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44a9f-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentQueryNotSupportedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentQueryNotSupportedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentQueryNotSupportedException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="44a9f-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="44a9f-116">Thread safety</span></span>

<span data-ttu-id="44a9f-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="44a9f-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="44a9f-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="44a9f-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="44a9f-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44a9f-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="44a9f-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="44a9f-120">Reference</span></span>

[<span data-ttu-id="44a9f-121">Membres EsentQueryNotSupportedException</span><span class="sxs-lookup"><span data-stu-id="44a9f-121">EsentQueryNotSupportedException members</span></span>](./esentquerynotsupportedexception-members.md)

[<span data-ttu-id="44a9f-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="44a9f-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
