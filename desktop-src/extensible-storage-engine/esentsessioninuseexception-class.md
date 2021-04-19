---
description: 'En savoir plus sur : classe EsentSessionInUseException'
title: EsentSessionInUseException, classe
TOCTitle: EsentSessionInUseException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSessionInUseException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsessioninuseexception(v=EXCHG.10)
ms:contentKeyID: 55102709
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSessionInUseException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSessionInUseException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b956d88e1a8c59f23bedc25fadcacd234841572b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538892"
---
# <a name="esentsessioninuseexception-class"></a><span data-ttu-id="a4112-103">EsentSessionInUseException, classe</span><span class="sxs-lookup"><span data-stu-id="a4112-103">EsentSessionInUseException class</span></span>

<span data-ttu-id="a4112-104">Classe de base pour JET_err. Exceptions SessionInUse.</span><span class="sxs-lookup"><span data-stu-id="a4112-104">Base class for JET_err.SessionInUse exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="a4112-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="a4112-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="a4112-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="a4112-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a4112-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="a4112-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="a4112-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="a4112-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="a4112-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="a4112-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="a4112-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="a4112-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="a4112-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="a4112-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="a4112-112">Microsoft. ISAM. esent. Interop. EsentSessionInUseException</span><span class="sxs-lookup"><span data-stu-id="a4112-112">Microsoft.Isam.Esent.Interop.EsentSessionInUseException</span></span>  

<span data-ttu-id="a4112-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a4112-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a4112-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a4112-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a4112-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4112-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSessionInUseException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentSessionInUseException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSessionInUseException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="a4112-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="a4112-116">Thread safety</span></span>

<span data-ttu-id="a4112-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="a4112-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a4112-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="a4112-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a4112-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4112-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a4112-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="a4112-120">Reference</span></span>

[<span data-ttu-id="a4112-121">Membres EsentSessionInUseException</span><span class="sxs-lookup"><span data-stu-id="a4112-121">EsentSessionInUseException members</span></span>](./esentsessioninuseexception-members.md)

[<span data-ttu-id="a4112-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a4112-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
