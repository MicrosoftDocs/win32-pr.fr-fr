---
description: 'En savoir plus sur : classe EsentWriteConflictException'
title: EsentWriteConflictException, classe
TOCTitle: EsentWriteConflictException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentWriteConflictException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentwriteconflictexception(v=EXCHG.10)
ms:contentKeyID: 55103199
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentWriteConflictException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentWriteConflictException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fffcb0b2bb07e12dc4dd9f86de5c22b13aca66b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523071"
---
# <a name="esentwriteconflictexception-class"></a><span data-ttu-id="108e7-103">EsentWriteConflictException, classe</span><span class="sxs-lookup"><span data-stu-id="108e7-103">EsentWriteConflictException class</span></span>

<span data-ttu-id="108e7-104">Classe de base pour JET_err. Exceptions WriteConflict.</span><span class="sxs-lookup"><span data-stu-id="108e7-104">Base class for JET_err.WriteConflict exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="108e7-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="108e7-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="108e7-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="108e7-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="108e7-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="108e7-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="108e7-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="108e7-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="108e7-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="108e7-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="108e7-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="108e7-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="108e7-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="108e7-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="108e7-112">Microsoft. ISAM. esent. Interop. EsentWriteConflictException</span><span class="sxs-lookup"><span data-stu-id="108e7-112">Microsoft.Isam.Esent.Interop.EsentWriteConflictException</span></span>  

<span data-ttu-id="108e7-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="108e7-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="108e7-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="108e7-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="108e7-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="108e7-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentWriteConflictException _
    Inherits EsentStateException
'Usage
Dim instance As EsentWriteConflictException
```

``` csharp
[SerializableAttribute]
public sealed class EsentWriteConflictException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="108e7-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="108e7-116">Thread safety</span></span>

<span data-ttu-id="108e7-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="108e7-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="108e7-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="108e7-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="108e7-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="108e7-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="108e7-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="108e7-120">Reference</span></span>

[<span data-ttu-id="108e7-121">Membres EsentWriteConflictException</span><span class="sxs-lookup"><span data-stu-id="108e7-121">EsentWriteConflictException members</span></span>](./esentwriteconflictexception-members.md)

[<span data-ttu-id="108e7-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="108e7-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
