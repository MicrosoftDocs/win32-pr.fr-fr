---
description: 'En savoir plus sur : classe EsentFileInvalidTypeException'
title: EsentFileInvalidTypeException, classe
TOCTitle: EsentFileInvalidTypeException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfileinvalidtypeexception(v=EXCHG.10)
ms:contentKeyID: 55107272
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d2c2bf5cf30cb45734613fcabc446834085d5bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320641"
---
# <a name="esentfileinvalidtypeexception-class"></a><span data-ttu-id="f0629-103">EsentFileInvalidTypeException, classe</span><span class="sxs-lookup"><span data-stu-id="f0629-103">EsentFileInvalidTypeException class</span></span>

<span data-ttu-id="f0629-104">Classe de base pour JET_err. Exceptions FileInvalidType.</span><span class="sxs-lookup"><span data-stu-id="f0629-104">Base class for JET_err.FileInvalidType exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f0629-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="f0629-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="f0629-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="f0629-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f0629-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="f0629-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="f0629-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="f0629-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="f0629-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="f0629-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="f0629-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="f0629-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="f0629-111">Microsoft. ISAM. esent. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="f0629-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="f0629-112">Microsoft. ISAM. esent. Interop. EsentFileInvalidTypeException</span><span class="sxs-lookup"><span data-stu-id="f0629-112">Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException</span></span>  

<span data-ttu-id="f0629-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f0629-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f0629-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f0629-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f0629-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0629-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFileInvalidTypeException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentFileInvalidTypeException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFileInvalidTypeException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="f0629-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="f0629-116">Thread safety</span></span>

<span data-ttu-id="f0629-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="f0629-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f0629-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="f0629-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f0629-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0629-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f0629-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="f0629-120">Reference</span></span>

[<span data-ttu-id="f0629-121">Membres EsentFileInvalidTypeException</span><span class="sxs-lookup"><span data-stu-id="f0629-121">EsentFileInvalidTypeException members</span></span>](./esentfileinvalidtypeexception-members.md)

[<span data-ttu-id="f0629-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f0629-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
