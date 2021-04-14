---
description: 'En savoir plus sur : classe EsentDatabaseLeakInSpaceException'
title: EsentDatabaseLeakInSpaceException, classe
TOCTitle: EsentDatabaseLeakInSpaceException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseLeakInSpaceException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaseleakinspaceexception(v=EXCHG.10)
ms:contentKeyID: 55101407
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseLeakInSpaceException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseLeakInSpaceException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 51c011fb1cf3c1dc7ebcade5d88dc2cbce66351b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527094"
---
# <a name="esentdatabaseleakinspaceexception-class"></a><span data-ttu-id="26422-103">EsentDatabaseLeakInSpaceException, classe</span><span class="sxs-lookup"><span data-stu-id="26422-103">EsentDatabaseLeakInSpaceException class</span></span>

<span data-ttu-id="26422-104">Classe de base pour JET_err. Exceptions DatabaseLeakInSpace.</span><span class="sxs-lookup"><span data-stu-id="26422-104">Base class for JET_err.DatabaseLeakInSpace exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="26422-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="26422-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="26422-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="26422-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="26422-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="26422-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="26422-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="26422-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="26422-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="26422-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="26422-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="26422-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="26422-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="26422-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="26422-112">Microsoft. ISAM. esent. Interop. EsentDatabaseLeakInSpaceException</span><span class="sxs-lookup"><span data-stu-id="26422-112">Microsoft.Isam.Esent.Interop.EsentDatabaseLeakInSpaceException</span></span>  

<span data-ttu-id="26422-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="26422-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="26422-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="26422-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="26422-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26422-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseLeakInSpaceException _
    Inherits EsentStateException
'Usage
Dim instance As EsentDatabaseLeakInSpaceException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseLeakInSpaceException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="26422-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="26422-116">Thread safety</span></span>

<span data-ttu-id="26422-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="26422-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="26422-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="26422-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="26422-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26422-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="26422-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="26422-120">Reference</span></span>

[<span data-ttu-id="26422-121">Membres EsentDatabaseLeakInSpaceException</span><span class="sxs-lookup"><span data-stu-id="26422-121">EsentDatabaseLeakInSpaceException members</span></span>](./esentdatabaseleakinspaceexception-members.md)

[<span data-ttu-id="26422-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="26422-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
