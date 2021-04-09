---
description: 'En savoir plus sur : classe EsentDiskReadVerificationFailureException'
title: EsentDiskReadVerificationFailureException, classe
TOCTitle: EsentDiskReadVerificationFailureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDiskReadVerificationFailureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdiskreadverificationfailureexception(v=EXCHG.10)
ms:contentKeyID: 55101620
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDiskReadVerificationFailureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDiskReadVerificationFailureException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f429efb66f5993f438e132ed564f110e88d234a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210510"
---
# <a name="esentdiskreadverificationfailureexception-class"></a><span data-ttu-id="3fc2f-103">EsentDiskReadVerificationFailureException, classe</span><span class="sxs-lookup"><span data-stu-id="3fc2f-103">EsentDiskReadVerificationFailureException class</span></span>

<span data-ttu-id="3fc2f-104">Classe de base pour JET_err. Exceptions DiskReadVerificationFailure.</span><span class="sxs-lookup"><span data-stu-id="3fc2f-104">Base class for JET_err.DiskReadVerificationFailure exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="3fc2f-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="3fc2f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="3fc2f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="3fc2f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="3fc2f-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="3fc2f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="3fc2f-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="3fc2f-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="3fc2f-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="3fc2f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="3fc2f-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="3fc2f-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="3fc2f-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="3fc2f-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="3fc2f-112">Microsoft. ISAM. esent. Interop. EsentDiskReadVerificationFailureException</span><span class="sxs-lookup"><span data-stu-id="3fc2f-112">Microsoft.Isam.Esent.Interop.EsentDiskReadVerificationFailureException</span></span>  

<span data-ttu-id="3fc2f-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3fc2f-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3fc2f-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3fc2f-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3fc2f-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3fc2f-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDiskReadVerificationFailureException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentDiskReadVerificationFailureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDiskReadVerificationFailureException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="3fc2f-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="3fc2f-116">Thread safety</span></span>

<span data-ttu-id="3fc2f-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="3fc2f-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="3fc2f-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="3fc2f-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="3fc2f-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3fc2f-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3fc2f-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="3fc2f-120">Reference</span></span>

[<span data-ttu-id="3fc2f-121">Membres EsentDiskReadVerificationFailureException</span><span class="sxs-lookup"><span data-stu-id="3fc2f-121">EsentDiskReadVerificationFailureException members</span></span>](./esentdiskreadverificationfailureexception-members.md)

[<span data-ttu-id="3fc2f-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3fc2f-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
