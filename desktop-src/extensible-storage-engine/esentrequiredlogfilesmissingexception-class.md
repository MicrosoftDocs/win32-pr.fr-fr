---
description: 'En savoir plus sur : classe EsentRequiredLogFilesMissingException'
title: EsentRequiredLogFilesMissingException, classe
TOCTitle: EsentRequiredLogFilesMissingException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRequiredLogFilesMissingException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrequiredlogfilesmissingexception(v=EXCHG.10)
ms:contentKeyID: 55102617
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRequiredLogFilesMissingException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRequiredLogFilesMissingException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c2ac90c685daa306d260c5386bae4e988d6d25a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033899"
---
# <a name="esentrequiredlogfilesmissingexception-class"></a><span data-ttu-id="f0b07-103">EsentRequiredLogFilesMissingException, classe</span><span class="sxs-lookup"><span data-stu-id="f0b07-103">EsentRequiredLogFilesMissingException class</span></span>

<span data-ttu-id="f0b07-104">Classe de base pour JET_err. Exceptions RequiredLogFilesMissing.</span><span class="sxs-lookup"><span data-stu-id="f0b07-104">Base class for JET_err.RequiredLogFilesMissing exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f0b07-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="f0b07-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="f0b07-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="f0b07-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f0b07-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="f0b07-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="f0b07-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="f0b07-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="f0b07-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="f0b07-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="f0b07-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="f0b07-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="f0b07-111">Microsoft. ISAM. esent. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="f0b07-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="f0b07-112">Microsoft. ISAM. esent. Interop. EsentRequiredLogFilesMissingException</span><span class="sxs-lookup"><span data-stu-id="f0b07-112">Microsoft.Isam.Esent.Interop.EsentRequiredLogFilesMissingException</span></span>  

<span data-ttu-id="f0b07-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f0b07-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f0b07-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f0b07-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f0b07-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0b07-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRequiredLogFilesMissingException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentRequiredLogFilesMissingException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRequiredLogFilesMissingException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="f0b07-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="f0b07-116">Thread safety</span></span>

<span data-ttu-id="f0b07-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="f0b07-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f0b07-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="f0b07-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f0b07-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0b07-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f0b07-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="f0b07-120">Reference</span></span>

[<span data-ttu-id="f0b07-121">Membres EsentRequiredLogFilesMissingException</span><span class="sxs-lookup"><span data-stu-id="f0b07-121">EsentRequiredLogFilesMissingException members</span></span>](./esentrequiredlogfilesmissingexception-members.md)

[<span data-ttu-id="f0b07-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f0b07-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
