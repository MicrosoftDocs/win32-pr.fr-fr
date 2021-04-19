---
description: 'En savoir plus sur : classe EsentRollbackErrorException'
title: EsentRollbackErrorException, classe
TOCTitle: EsentRollbackErrorException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRollbackErrorException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrollbackerrorexception(v=EXCHG.10)
ms:contentKeyID: 55102663
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRollbackErrorException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRollbackErrorException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6e56e3e829b8c44ff6325ed877606fb44471f6a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520465"
---
# <a name="esentrollbackerrorexception-class"></a><span data-ttu-id="9e4de-103">EsentRollbackErrorException, classe</span><span class="sxs-lookup"><span data-stu-id="9e4de-103">EsentRollbackErrorException class</span></span>

<span data-ttu-id="9e4de-104">Classe de base pour JET_err. Exceptions RollbackError.</span><span class="sxs-lookup"><span data-stu-id="9e4de-104">Base class for JET_err.RollbackError exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="9e4de-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="9e4de-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="9e4de-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="9e4de-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="9e4de-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="9e4de-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="9e4de-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="9e4de-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="9e4de-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="9e4de-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="9e4de-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="9e4de-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="9e4de-111">Microsoft. ISAM. esent. Interop. EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="9e4de-111">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>](./esentfatalexception-class.md)  
            <span data-ttu-id="9e4de-112">Microsoft. ISAM. esent. Interop. EsentRollbackErrorException</span><span class="sxs-lookup"><span data-stu-id="9e4de-112">Microsoft.Isam.Esent.Interop.EsentRollbackErrorException</span></span>  

<span data-ttu-id="9e4de-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9e4de-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9e4de-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9e4de-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9e4de-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e4de-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRollbackErrorException _
    Inherits EsentFatalException
'Usage
Dim instance As EsentRollbackErrorException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRollbackErrorException : EsentFatalException
```

## <a name="thread-safety"></a><span data-ttu-id="9e4de-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="9e4de-116">Thread safety</span></span>

<span data-ttu-id="9e4de-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="9e4de-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="9e4de-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="9e4de-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="9e4de-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e4de-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9e4de-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="9e4de-120">Reference</span></span>

[<span data-ttu-id="9e4de-121">Membres EsentRollbackErrorException</span><span class="sxs-lookup"><span data-stu-id="9e4de-121">EsentRollbackErrorException members</span></span>](./esentrollbackerrorexception-members.md)

[<span data-ttu-id="9e4de-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="9e4de-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
