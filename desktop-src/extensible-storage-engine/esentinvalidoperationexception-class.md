---
description: 'En savoir plus sur : classe EsentInvalidOperationException'
title: EsentInvalidOperationException, classe
TOCTitle: EsentInvalidOperationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidOperationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidoperationexception(v=EXCHG.10)
ms:contentKeyID: 55102007
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidOperationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidOperationException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ccf4c4fe3b980251c91d11387af02c56cc23772f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321173"
---
# <a name="esentinvalidoperationexception-class"></a><span data-ttu-id="34953-103">EsentInvalidOperationException, classe</span><span class="sxs-lookup"><span data-stu-id="34953-103">EsentInvalidOperationException class</span></span>

<span data-ttu-id="34953-104">Classe de base pour JET_err. Exceptions InvalidOperation.</span><span class="sxs-lookup"><span data-stu-id="34953-104">Base class for JET_err.InvalidOperation exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="34953-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="34953-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="34953-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="34953-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="34953-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="34953-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="34953-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="34953-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="34953-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="34953-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="34953-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="34953-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="34953-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="34953-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="34953-112">Microsoft. ISAM. esent. Interop. EsentInvalidOperationException</span><span class="sxs-lookup"><span data-stu-id="34953-112">Microsoft.Isam.Esent.Interop.EsentInvalidOperationException</span></span>  

<span data-ttu-id="34953-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="34953-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="34953-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="34953-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="34953-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34953-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidOperationException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentInvalidOperationException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidOperationException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="34953-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="34953-116">Thread safety</span></span>

<span data-ttu-id="34953-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="34953-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="34953-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="34953-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="34953-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34953-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="34953-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="34953-120">Reference</span></span>

[<span data-ttu-id="34953-121">Membres EsentInvalidOperationException</span><span class="sxs-lookup"><span data-stu-id="34953-121">EsentInvalidOperationException members</span></span>](./esentinvalidoperationexception-members.md)

[<span data-ttu-id="34953-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="34953-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
