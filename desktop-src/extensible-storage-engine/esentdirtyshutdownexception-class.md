---
description: 'En savoir plus sur : classe EsentDirtyShutdownException'
title: EsentDirtyShutdownException, classe
TOCTitle: EsentDirtyShutdownException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDirtyShutdownException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdirtyshutdownexception(v=EXCHG.10)
ms:contentKeyID: 55101504
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDirtyShutdownException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDirtyShutdownException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72eb3984c034cbbb9c6163e183a5b8680fc49845
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524706"
---
# <a name="esentdirtyshutdownexception-class"></a><span data-ttu-id="16a47-103">EsentDirtyShutdownException, classe</span><span class="sxs-lookup"><span data-stu-id="16a47-103">EsentDirtyShutdownException class</span></span>

<span data-ttu-id="16a47-104">Classe de base pour JET_err. Exceptions DirtyShutdown.</span><span class="sxs-lookup"><span data-stu-id="16a47-104">Base class for JET_err.DirtyShutdown exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="16a47-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="16a47-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="16a47-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="16a47-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="16a47-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="16a47-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="16a47-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="16a47-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="16a47-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="16a47-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="16a47-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="16a47-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="16a47-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="16a47-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="16a47-112">Microsoft. ISAM. esent. Interop. EsentDirtyShutdownException</span><span class="sxs-lookup"><span data-stu-id="16a47-112">Microsoft.Isam.Esent.Interop.EsentDirtyShutdownException</span></span>  

<span data-ttu-id="16a47-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="16a47-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="16a47-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="16a47-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="16a47-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16a47-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDirtyShutdownException _
    Inherits EsentStateException
'Usage
Dim instance As EsentDirtyShutdownException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDirtyShutdownException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="16a47-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="16a47-116">Thread safety</span></span>

<span data-ttu-id="16a47-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="16a47-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="16a47-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="16a47-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="16a47-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16a47-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="16a47-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="16a47-120">Reference</span></span>

[<span data-ttu-id="16a47-121">Membres EsentDirtyShutdownException</span><span class="sxs-lookup"><span data-stu-id="16a47-121">EsentDirtyShutdownException members</span></span>](./esentdirtyshutdownexception-members.md)

[<span data-ttu-id="16a47-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="16a47-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
