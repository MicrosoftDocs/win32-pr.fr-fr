---
description: 'En savoir plus sur : classe EsentKeyDuplicateException'
title: EsentKeyDuplicateException, classe
TOCTitle: EsentKeyDuplicateException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentKeyDuplicateException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentkeyduplicateexception(v=EXCHG.10)
ms:contentKeyID: 55102039
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentKeyDuplicateException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentKeyDuplicateException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0d63945d5db3ca97e858e7f02fd2b4e8a9045f86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320778"
---
# <a name="esentkeyduplicateexception-class"></a><span data-ttu-id="8f06d-103">EsentKeyDuplicateException, classe</span><span class="sxs-lookup"><span data-stu-id="8f06d-103">EsentKeyDuplicateException class</span></span>

<span data-ttu-id="8f06d-104">Classe de base pour JET_err. Exceptions KeyDuplicate.</span><span class="sxs-lookup"><span data-stu-id="8f06d-104">Base class for JET_err.KeyDuplicate exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="8f06d-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="8f06d-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="8f06d-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="8f06d-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="8f06d-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="8f06d-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="8f06d-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="8f06d-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="8f06d-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="8f06d-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="8f06d-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="8f06d-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="8f06d-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="8f06d-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="8f06d-112">Microsoft. ISAM. esent. Interop. EsentKeyDuplicateException</span><span class="sxs-lookup"><span data-stu-id="8f06d-112">Microsoft.Isam.Esent.Interop.EsentKeyDuplicateException</span></span>  

<span data-ttu-id="8f06d-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8f06d-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8f06d-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8f06d-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8f06d-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8f06d-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentKeyDuplicateException _
    Inherits EsentStateException
'Usage
Dim instance As EsentKeyDuplicateException
```

``` csharp
[SerializableAttribute]
public sealed class EsentKeyDuplicateException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="8f06d-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="8f06d-116">Thread safety</span></span>

<span data-ttu-id="8f06d-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="8f06d-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="8f06d-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="8f06d-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="8f06d-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f06d-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8f06d-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="8f06d-120">Reference</span></span>

[<span data-ttu-id="8f06d-121">Membres EsentKeyDuplicateException</span><span class="sxs-lookup"><span data-stu-id="8f06d-121">EsentKeyDuplicateException members</span></span>](./esentkeyduplicateexception-members.md)

[<span data-ttu-id="8f06d-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8f06d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
