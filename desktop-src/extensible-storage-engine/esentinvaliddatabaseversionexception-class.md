---
description: 'En savoir plus sur : classe EsentInvalidDatabaseVersionException'
title: EsentInvalidDatabaseVersionException, classe
TOCTitle: EsentInvalidDatabaseVersionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidDatabaseVersionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvaliddatabaseversionexception(v=EXCHG.10)
ms:contentKeyID: 55101922
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidDatabaseVersionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidDatabaseVersionException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 24b3e348c0c0adaf4d261705c1e4de7bf5d7297b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104211031"
---
# <a name="esentinvaliddatabaseversionexception-class"></a><span data-ttu-id="7da52-103">EsentInvalidDatabaseVersionException, classe</span><span class="sxs-lookup"><span data-stu-id="7da52-103">EsentInvalidDatabaseVersionException class</span></span>

<span data-ttu-id="7da52-104">Classe de base pour JET_err. Exceptions InvalidDatabaseVersion.</span><span class="sxs-lookup"><span data-stu-id="7da52-104">Base class for JET_err.InvalidDatabaseVersion exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="7da52-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="7da52-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="7da52-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="7da52-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="7da52-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="7da52-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="7da52-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="7da52-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="7da52-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="7da52-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="7da52-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="7da52-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="7da52-111">Microsoft. ISAM. esent. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="7da52-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="7da52-112">Microsoft. ISAM. esent. Interop. EsentInvalidDatabaseVersionException</span><span class="sxs-lookup"><span data-stu-id="7da52-112">Microsoft.Isam.Esent.Interop.EsentInvalidDatabaseVersionException</span></span>  

<span data-ttu-id="7da52-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7da52-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7da52-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7da52-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7da52-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7da52-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidDatabaseVersionException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentInvalidDatabaseVersionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidDatabaseVersionException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="7da52-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="7da52-116">Thread safety</span></span>

<span data-ttu-id="7da52-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="7da52-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="7da52-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="7da52-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="7da52-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7da52-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7da52-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="7da52-120">Reference</span></span>

[<span data-ttu-id="7da52-121">Membres EsentInvalidDatabaseVersionException</span><span class="sxs-lookup"><span data-stu-id="7da52-121">EsentInvalidDatabaseVersionException members</span></span>](./esentinvaliddatabaseversionexception-members.md)

[<span data-ttu-id="7da52-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7da52-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
