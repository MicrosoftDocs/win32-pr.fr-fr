---
description: 'En savoir plus sur : classe d’instance'
title: Classe d’instance
TOCTitle: Instance class
ms:assetid: T:Microsoft.Isam.Esent.Interop.Instance
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance(v=EXCHG.10)
ms:contentKeyID: 55103260
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Instance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Instance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7b717286a9d07b7eb17b87354cbe0896cf182f5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753316"
---
# <a name="instance-class"></a><span data-ttu-id="f6331-103">Classe d’instance</span><span class="sxs-lookup"><span data-stu-id="f6331-103">Instance class</span></span>

<span data-ttu-id="f6331-104">Classe qui encapsule un [JET_INSTANCE](./jet-instance-structure.md) dans un objet jetable.</span><span class="sxs-lookup"><span data-stu-id="f6331-104">A class that encapsulates a [JET_INSTANCE](./jet-instance-structure.md) in a disposable object.</span></span> <span data-ttu-id="f6331-105">L’instance doit être fermée en dernier et la fermeture de l’instance libère toutes les autres ressources pour l’instance.</span><span class="sxs-lookup"><span data-stu-id="f6331-105">The instance must be closed last and closing the instance releases all other resources for the instance.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f6331-106">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="f6331-106">Inheritance hierarchy</span></span>

[<span data-ttu-id="f6331-107">System.Object</span><span class="sxs-lookup"><span data-stu-id="f6331-107">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f6331-108">System. Runtime. ConstrainedExecution. CriticalFinalizerObject</span><span class="sxs-lookup"><span data-stu-id="f6331-108">System.Runtime.ConstrainedExecution.CriticalFinalizerObject</span></span>](/dotnet/api/system.runtime.constrainedexecution.criticalfinalizerobject)  
    [<span data-ttu-id="f6331-109">System.Runtime.InteropServices.SafeHandle</span><span class="sxs-lookup"><span data-stu-id="f6331-109">System.Runtime.InteropServices.SafeHandle</span></span>](/dotnet/api/system.runtime.interopservices.safehandle)  
      [<span data-ttu-id="f6331-110">Microsoft. Win32. SafeHandles. SafeHandleZeroOrMinusOneIsInvalid</span><span class="sxs-lookup"><span data-stu-id="f6331-110">Microsoft.Win32.SafeHandles.SafeHandleZeroOrMinusOneIsInvalid</span></span>](/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid)  
        <span data-ttu-id="f6331-111">Microsoft. ISAM. esent. Interop. instance</span><span class="sxs-lookup"><span data-stu-id="f6331-111">Microsoft.Isam.Esent.Interop.Instance</span></span>  

<span data-ttu-id="f6331-112">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f6331-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f6331-113">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f6331-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f6331-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6331-114">Syntax</span></span>

``` vb
'Declaration
Public Class Instance _
    Inherits SafeHandleZeroOrMinusOneIsInvalid
'Usage
Dim instance As Instance
```

``` csharp
public class Instance : SafeHandleZeroOrMinusOneIsInvalid
```

## <a name="thread-safety"></a><span data-ttu-id="f6331-115">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="f6331-115">Thread safety</span></span>

<span data-ttu-id="f6331-116">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="f6331-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f6331-117">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="f6331-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f6331-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6331-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f6331-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="f6331-119">Reference</span></span>

[<span data-ttu-id="f6331-120">Membres d’instance</span><span class="sxs-lookup"><span data-stu-id="f6331-120">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="f6331-121">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f6331-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
