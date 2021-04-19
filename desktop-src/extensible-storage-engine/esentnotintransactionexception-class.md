---
description: 'En savoir plus sur : classe EsentNotInTransactionException'
title: EsentNotInTransactionException, classe
TOCTitle: EsentNotInTransactionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentNotInTransactionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentnotintransactionexception(v=EXCHG.10)
ms:contentKeyID: 55107294
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentNotInTransactionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentNotInTransactionException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1630ecc3cea33af09c0c81be69beb9a852609f32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518495"
---
# <a name="esentnotintransactionexception-class"></a><span data-ttu-id="d1211-103">EsentNotInTransactionException, classe</span><span class="sxs-lookup"><span data-stu-id="d1211-103">EsentNotInTransactionException class</span></span>

<span data-ttu-id="d1211-104">Classe de base pour JET_err. Exceptions NotInTransaction.</span><span class="sxs-lookup"><span data-stu-id="d1211-104">Base class for JET_err.NotInTransaction exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="d1211-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="d1211-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="d1211-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="d1211-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="d1211-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="d1211-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="d1211-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="d1211-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="d1211-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="d1211-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="d1211-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="d1211-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="d1211-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="d1211-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="d1211-112">Microsoft. ISAM. esent. Interop. EsentNotInTransactionException</span><span class="sxs-lookup"><span data-stu-id="d1211-112">Microsoft.Isam.Esent.Interop.EsentNotInTransactionException</span></span>  

<span data-ttu-id="d1211-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d1211-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d1211-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d1211-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d1211-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1211-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentNotInTransactionException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentNotInTransactionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentNotInTransactionException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="d1211-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="d1211-116">Thread safety</span></span>

<span data-ttu-id="d1211-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="d1211-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="d1211-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="d1211-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="d1211-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1211-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d1211-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="d1211-120">Reference</span></span>

[<span data-ttu-id="d1211-121">Membres EsentNotInTransactionException</span><span class="sxs-lookup"><span data-stu-id="d1211-121">EsentNotInTransactionException members</span></span>](./esentnotintransactionexception-members.md)

[<span data-ttu-id="d1211-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d1211-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
