---
description: 'En savoir plus sur : classe EsentLogCorruptDuringHardRecoveryException'
title: EsentLogCorruptDuringHardRecoveryException, classe
TOCTitle: EsentLogCorruptDuringHardRecoveryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRecoveryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogcorruptduringhardrecoveryexception(v=EXCHG.10)
ms:contentKeyID: 55102063
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRecoveryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRecoveryException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: da137553a791b92a929d60dc9cc9cd764695c784
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527706"
---
# <a name="esentlogcorruptduringhardrecoveryexception-class"></a><span data-ttu-id="355d6-103">EsentLogCorruptDuringHardRecoveryException, classe</span><span class="sxs-lookup"><span data-stu-id="355d6-103">EsentLogCorruptDuringHardRecoveryException class</span></span>

<span data-ttu-id="355d6-104">Classe de base pour JET_err. Exceptions LogCorruptDuringHardRecovery.</span><span class="sxs-lookup"><span data-stu-id="355d6-104">Base class for JET_err.LogCorruptDuringHardRecovery exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="355d6-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="355d6-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="355d6-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="355d6-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="355d6-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="355d6-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="355d6-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="355d6-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="355d6-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="355d6-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="355d6-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="355d6-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="355d6-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="355d6-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="355d6-112">Microsoft. ISAM. esent. Interop. EsentLogCorruptDuringHardRecoveryException</span><span class="sxs-lookup"><span data-stu-id="355d6-112">Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRecoveryException</span></span>  

<span data-ttu-id="355d6-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="355d6-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="355d6-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="355d6-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="355d6-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="355d6-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogCorruptDuringHardRecoveryException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentLogCorruptDuringHardRecoveryException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogCorruptDuringHardRecoveryException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="355d6-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="355d6-116">Thread safety</span></span>

<span data-ttu-id="355d6-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="355d6-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="355d6-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="355d6-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="355d6-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="355d6-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="355d6-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="355d6-120">Reference</span></span>

[<span data-ttu-id="355d6-121">Membres EsentLogCorruptDuringHardRecoveryException</span><span class="sxs-lookup"><span data-stu-id="355d6-121">EsentLogCorruptDuringHardRecoveryException members</span></span>](./esentlogcorruptduringhardrecoveryexception-members.md)

[<span data-ttu-id="355d6-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="355d6-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
