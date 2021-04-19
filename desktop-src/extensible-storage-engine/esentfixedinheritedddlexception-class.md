---
description: 'En savoir plus sur : classe EsentFixedInheritedDDLException'
title: EsentFixedInheritedDDLException, classe
TOCTitle: EsentFixedInheritedDDLException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFixedInheritedDDLException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfixedinheritedddlexception(v=EXCHG.10)
ms:contentKeyID: 55101724
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFixedInheritedDDLException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFixedInheritedDDLException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43f8638b396848503819635860b7472a8af684c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517761"
---
# <a name="esentfixedinheritedddlexception-class"></a><span data-ttu-id="952a7-103">EsentFixedInheritedDDLException, classe</span><span class="sxs-lookup"><span data-stu-id="952a7-103">EsentFixedInheritedDDLException class</span></span>

<span data-ttu-id="952a7-104">Classe de base pour JET_err. Exceptions FixedInheritedDDL.</span><span class="sxs-lookup"><span data-stu-id="952a7-104">Base class for JET_err.FixedInheritedDDL exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="952a7-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="952a7-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="952a7-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="952a7-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="952a7-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="952a7-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="952a7-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="952a7-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="952a7-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="952a7-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="952a7-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="952a7-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="952a7-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="952a7-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="952a7-112">Microsoft. ISAM. esent. Interop. EsentFixedInheritedDDLException</span><span class="sxs-lookup"><span data-stu-id="952a7-112">Microsoft.Isam.Esent.Interop.EsentFixedInheritedDDLException</span></span>  

<span data-ttu-id="952a7-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="952a7-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="952a7-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="952a7-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="952a7-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="952a7-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFixedInheritedDDLException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentFixedInheritedDDLException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFixedInheritedDDLException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="952a7-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="952a7-116">Thread safety</span></span>

<span data-ttu-id="952a7-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="952a7-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="952a7-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="952a7-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="952a7-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="952a7-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="952a7-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="952a7-120">Reference</span></span>

[<span data-ttu-id="952a7-121">Membres EsentFixedInheritedDDLException</span><span class="sxs-lookup"><span data-stu-id="952a7-121">EsentFixedInheritedDDLException members</span></span>](./esentfixedinheritedddlexception-members.md)

[<span data-ttu-id="952a7-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="952a7-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
