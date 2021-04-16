---
description: 'En savoir plus sur : classe EsentDistributedTransactionAlreadyPreparedToCommitException'
title: EsentDistributedTransactionAlreadyPreparedToCommitException, classe
TOCTitle: EsentDistributedTransactionAlreadyPreparedToCommitException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDistributedTransactionAlreadyPreparedToCommitException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdistributedtransactionalreadypreparedtocommitexception(v=EXCHG.10)
ms:contentKeyID: 55101543
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDistributedTransactionAlreadyPreparedToCommitException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDistributedTransactionAlreadyPreparedToCommitException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bbf4c9b6059cafa6a8cd2c35ce1a26e82fc8804d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393711"
---
# <a name="esentdistributedtransactionalreadypreparedtocommitexception-class"></a><span data-ttu-id="1fc0e-103">EsentDistributedTransactionAlreadyPreparedToCommitException, classe</span><span class="sxs-lookup"><span data-stu-id="1fc0e-103">EsentDistributedTransactionAlreadyPreparedToCommitException class</span></span>

<span data-ttu-id="1fc0e-104">Classe de base pour JET_err. Exceptions DistributedTransactionAlreadyPreparedToCommit.</span><span class="sxs-lookup"><span data-stu-id="1fc0e-104">Base class for JET_err.DistributedTransactionAlreadyPreparedToCommit exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="1fc0e-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="1fc0e-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="1fc0e-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="1fc0e-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="1fc0e-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="1fc0e-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="1fc0e-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="1fc0e-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="1fc0e-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="1fc0e-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="1fc0e-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="1fc0e-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="1fc0e-111">Microsoft. ISAM. esent. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="1fc0e-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="1fc0e-112">Microsoft. ISAM. esent. Interop. EsentDistributedTransactionAlreadyPreparedToCommitException</span><span class="sxs-lookup"><span data-stu-id="1fc0e-112">Microsoft.Isam.Esent.Interop.EsentDistributedTransactionAlreadyPreparedToCommitException</span></span>  

<span data-ttu-id="1fc0e-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1fc0e-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1fc0e-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1fc0e-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1fc0e-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1fc0e-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDistributedTransactionAlreadyPreparedToCommitException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentDistributedTransactionAlreadyPreparedToCommitException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDistributedTransactionAlreadyPreparedToCommitException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="1fc0e-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="1fc0e-116">Thread safety</span></span>

<span data-ttu-id="1fc0e-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="1fc0e-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="1fc0e-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="1fc0e-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="1fc0e-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1fc0e-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1fc0e-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="1fc0e-120">Reference</span></span>

[<span data-ttu-id="1fc0e-121">Membres EsentDistributedTransactionAlreadyPreparedToCommitException</span><span class="sxs-lookup"><span data-stu-id="1fc0e-121">EsentDistributedTransactionAlreadyPreparedToCommitException members</span></span>](./esentdistributedtransactionalreadypreparedtocommitexception-members.md)

[<span data-ttu-id="1fc0e-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1fc0e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
