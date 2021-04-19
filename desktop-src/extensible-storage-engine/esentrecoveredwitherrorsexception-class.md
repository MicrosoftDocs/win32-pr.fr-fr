---
description: 'En savoir plus sur : classe EsentRecoveredWithErrorsException'
title: EsentRecoveredWithErrorsException, classe
TOCTitle: EsentRecoveredWithErrorsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecoveredWithErrorsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecoveredwitherrorsexception(v=EXCHG.10)
ms:contentKeyID: 55102545
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecoveredWithErrorsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecoveredWithErrorsException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fd90328b3b592232e1f87f4fe568022443be8b77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531672"
---
# <a name="esentrecoveredwitherrorsexception-class"></a><span data-ttu-id="f488a-103">EsentRecoveredWithErrorsException, classe</span><span class="sxs-lookup"><span data-stu-id="f488a-103">EsentRecoveredWithErrorsException class</span></span>

<span data-ttu-id="f488a-104">Classe de base pour JET_err. Exceptions RecoveredWithErrors.</span><span class="sxs-lookup"><span data-stu-id="f488a-104">Base class for JET_err.RecoveredWithErrors exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f488a-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="f488a-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="f488a-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="f488a-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f488a-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="f488a-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="f488a-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="f488a-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="f488a-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="f488a-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="f488a-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="f488a-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="f488a-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="f488a-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="f488a-112">Microsoft. ISAM. esent. Interop. EsentRecoveredWithErrorsException</span><span class="sxs-lookup"><span data-stu-id="f488a-112">Microsoft.Isam.Esent.Interop.EsentRecoveredWithErrorsException</span></span>  

<span data-ttu-id="f488a-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f488a-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f488a-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f488a-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f488a-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f488a-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecoveredWithErrorsException _
    Inherits EsentStateException
'Usage
Dim instance As EsentRecoveredWithErrorsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecoveredWithErrorsException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="f488a-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="f488a-116">Thread safety</span></span>

<span data-ttu-id="f488a-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="f488a-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f488a-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="f488a-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f488a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f488a-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f488a-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="f488a-120">Reference</span></span>

[<span data-ttu-id="f488a-121">Membres EsentRecoveredWithErrorsException</span><span class="sxs-lookup"><span data-stu-id="f488a-121">EsentRecoveredWithErrorsException members</span></span>](./esentrecoveredwitherrorsexception-members.md)

[<span data-ttu-id="f488a-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f488a-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
