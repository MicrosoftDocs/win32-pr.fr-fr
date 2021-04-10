---
description: 'En savoir plus sur : classe EsentNotInDistributedTransactionException'
title: EsentNotInDistributedTransactionException, classe
TOCTitle: EsentNotInDistributedTransactionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentNotInDistributedTransactionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentnotindistributedtransactionexception(v=EXCHG.10)
ms:contentKeyID: 55102293
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentNotInDistributedTransactionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentNotInDistributedTransactionException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 983aa045b83a0382a3ec7676080f3cdada5e1517
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953133"
---
# <a name="esentnotindistributedtransactionexception-class"></a><span data-ttu-id="b27e3-103">EsentNotInDistributedTransactionException, classe</span><span class="sxs-lookup"><span data-stu-id="b27e3-103">EsentNotInDistributedTransactionException class</span></span>

<span data-ttu-id="b27e3-104">Classe de base pour JET_err. Exceptions NotInDistributedTransaction.</span><span class="sxs-lookup"><span data-stu-id="b27e3-104">Base class for JET_err.NotInDistributedTransaction exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b27e3-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="b27e3-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b27e3-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b27e3-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b27e3-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="b27e3-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b27e3-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="b27e3-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b27e3-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="b27e3-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="b27e3-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="b27e3-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="b27e3-111">Microsoft. ISAM. esent. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="b27e3-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="b27e3-112">Microsoft. ISAM. esent. Interop. EsentNotInDistributedTransactionException</span><span class="sxs-lookup"><span data-stu-id="b27e3-112">Microsoft.Isam.Esent.Interop.EsentNotInDistributedTransactionException</span></span>  

<span data-ttu-id="b27e3-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b27e3-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b27e3-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b27e3-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b27e3-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b27e3-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentNotInDistributedTransactionException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentNotInDistributedTransactionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentNotInDistributedTransactionException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="b27e3-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="b27e3-116">Thread safety</span></span>

<span data-ttu-id="b27e3-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="b27e3-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b27e3-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="b27e3-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b27e3-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b27e3-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b27e3-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="b27e3-120">Reference</span></span>

[<span data-ttu-id="b27e3-121">Membres EsentNotInDistributedTransactionException</span><span class="sxs-lookup"><span data-stu-id="b27e3-121">EsentNotInDistributedTransactionException members</span></span>](./esentnotindistributedtransactionexception-members.md)

[<span data-ttu-id="b27e3-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b27e3-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
