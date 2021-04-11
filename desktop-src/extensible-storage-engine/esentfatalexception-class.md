---
description: 'En savoir plus sur : classe EsentFatalException'
title: EsentFatalException, classe
TOCTitle: EsentFatalException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFatalException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfatalexception(v=EXCHG.10)
ms:contentKeyID: 55101653
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFatalException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFatalException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c38df447f2eb816772713ba930204e75aa38a88c
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104211186"
---
# <a name="esentfatalexception-class"></a><span data-ttu-id="c3b0a-103">EsentFatalException, classe</span><span class="sxs-lookup"><span data-stu-id="c3b0a-103">EsentFatalException class</span></span>

<span data-ttu-id="c3b0a-104">Classe de base pour les exceptions irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="c3b0a-104">Base class for Fatal exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="c3b0a-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="c3b0a-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="c3b0a-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="c3b0a-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="c3b0a-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="c3b0a-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="c3b0a-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="c3b0a-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="c3b0a-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="c3b0a-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="c3b0a-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="c3b0a-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="c3b0a-111">Microsoft. ISAM. esent. Interop. EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="c3b0a-111">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>  
            

<span data-ttu-id="c3b0a-112">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c3b0a-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c3b0a-113">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c3b0a-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c3b0a-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3b0a-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentFatalException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentFatalException
```

``` csharp
[SerializableAttribute]
public abstract class EsentFatalException : EsentOperationException
```

## <a name="thread-safety"></a><span data-ttu-id="c3b0a-115">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="c3b0a-115">Thread safety</span></span>

<span data-ttu-id="c3b0a-116">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="c3b0a-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c3b0a-117">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="c3b0a-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c3b0a-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3b0a-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c3b0a-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="c3b0a-119">Reference</span></span>

[<span data-ttu-id="c3b0a-120">Membres EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="c3b0a-120">EsentFatalException members</span></span>](./esentfatalexception-members.md)

[<span data-ttu-id="c3b0a-121">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c3b0a-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="c3b0a-122">Types dérivés</span><span class="sxs-lookup"><span data-stu-id="c3b0a-122">Derived types</span></span>

[<span data-ttu-id="c3b0a-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="c3b0a-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="c3b0a-124">System.Exception</span><span class="sxs-lookup"><span data-stu-id="c3b0a-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="c3b0a-125">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="c3b0a-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="c3b0a-126">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="c3b0a-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="c3b0a-127">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="c3b0a-127">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="c3b0a-128">Microsoft. ISAM. esent. Interop. EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="c3b0a-128">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>  
            [<span data-ttu-id="c3b0a-129">Microsoft. ISAM. esent. Interop. EsentInstanceUnavailableDueToFatalLogDiskFullException</span><span class="sxs-lookup"><span data-stu-id="c3b0a-129">Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableDueToFatalLogDiskFullException</span></span>](./esentinstanceunavailableduetofatallogdiskfullexception-class.md)  
            [<span data-ttu-id="c3b0a-130">Microsoft. ISAM. esent. Interop. EsentInstanceUnavailableException</span><span class="sxs-lookup"><span data-stu-id="c3b0a-130">Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableException</span></span>](./esentinstanceunavailableexception-class.md)  
            [<span data-ttu-id="c3b0a-131">Microsoft. ISAM. esent. Interop. EsentLogDisabledDueToRecoveryFailureException</span><span class="sxs-lookup"><span data-stu-id="c3b0a-131">Microsoft.Isam.Esent.Interop.EsentLogDisabledDueToRecoveryFailureException</span></span>](./esentlogdisabledduetorecoveryfailureexception-class.md)  
            [<span data-ttu-id="c3b0a-132">Microsoft. ISAM. esent. Interop. EsentRollbackErrorException</span><span class="sxs-lookup"><span data-stu-id="c3b0a-132">Microsoft.Isam.Esent.Interop.EsentRollbackErrorException</span></span>](./esentrollbackerrorexception-class.md)  
            [<span data-ttu-id="c3b0a-133">Microsoft. ISAM. esent. Interop. EsentSectorSizeNotSupportedException</span><span class="sxs-lookup"><span data-stu-id="c3b0a-133">Microsoft.Isam.Esent.Interop.EsentSectorSizeNotSupportedException</span></span>](./esentsectorsizenotsupportedexception-class.md)  
            [<span data-ttu-id="c3b0a-134">Microsoft. ISAM. esent. Interop. EsentUnloadableOSFunctionalityException</span><span class="sxs-lookup"><span data-stu-id="c3b0a-134">Microsoft.Isam.Esent.Interop.EsentUnloadableOSFunctionalityException</span></span>](./esentunloadableosfunctionalityexception-class.md)