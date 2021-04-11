---
description: 'En savoir plus sur : classe EsentInvalidInstanceException'
title: EsentInvalidInstanceException, classe
TOCTitle: EsentInvalidInstanceException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidInstanceException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidinstanceexception(v=EXCHG.10)
ms:contentKeyID: 55101939
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidInstanceException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidInstanceException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ba855e89f7714b7042b882b5c8cb28eba3dca3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209840"
---
# <a name="esentinvalidinstanceexception-class"></a><span data-ttu-id="1ef52-103">EsentInvalidInstanceException, classe</span><span class="sxs-lookup"><span data-stu-id="1ef52-103">EsentInvalidInstanceException class</span></span>

<span data-ttu-id="1ef52-104">Classe de base pour JET_err. Exceptions InvalidInstance.</span><span class="sxs-lookup"><span data-stu-id="1ef52-104">Base class for JET_err.InvalidInstance exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="1ef52-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="1ef52-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="1ef52-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="1ef52-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="1ef52-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="1ef52-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="1ef52-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="1ef52-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="1ef52-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="1ef52-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="1ef52-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="1ef52-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="1ef52-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="1ef52-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="1ef52-112">Microsoft. ISAM. esent. Interop. EsentInvalidInstanceException</span><span class="sxs-lookup"><span data-stu-id="1ef52-112">Microsoft.Isam.Esent.Interop.EsentInvalidInstanceException</span></span>  

<span data-ttu-id="1ef52-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1ef52-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1ef52-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1ef52-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1ef52-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ef52-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidInstanceException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentInvalidInstanceException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidInstanceException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="1ef52-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="1ef52-116">Thread safety</span></span>

<span data-ttu-id="1ef52-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="1ef52-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="1ef52-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="1ef52-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="1ef52-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ef52-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1ef52-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="1ef52-120">Reference</span></span>

[<span data-ttu-id="1ef52-121">Membres EsentInvalidInstanceException</span><span class="sxs-lookup"><span data-stu-id="1ef52-121">EsentInvalidInstanceException members</span></span>](./esentinvalidinstanceexception-members.md)

[<span data-ttu-id="1ef52-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1ef52-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
