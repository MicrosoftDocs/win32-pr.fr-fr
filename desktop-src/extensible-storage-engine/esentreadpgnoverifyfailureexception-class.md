---
description: 'En savoir plus sur : classe EsentReadPgnoVerifyFailureException'
title: EsentReadPgnoVerifyFailureException, classe
TOCTitle: EsentReadPgnoVerifyFailureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentReadPgnoVerifyFailureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentreadpgnoverifyfailureexception(v=EXCHG.10)
ms:contentKeyID: 55102553
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentReadPgnoVerifyFailureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentReadPgnoVerifyFailureException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0de6967016196e48fe15bf6f190d1a4207678bcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524556"
---
# <a name="esentreadpgnoverifyfailureexception-class"></a><span data-ttu-id="108a4-103">EsentReadPgnoVerifyFailureException, classe</span><span class="sxs-lookup"><span data-stu-id="108a4-103">EsentReadPgnoVerifyFailureException class</span></span>

<span data-ttu-id="108a4-104">Classe de base pour JET_err. Exceptions ReadPgnoVerifyFailure.</span><span class="sxs-lookup"><span data-stu-id="108a4-104">Base class for JET_err.ReadPgnoVerifyFailure exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="108a4-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="108a4-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="108a4-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="108a4-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="108a4-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="108a4-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="108a4-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="108a4-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="108a4-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="108a4-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="108a4-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="108a4-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="108a4-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="108a4-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="108a4-112">Microsoft. ISAM. esent. Interop. EsentReadPgnoVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="108a4-112">Microsoft.Isam.Esent.Interop.EsentReadPgnoVerifyFailureException</span></span>  

<span data-ttu-id="108a4-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="108a4-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="108a4-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="108a4-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="108a4-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="108a4-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentReadPgnoVerifyFailureException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentReadPgnoVerifyFailureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentReadPgnoVerifyFailureException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="108a4-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="108a4-116">Thread safety</span></span>

<span data-ttu-id="108a4-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="108a4-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="108a4-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="108a4-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="108a4-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="108a4-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="108a4-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="108a4-120">Reference</span></span>

[<span data-ttu-id="108a4-121">Membres EsentReadPgnoVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="108a4-121">EsentReadPgnoVerifyFailureException members</span></span>](./esentreadpgnoverifyfailureexception-members.md)

[<span data-ttu-id="108a4-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="108a4-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
