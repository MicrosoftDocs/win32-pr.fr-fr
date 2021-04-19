---
description: 'En savoir plus sur : classe EsentCheckpointCorruptException'
title: EsentCheckpointCorruptException, classe
TOCTitle: EsentCheckpointCorruptException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCheckpointCorruptException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcheckpointcorruptexception(v=EXCHG.10)
ms:contentKeyID: 55101237
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCheckpointCorruptException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCheckpointCorruptException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d0654ff85fa74cca8435ca6366e301bc3c70fc53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534166"
---
# <a name="esentcheckpointcorruptexception-class"></a><span data-ttu-id="5e666-103">EsentCheckpointCorruptException, classe</span><span class="sxs-lookup"><span data-stu-id="5e666-103">EsentCheckpointCorruptException class</span></span>

<span data-ttu-id="5e666-104">Classe de base pour JET_err. Exceptions CheckpointCorrupt.</span><span class="sxs-lookup"><span data-stu-id="5e666-104">Base class for JET_err.CheckpointCorrupt exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="5e666-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="5e666-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="5e666-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="5e666-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="5e666-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="5e666-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="5e666-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="5e666-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="5e666-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="5e666-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="5e666-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="5e666-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="5e666-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="5e666-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="5e666-112">Microsoft. ISAM. esent. Interop. EsentCheckpointCorruptException</span><span class="sxs-lookup"><span data-stu-id="5e666-112">Microsoft.Isam.Esent.Interop.EsentCheckpointCorruptException</span></span>  

<span data-ttu-id="5e666-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5e666-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5e666-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5e666-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5e666-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e666-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCheckpointCorruptException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentCheckpointCorruptException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCheckpointCorruptException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="5e666-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="5e666-116">Thread safety</span></span>

<span data-ttu-id="5e666-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="5e666-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="5e666-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="5e666-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="5e666-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e666-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5e666-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="5e666-120">Reference</span></span>

[<span data-ttu-id="5e666-121">Membres EsentCheckpointCorruptException</span><span class="sxs-lookup"><span data-stu-id="5e666-121">EsentCheckpointCorruptException members</span></span>](./esentcheckpointcorruptexception-members.md)

[<span data-ttu-id="5e666-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="5e666-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
