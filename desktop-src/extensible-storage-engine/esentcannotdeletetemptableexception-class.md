---
description: 'En savoir plus sur : classe EsentCannotDeleteTempTableException'
title: EsentCannotDeleteTempTableException, classe
TOCTitle: EsentCannotDeleteTempTableException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCannotDeleteTempTableException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcannotdeletetemptableexception(v=EXCHG.10)
ms:contentKeyID: 55101145
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCannotDeleteTempTableException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCannotDeleteTempTableException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f333798a6b151b63cbd40c69fab438ecdff68ed9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545849"
---
# <a name="esentcannotdeletetemptableexception-class"></a><span data-ttu-id="b5e5c-103">EsentCannotDeleteTempTableException, classe</span><span class="sxs-lookup"><span data-stu-id="b5e5c-103">EsentCannotDeleteTempTableException class</span></span>

<span data-ttu-id="b5e5c-104">Classe de base pour JET_err. Exceptions CannotDeleteTempTable.</span><span class="sxs-lookup"><span data-stu-id="b5e5c-104">Base class for JET_err.CannotDeleteTempTable exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b5e5c-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="b5e5c-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b5e5c-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b5e5c-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b5e5c-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="b5e5c-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b5e5c-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="b5e5c-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b5e5c-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="b5e5c-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="b5e5c-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="b5e5c-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="b5e5c-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="b5e5c-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="b5e5c-112">Microsoft. ISAM. esent. Interop. EsentCannotDeleteTempTableException</span><span class="sxs-lookup"><span data-stu-id="b5e5c-112">Microsoft.Isam.Esent.Interop.EsentCannotDeleteTempTableException</span></span>  

<span data-ttu-id="b5e5c-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b5e5c-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b5e5c-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b5e5c-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b5e5c-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5e5c-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCannotDeleteTempTableException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentCannotDeleteTempTableException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCannotDeleteTempTableException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="b5e5c-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="b5e5c-116">Thread safety</span></span>

<span data-ttu-id="b5e5c-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="b5e5c-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b5e5c-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="b5e5c-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b5e5c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5e5c-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b5e5c-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="b5e5c-120">Reference</span></span>

[<span data-ttu-id="b5e5c-121">Membres EsentCannotDeleteTempTableException</span><span class="sxs-lookup"><span data-stu-id="b5e5c-121">EsentCannotDeleteTempTableException members</span></span>](./esentcannotdeletetemptableexception-members.md)

[<span data-ttu-id="b5e5c-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b5e5c-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
