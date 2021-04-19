---
description: 'En savoir plus sur : classe EsentAfterInitializationException'
title: EsentAfterInitializationException, classe
TOCTitle: EsentAfterInitializationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentAfterInitializationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentafterinitializationexception(v=EXCHG.10)
ms:contentKeyID: 55101005
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentAfterInitializationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentAfterInitializationException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f5680d6d13eaa556e0c210403066c807ef2505d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536783"
---
# <a name="esentafterinitializationexception-class"></a><span data-ttu-id="b4c0b-103">EsentAfterInitializationException, classe</span><span class="sxs-lookup"><span data-stu-id="b4c0b-103">EsentAfterInitializationException class</span></span>

<span data-ttu-id="b4c0b-104">Classe de base pour JET_err. Exceptions AfterInitialization.</span><span class="sxs-lookup"><span data-stu-id="b4c0b-104">Base class for JET_err.AfterInitialization exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b4c0b-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="b4c0b-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b4c0b-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b4c0b-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b4c0b-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="b4c0b-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b4c0b-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="b4c0b-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b4c0b-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="b4c0b-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="b4c0b-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="b4c0b-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="b4c0b-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="b4c0b-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="b4c0b-112">Microsoft. ISAM. esent. Interop. EsentAfterInitializationException</span><span class="sxs-lookup"><span data-stu-id="b4c0b-112">Microsoft.Isam.Esent.Interop.EsentAfterInitializationException</span></span>  

<span data-ttu-id="b4c0b-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b4c0b-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b4c0b-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b4c0b-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b4c0b-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4c0b-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentAfterInitializationException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentAfterInitializationException
```

``` csharp
[SerializableAttribute]
public sealed class EsentAfterInitializationException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="b4c0b-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="b4c0b-116">Thread safety</span></span>

<span data-ttu-id="b4c0b-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="b4c0b-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b4c0b-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="b4c0b-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b4c0b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4c0b-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b4c0b-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="b4c0b-120">Reference</span></span>

[<span data-ttu-id="b4c0b-121">Membres EsentAfterInitializationException</span><span class="sxs-lookup"><span data-stu-id="b4c0b-121">EsentAfterInitializationException members</span></span>](./esentafterinitializationexception-members.md)

[<span data-ttu-id="b4c0b-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b4c0b-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
