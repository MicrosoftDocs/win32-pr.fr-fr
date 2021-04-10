---
description: 'En savoir plus sur : classe EsentLogCorruptDuringHardRestoreException'
title: EsentLogCorruptDuringHardRestoreException, classe
TOCTitle: EsentLogCorruptDuringHardRestoreException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRestoreException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogcorruptduringhardrestoreexception(v=EXCHG.10)
ms:contentKeyID: 55102073
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRestoreException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRestoreException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: daeabeae72916781e01640cd0de10c737b53e5ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210656"
---
# <a name="esentlogcorruptduringhardrestoreexception-class"></a><span data-ttu-id="ee7a9-103">EsentLogCorruptDuringHardRestoreException, classe</span><span class="sxs-lookup"><span data-stu-id="ee7a9-103">EsentLogCorruptDuringHardRestoreException class</span></span>

<span data-ttu-id="ee7a9-104">Classe de base pour JET_err. Exceptions LogCorruptDuringHardRestore.</span><span class="sxs-lookup"><span data-stu-id="ee7a9-104">Base class for JET_err.LogCorruptDuringHardRestore exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ee7a9-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="ee7a9-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ee7a9-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ee7a9-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ee7a9-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="ee7a9-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ee7a9-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="ee7a9-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ee7a9-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="ee7a9-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ee7a9-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="ee7a9-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="ee7a9-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="ee7a9-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="ee7a9-112">Microsoft. ISAM. esent. Interop. EsentLogCorruptDuringHardRestoreException</span><span class="sxs-lookup"><span data-stu-id="ee7a9-112">Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRestoreException</span></span>  

<span data-ttu-id="ee7a9-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ee7a9-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ee7a9-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ee7a9-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ee7a9-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee7a9-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogCorruptDuringHardRestoreException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentLogCorruptDuringHardRestoreException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogCorruptDuringHardRestoreException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="ee7a9-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="ee7a9-116">Thread safety</span></span>

<span data-ttu-id="ee7a9-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="ee7a9-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ee7a9-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="ee7a9-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ee7a9-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee7a9-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ee7a9-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="ee7a9-120">Reference</span></span>

[<span data-ttu-id="ee7a9-121">Membres EsentLogCorruptDuringHardRestoreException</span><span class="sxs-lookup"><span data-stu-id="ee7a9-121">EsentLogCorruptDuringHardRestoreException members</span></span>](./esentlogcorruptduringhardrestoreexception-members.md)

[<span data-ttu-id="ee7a9-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ee7a9-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
