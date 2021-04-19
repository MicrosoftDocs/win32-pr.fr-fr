---
description: 'En savoir plus sur : classe EsentBadLogSignatureException'
title: EsentBadLogSignatureException, classe
TOCTitle: EsentBadLogSignatureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBadLogSignatureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbadlogsignatureexception(v=EXCHG.10)
ms:contentKeyID: 55101128
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBadLogSignatureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBadLogSignatureException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a77f5ae2b8c7148e80f2ea3163837dc9028e5510
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520734"
---
# <a name="esentbadlogsignatureexception-class"></a><span data-ttu-id="01b2b-103">EsentBadLogSignatureException, classe</span><span class="sxs-lookup"><span data-stu-id="01b2b-103">EsentBadLogSignatureException class</span></span>

<span data-ttu-id="01b2b-104">Classe de base pour JET_err. Exceptions BadLogSignature.</span><span class="sxs-lookup"><span data-stu-id="01b2b-104">Base class for JET_err.BadLogSignature exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="01b2b-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="01b2b-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="01b2b-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="01b2b-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="01b2b-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="01b2b-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="01b2b-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="01b2b-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="01b2b-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="01b2b-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="01b2b-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="01b2b-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="01b2b-111">Microsoft. ISAM. esent. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="01b2b-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="01b2b-112">Microsoft. ISAM. esent. Interop. EsentBadLogSignatureException</span><span class="sxs-lookup"><span data-stu-id="01b2b-112">Microsoft.Isam.Esent.Interop.EsentBadLogSignatureException</span></span>  

<span data-ttu-id="01b2b-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="01b2b-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="01b2b-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="01b2b-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="01b2b-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01b2b-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBadLogSignatureException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentBadLogSignatureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBadLogSignatureException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="01b2b-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="01b2b-116">Thread safety</span></span>

<span data-ttu-id="01b2b-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="01b2b-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="01b2b-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="01b2b-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="01b2b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01b2b-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="01b2b-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="01b2b-120">Reference</span></span>

[<span data-ttu-id="01b2b-121">Membres EsentBadLogSignatureException</span><span class="sxs-lookup"><span data-stu-id="01b2b-121">EsentBadLogSignatureException members</span></span>](./esentbadlogsignatureexception-members.md)

[<span data-ttu-id="01b2b-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="01b2b-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
