---
description: 'En savoir plus sur : classe EsentErrorException'
title: Classe EsentErrorException
TOCTitle: EsentErrorException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentErrorException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenterrorexception(v=EXCHG.10)
ms:contentKeyID: 55101648
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentErrorException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentErrorException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eb05197392c1d5c8798968254b24d2d0ae677bbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034724"
---
# <a name="esenterrorexception-class"></a><span data-ttu-id="f17b2-103">Classe EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="f17b2-103">EsentErrorException class</span></span>

<span data-ttu-id="f17b2-104">Classe de base pour les exceptions d’erreur ESENT.</span><span class="sxs-lookup"><span data-stu-id="f17b2-104">Base class for ESENT error exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f17b2-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="f17b2-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="f17b2-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="f17b2-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f17b2-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="f17b2-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="f17b2-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="f17b2-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      <span data-ttu-id="f17b2-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="f17b2-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>  
        [<span data-ttu-id="f17b2-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="f17b2-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
        [<span data-ttu-id="f17b2-111">Microsoft. ISAM. esent. Interop. EsentCannotLogDuringRecoveryRedoException</span><span class="sxs-lookup"><span data-stu-id="f17b2-111">Microsoft.Isam.Esent.Interop.EsentCannotLogDuringRecoveryRedoException</span></span>](./esentcannotlogduringrecoveryredoexception-class.md)  
        [<span data-ttu-id="f17b2-112">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="f17b2-112">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
        [<span data-ttu-id="f17b2-113">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="f17b2-113">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
        [<span data-ttu-id="f17b2-114">Microsoft. ISAM. esent. Interop. EsentPreviousVersionException</span><span class="sxs-lookup"><span data-stu-id="f17b2-114">Microsoft.Isam.Esent.Interop.EsentPreviousVersionException</span></span>](./esentpreviousversionexception-class.md)  
        [<span data-ttu-id="f17b2-115">Microsoft. ISAM. esent. Interop. EsentVersionStoreEntryTooBigException</span><span class="sxs-lookup"><span data-stu-id="f17b2-115">Microsoft.Isam.Esent.Interop.EsentVersionStoreEntryTooBigException</span></span>](./esentversionstoreentrytoobigexception-class.md)  

<span data-ttu-id="f17b2-116">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f17b2-116">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f17b2-117">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f17b2-117">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f17b2-118">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f17b2-118">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public Class EsentErrorException _
    Inherits EsentException
'Usage
Dim instance As EsentErrorException
```

``` csharp
[SerializableAttribute]
public class EsentErrorException : EsentException
```

## <a name="thread-safety"></a><span data-ttu-id="f17b2-119">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="f17b2-119">Thread safety</span></span>

<span data-ttu-id="f17b2-120">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="f17b2-120">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f17b2-121">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="f17b2-121">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f17b2-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f17b2-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f17b2-123">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="f17b2-123">Reference</span></span>

[<span data-ttu-id="f17b2-124">Membres EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="f17b2-124">EsentErrorException members</span></span>](./esenterrorexception-members.md)

[<span data-ttu-id="f17b2-125">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f17b2-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
