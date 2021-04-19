---
description: 'En savoir plus sur : classe EsentKeyNotMadeException'
title: EsentKeyNotMadeException, classe
TOCTitle: EsentKeyNotMadeException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentKeyNotMadeException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentkeynotmadeexception(v=EXCHG.10)
ms:contentKeyID: 55102115
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentKeyNotMadeException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentKeyNotMadeException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e77be995e6f06aaa7058455f9e0f64bd9721f6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545037"
---
# <a name="esentkeynotmadeexception-class"></a><span data-ttu-id="f78b2-103">EsentKeyNotMadeException, classe</span><span class="sxs-lookup"><span data-stu-id="f78b2-103">EsentKeyNotMadeException class</span></span>

<span data-ttu-id="f78b2-104">Classe de base pour JET_err. Exceptions KeyNotMade.</span><span class="sxs-lookup"><span data-stu-id="f78b2-104">Base class for JET_err.KeyNotMade exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f78b2-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="f78b2-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="f78b2-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="f78b2-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f78b2-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="f78b2-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="f78b2-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="f78b2-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="f78b2-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="f78b2-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="f78b2-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="f78b2-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="f78b2-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="f78b2-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="f78b2-112">Microsoft. ISAM. esent. Interop. EsentKeyNotMadeException</span><span class="sxs-lookup"><span data-stu-id="f78b2-112">Microsoft.Isam.Esent.Interop.EsentKeyNotMadeException</span></span>  

<span data-ttu-id="f78b2-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f78b2-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f78b2-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f78b2-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f78b2-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f78b2-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentKeyNotMadeException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentKeyNotMadeException
```

``` csharp
[SerializableAttribute]
public sealed class EsentKeyNotMadeException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="f78b2-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="f78b2-116">Thread safety</span></span>

<span data-ttu-id="f78b2-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="f78b2-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f78b2-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="f78b2-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f78b2-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f78b2-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f78b2-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="f78b2-120">Reference</span></span>

[<span data-ttu-id="f78b2-121">Membres EsentKeyNotMadeException</span><span class="sxs-lookup"><span data-stu-id="f78b2-121">EsentKeyNotMadeException members</span></span>](./esentkeynotmadeexception-members.md)

[<span data-ttu-id="f78b2-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f78b2-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
