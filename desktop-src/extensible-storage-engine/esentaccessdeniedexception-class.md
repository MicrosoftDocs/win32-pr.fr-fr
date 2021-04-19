---
description: 'En savoir plus sur : classe EsentAccessDeniedException'
title: EsentAccessDeniedException, classe
TOCTitle: EsentAccessDeniedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentAccessDeniedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentaccessdeniedexception(v=EXCHG.10)
ms:contentKeyID: 55101035
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentAccessDeniedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentAccessDeniedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7d81979a93bfa2ad3801047e5ec5cac9796bcda8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530197"
---
# <a name="esentaccessdeniedexception-class"></a><span data-ttu-id="d8b23-103">EsentAccessDeniedException, classe</span><span class="sxs-lookup"><span data-stu-id="d8b23-103">EsentAccessDeniedException class</span></span>

<span data-ttu-id="d8b23-104">Classe de base pour JET_err. Exceptions AccessDenied.</span><span class="sxs-lookup"><span data-stu-id="d8b23-104">Base class for JET_err.AccessDenied exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="d8b23-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="d8b23-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="d8b23-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="d8b23-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="d8b23-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="d8b23-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="d8b23-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="d8b23-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="d8b23-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="d8b23-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="d8b23-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="d8b23-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="d8b23-111">Microsoft. ISAM. esent. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="d8b23-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="d8b23-112">Microsoft. ISAM. esent. Interop. EsentAccessDeniedException</span><span class="sxs-lookup"><span data-stu-id="d8b23-112">Microsoft.Isam.Esent.Interop.EsentAccessDeniedException</span></span>  

<span data-ttu-id="d8b23-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d8b23-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d8b23-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d8b23-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d8b23-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8b23-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentAccessDeniedException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentAccessDeniedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentAccessDeniedException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="d8b23-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="d8b23-116">Thread safety</span></span>

<span data-ttu-id="d8b23-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="d8b23-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="d8b23-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="d8b23-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="d8b23-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8b23-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d8b23-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="d8b23-120">Reference</span></span>

[<span data-ttu-id="d8b23-121">Membres EsentAccessDeniedException</span><span class="sxs-lookup"><span data-stu-id="d8b23-121">EsentAccessDeniedException members</span></span>](./esentaccessdeniedexception-members.md)

[<span data-ttu-id="d8b23-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d8b23-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
