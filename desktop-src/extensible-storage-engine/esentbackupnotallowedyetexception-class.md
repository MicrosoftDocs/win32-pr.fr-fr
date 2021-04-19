---
description: 'En savoir plus sur : classe EsentBackupNotAllowedYetException'
title: EsentBackupNotAllowedYetException, classe
TOCTitle: EsentBackupNotAllowedYetException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBackupNotAllowedYetException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbackupnotallowedyetexception(v=EXCHG.10)
ms:contentKeyID: 55101088
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBackupNotAllowedYetException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBackupNotAllowedYetException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5481c51c4a0b78ea1b66b950ac53d2a04c28595
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530216"
---
# <a name="esentbackupnotallowedyetexception-class"></a><span data-ttu-id="2a3d9-103">EsentBackupNotAllowedYetException, classe</span><span class="sxs-lookup"><span data-stu-id="2a3d9-103">EsentBackupNotAllowedYetException class</span></span>

<span data-ttu-id="2a3d9-104">Classe de base pour JET_err. Exceptions BackupNotAllowedYet.</span><span class="sxs-lookup"><span data-stu-id="2a3d9-104">Base class for JET_err.BackupNotAllowedYet exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="2a3d9-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="2a3d9-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="2a3d9-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="2a3d9-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="2a3d9-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="2a3d9-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="2a3d9-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="2a3d9-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="2a3d9-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="2a3d9-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="2a3d9-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="2a3d9-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="2a3d9-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="2a3d9-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="2a3d9-112">Microsoft. ISAM. esent. Interop. EsentBackupNotAllowedYetException</span><span class="sxs-lookup"><span data-stu-id="2a3d9-112">Microsoft.Isam.Esent.Interop.EsentBackupNotAllowedYetException</span></span>  

<span data-ttu-id="2a3d9-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2a3d9-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2a3d9-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2a3d9-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2a3d9-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a3d9-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBackupNotAllowedYetException _
    Inherits EsentStateException
'Usage
Dim instance As EsentBackupNotAllowedYetException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBackupNotAllowedYetException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="2a3d9-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="2a3d9-116">Thread safety</span></span>

<span data-ttu-id="2a3d9-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="2a3d9-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="2a3d9-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="2a3d9-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="2a3d9-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a3d9-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2a3d9-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="2a3d9-120">Reference</span></span>

[<span data-ttu-id="2a3d9-121">Membres EsentBackupNotAllowedYetException</span><span class="sxs-lookup"><span data-stu-id="2a3d9-121">EsentBackupNotAllowedYetException members</span></span>](./esentbackupnotallowedyetexception-members.md)

[<span data-ttu-id="2a3d9-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2a3d9-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
