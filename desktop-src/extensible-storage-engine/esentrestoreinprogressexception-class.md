---
description: 'En savoir plus sur : classe EsentRestoreInProgressException'
title: EsentRestoreInProgressException, classe
TOCTitle: EsentRestoreInProgressException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRestoreInProgressException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrestoreinprogressexception(v=EXCHG.10)
ms:contentKeyID: 55102631
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRestoreInProgressException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRestoreInProgressException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0906d1ee8c196260d36da8d385a0e48e12f31018
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523072"
---
# <a name="esentrestoreinprogressexception-class"></a><span data-ttu-id="8e3b7-103">EsentRestoreInProgressException, classe</span><span class="sxs-lookup"><span data-stu-id="8e3b7-103">EsentRestoreInProgressException class</span></span>

<span data-ttu-id="8e3b7-104">Classe de base pour JET_err. Exceptions RestoreInProgress.</span><span class="sxs-lookup"><span data-stu-id="8e3b7-104">Base class for JET_err.RestoreInProgress exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="8e3b7-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="8e3b7-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="8e3b7-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="8e3b7-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="8e3b7-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="8e3b7-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="8e3b7-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="8e3b7-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="8e3b7-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="8e3b7-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="8e3b7-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="8e3b7-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="8e3b7-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="8e3b7-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="8e3b7-112">Microsoft. ISAM. esent. Interop. EsentRestoreInProgressException</span><span class="sxs-lookup"><span data-stu-id="8e3b7-112">Microsoft.Isam.Esent.Interop.EsentRestoreInProgressException</span></span>  

<span data-ttu-id="8e3b7-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8e3b7-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8e3b7-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8e3b7-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8e3b7-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e3b7-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRestoreInProgressException _
    Inherits EsentStateException
'Usage
Dim instance As EsentRestoreInProgressException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRestoreInProgressException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="8e3b7-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="8e3b7-116">Thread safety</span></span>

<span data-ttu-id="8e3b7-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="8e3b7-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="8e3b7-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="8e3b7-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="8e3b7-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e3b7-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8e3b7-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="8e3b7-120">Reference</span></span>

[<span data-ttu-id="8e3b7-121">Membres EsentRestoreInProgressException</span><span class="sxs-lookup"><span data-stu-id="8e3b7-121">EsentRestoreInProgressException members</span></span>](./esentrestoreinprogressexception-members.md)

[<span data-ttu-id="8e3b7-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8e3b7-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
