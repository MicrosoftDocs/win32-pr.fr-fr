---
description: 'En savoir plus sur : classe EsentMissingFullBackupException'
title: EsentMissingFullBackupException, classe
TOCTitle: EsentMissingFullBackupException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMissingFullBackupException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmissingfullbackupexception(v=EXCHG.10)
ms:contentKeyID: 55102230
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMissingFullBackupException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMissingFullBackupException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c345475e9e23f60460d7ee5eb901e5997ecb6062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114767"
---
# <a name="esentmissingfullbackupexception-class"></a><span data-ttu-id="2543e-103">EsentMissingFullBackupException, classe</span><span class="sxs-lookup"><span data-stu-id="2543e-103">EsentMissingFullBackupException class</span></span>

<span data-ttu-id="2543e-104">Classe de base pour JET_err. Exceptions MissingFullBackup.</span><span class="sxs-lookup"><span data-stu-id="2543e-104">Base class for JET_err.MissingFullBackup exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="2543e-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="2543e-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="2543e-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="2543e-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="2543e-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="2543e-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="2543e-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="2543e-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="2543e-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="2543e-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="2543e-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="2543e-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="2543e-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="2543e-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="2543e-112">Microsoft. ISAM. esent. Interop. EsentMissingFullBackupException</span><span class="sxs-lookup"><span data-stu-id="2543e-112">Microsoft.Isam.Esent.Interop.EsentMissingFullBackupException</span></span>  

<span data-ttu-id="2543e-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2543e-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2543e-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2543e-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2543e-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2543e-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMissingFullBackupException _
    Inherits EsentStateException
'Usage
Dim instance As EsentMissingFullBackupException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMissingFullBackupException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="2543e-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="2543e-116">Thread safety</span></span>

<span data-ttu-id="2543e-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="2543e-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="2543e-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="2543e-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="2543e-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2543e-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2543e-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="2543e-120">Reference</span></span>

[<span data-ttu-id="2543e-121">Membres EsentMissingFullBackupException</span><span class="sxs-lookup"><span data-stu-id="2543e-121">EsentMissingFullBackupException members</span></span>](./esentmissingfullbackupexception-members.md)

[<span data-ttu-id="2543e-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2543e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
