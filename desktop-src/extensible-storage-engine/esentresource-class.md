---
description: 'En savoir plus sur : classe EsentResource'
title: EsentResource, classe
TOCTitle: EsentResource class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentResource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresource(v=EXCHG.10)
ms:contentKeyID: 55102575
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentResource
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentResource
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 607fb59d6f9f89c33e685ed411ae9dc95eaa6818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529676"
---
# <a name="esentresource-class"></a><span data-ttu-id="af24c-103">EsentResource, classe</span><span class="sxs-lookup"><span data-stu-id="af24c-103">EsentResource class</span></span>

<span data-ttu-id="af24c-104">Il s’agit de la classe de base pour tous les objets de ressource esent.</span><span class="sxs-lookup"><span data-stu-id="af24c-104">This is the base class for all esent resource objects.</span></span> <span data-ttu-id="af24c-105">Les sous-classes de cette classe peuvent allouer et libérer des ressources non managées.</span><span class="sxs-lookup"><span data-stu-id="af24c-105">Subclasses of this class can allocate and release unmanaged resources.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="af24c-106">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="af24c-106">Inheritance hierarchy</span></span>

[<span data-ttu-id="af24c-107">System.Object</span><span class="sxs-lookup"><span data-stu-id="af24c-107">System.Object</span></span>](/dotnet/api/system.object)  
  <span data-ttu-id="af24c-108">Microsoft. ISAM. esent. Interop. EsentResource</span><span class="sxs-lookup"><span data-stu-id="af24c-108">Microsoft.Isam.Esent.Interop.EsentResource</span></span>  
    [<span data-ttu-id="af24c-109">Microsoft. ISAM. esent. Interop. session</span><span class="sxs-lookup"><span data-stu-id="af24c-109">Microsoft.Isam.Esent.Interop.Session</span></span>](./session-class.md)  
    [<span data-ttu-id="af24c-110">Microsoft. ISAM. esent. Interop. table</span><span class="sxs-lookup"><span data-stu-id="af24c-110">Microsoft.Isam.Esent.Interop.Table</span></span>](./table-class.md)  
    [<span data-ttu-id="af24c-111">Microsoft. ISAM. esent. Interop. transaction</span><span class="sxs-lookup"><span data-stu-id="af24c-111">Microsoft.Isam.Esent.Interop.Transaction</span></span>](./transaction-class.md)  
    [<span data-ttu-id="af24c-112">Microsoft. ISAM. esent. Interop. Update</span><span class="sxs-lookup"><span data-stu-id="af24c-112">Microsoft.Isam.Esent.Interop.Update</span></span>](./update-class.md)  
    [<span data-ttu-id="af24c-113">Microsoft. ISAM. esent. Interop. Windows8. DurableCommitCallback</span><span class="sxs-lookup"><span data-stu-id="af24c-113">Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback</span></span>](./durablecommitcallback-class.md)  

<span data-ttu-id="af24c-114">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="af24c-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="af24c-115">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="af24c-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="af24c-116">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af24c-116">Syntax</span></span>

``` vb
'Declaration
Public MustInherit Class EsentResource _
    Implements IDisposable
'Usage
Dim instance As EsentResource
```

``` csharp
public abstract class EsentResource : IDisposable
```

## <a name="thread-safety"></a><span data-ttu-id="af24c-117">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="af24c-117">Thread safety</span></span>

<span data-ttu-id="af24c-118">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="af24c-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="af24c-119">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="af24c-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="af24c-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af24c-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="af24c-121">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="af24c-121">Reference</span></span>

[<span data-ttu-id="af24c-122">Membres EsentResource</span><span class="sxs-lookup"><span data-stu-id="af24c-122">EsentResource members</span></span>](./esentresource-members.md)

[<span data-ttu-id="af24c-123">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="af24c-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
