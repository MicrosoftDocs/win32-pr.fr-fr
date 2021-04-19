---
description: 'En savoir plus sur : classe EsentLogFileCorruptException'
title: EsentLogFileCorruptException, classe
TOCTitle: EsentLogFileCorruptException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogFileCorruptException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogfilecorruptexception(v=EXCHG.10)
ms:contentKeyID: 55102161
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogFileCorruptException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogFileCorruptException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f2a3fa54d83cd1e88597b3689619e48a2372952e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519916"
---
# <a name="esentlogfilecorruptexception-class"></a><span data-ttu-id="41623-103">EsentLogFileCorruptException, classe</span><span class="sxs-lookup"><span data-stu-id="41623-103">EsentLogFileCorruptException class</span></span>

<span data-ttu-id="41623-104">Classe de base pour JET_err. Exceptions LogFileCorrupt.</span><span class="sxs-lookup"><span data-stu-id="41623-104">Base class for JET_err.LogFileCorrupt exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="41623-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="41623-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="41623-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="41623-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="41623-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="41623-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="41623-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="41623-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="41623-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="41623-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="41623-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="41623-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="41623-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="41623-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="41623-112">Microsoft. ISAM. esent. Interop. EsentLogFileCorruptException</span><span class="sxs-lookup"><span data-stu-id="41623-112">Microsoft.Isam.Esent.Interop.EsentLogFileCorruptException</span></span>  

<span data-ttu-id="41623-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="41623-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="41623-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="41623-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="41623-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41623-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogFileCorruptException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentLogFileCorruptException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogFileCorruptException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="41623-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="41623-116">Thread safety</span></span>

<span data-ttu-id="41623-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="41623-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="41623-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="41623-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="41623-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41623-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="41623-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="41623-120">Reference</span></span>

[<span data-ttu-id="41623-121">Membres EsentLogFileCorruptException</span><span class="sxs-lookup"><span data-stu-id="41623-121">EsentLogFileCorruptException members</span></span>](./esentlogfilecorruptexception-members.md)

[<span data-ttu-id="41623-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="41623-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
