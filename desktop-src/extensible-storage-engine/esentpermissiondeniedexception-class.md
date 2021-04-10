---
description: 'En savoir plus sur : classe EsentPermissionDeniedException'
title: EsentPermissionDeniedException, classe
TOCTitle: EsentPermissionDeniedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentPermissionDeniedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentpermissiondeniedexception(v=EXCHG.10)
ms:contentKeyID: 55107318
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentPermissionDeniedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentPermissionDeniedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ea3669f59ac4ad29d89379d656047a03c42ee907
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862978"
---
# <a name="esentpermissiondeniedexception-class"></a><span data-ttu-id="6eb00-103">EsentPermissionDeniedException, classe</span><span class="sxs-lookup"><span data-stu-id="6eb00-103">EsentPermissionDeniedException class</span></span>

<span data-ttu-id="6eb00-104">Classe de base pour JET_err. Exceptions PermissionDenied.</span><span class="sxs-lookup"><span data-stu-id="6eb00-104">Base class for JET_err.PermissionDenied exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="6eb00-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="6eb00-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="6eb00-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="6eb00-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="6eb00-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="6eb00-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="6eb00-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="6eb00-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="6eb00-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="6eb00-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="6eb00-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="6eb00-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="6eb00-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="6eb00-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="6eb00-112">Microsoft. ISAM. esent. Interop. EsentPermissionDeniedException</span><span class="sxs-lookup"><span data-stu-id="6eb00-112">Microsoft.Isam.Esent.Interop.EsentPermissionDeniedException</span></span>  

<span data-ttu-id="6eb00-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6eb00-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6eb00-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6eb00-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6eb00-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6eb00-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentPermissionDeniedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentPermissionDeniedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentPermissionDeniedException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="6eb00-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="6eb00-116">Thread safety</span></span>

<span data-ttu-id="6eb00-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="6eb00-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="6eb00-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="6eb00-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="6eb00-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6eb00-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6eb00-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="6eb00-120">Reference</span></span>

[<span data-ttu-id="6eb00-121">Membres EsentPermissionDeniedException</span><span class="sxs-lookup"><span data-stu-id="6eb00-121">EsentPermissionDeniedException members</span></span>](./esentpermissiondeniedexception-members.md)

[<span data-ttu-id="6eb00-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="6eb00-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
