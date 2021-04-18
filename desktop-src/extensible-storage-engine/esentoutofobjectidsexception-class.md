---
description: 'En savoir plus sur : classe EsentOutOfObjectIDsException'
title: EsentOutOfObjectIDsException, classe
TOCTitle: EsentOutOfObjectIDsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfObjectIDsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofobjectidsexception(v=EXCHG.10)
ms:contentKeyID: 55102436
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfObjectIDsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfObjectIDsException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 18cf8d1b7c98db8f855cf970eed7be87185fc9fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520102"
---
# <a name="esentoutofobjectidsexception-class"></a><span data-ttu-id="469ba-103">EsentOutOfObjectIDsException, classe</span><span class="sxs-lookup"><span data-stu-id="469ba-103">EsentOutOfObjectIDsException class</span></span>

<span data-ttu-id="469ba-104">Classe de base pour JET_err. Exceptions OutOfObjectIDs.</span><span class="sxs-lookup"><span data-stu-id="469ba-104">Base class for JET_err.OutOfObjectIDs exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="469ba-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="469ba-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="469ba-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="469ba-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="469ba-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="469ba-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="469ba-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="469ba-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="469ba-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="469ba-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="469ba-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="469ba-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="469ba-111">Microsoft. ISAM. esent. Interop. EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="469ba-111">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>](./esentfragmentationexception-class.md)  
            <span data-ttu-id="469ba-112">Microsoft. ISAM. esent. Interop. EsentOutOfObjectIDsException</span><span class="sxs-lookup"><span data-stu-id="469ba-112">Microsoft.Isam.Esent.Interop.EsentOutOfObjectIDsException</span></span>  

<span data-ttu-id="469ba-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="469ba-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="469ba-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="469ba-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="469ba-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="469ba-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfObjectIDsException _
    Inherits EsentFragmentationException
'Usage
Dim instance As EsentOutOfObjectIDsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfObjectIDsException : EsentFragmentationException
```

## <a name="thread-safety"></a><span data-ttu-id="469ba-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="469ba-116">Thread safety</span></span>

<span data-ttu-id="469ba-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="469ba-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="469ba-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="469ba-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="469ba-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="469ba-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="469ba-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="469ba-120">Reference</span></span>

[<span data-ttu-id="469ba-121">Membres EsentOutOfObjectIDsException</span><span class="sxs-lookup"><span data-stu-id="469ba-121">EsentOutOfObjectIDsException members</span></span>](./esentoutofobjectidsexception-members.md)

[<span data-ttu-id="469ba-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="469ba-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
