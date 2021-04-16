---
description: 'En savoir plus sur : classe EsentLogSequenceEndException'
title: EsentLogSequenceEndException, classe
TOCTitle: EsentLogSequenceEndException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogSequenceEndException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogsequenceendexception(v=EXCHG.10)
ms:contentKeyID: 55102213
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogSequenceEndException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogSequenceEndException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 78de803d31d8e97f9493d605d688916501edba6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202093"
---
# <a name="esentlogsequenceendexception-class"></a><span data-ttu-id="1ebbd-103">EsentLogSequenceEndException, classe</span><span class="sxs-lookup"><span data-stu-id="1ebbd-103">EsentLogSequenceEndException class</span></span>

<span data-ttu-id="1ebbd-104">Classe de base pour JET_err. Exceptions LogSequenceEnd.</span><span class="sxs-lookup"><span data-stu-id="1ebbd-104">Base class for JET_err.LogSequenceEnd exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="1ebbd-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="1ebbd-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="1ebbd-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="1ebbd-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="1ebbd-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="1ebbd-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="1ebbd-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="1ebbd-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="1ebbd-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="1ebbd-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="1ebbd-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="1ebbd-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="1ebbd-111">Microsoft. ISAM. esent. Interop. EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="1ebbd-111">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>](./esentfragmentationexception-class.md)  
            <span data-ttu-id="1ebbd-112">Microsoft. ISAM. esent. Interop. EsentLogSequenceEndException</span><span class="sxs-lookup"><span data-stu-id="1ebbd-112">Microsoft.Isam.Esent.Interop.EsentLogSequenceEndException</span></span>  

<span data-ttu-id="1ebbd-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1ebbd-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1ebbd-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1ebbd-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1ebbd-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ebbd-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogSequenceEndException _
    Inherits EsentFragmentationException
'Usage
Dim instance As EsentLogSequenceEndException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogSequenceEndException : EsentFragmentationException
```

## <a name="thread-safety"></a><span data-ttu-id="1ebbd-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="1ebbd-116">Thread safety</span></span>

<span data-ttu-id="1ebbd-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="1ebbd-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="1ebbd-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="1ebbd-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="1ebbd-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ebbd-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1ebbd-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="1ebbd-120">Reference</span></span>

[<span data-ttu-id="1ebbd-121">Membres EsentLogSequenceEndException</span><span class="sxs-lookup"><span data-stu-id="1ebbd-121">EsentLogSequenceEndException members</span></span>](./esentlogsequenceendexception-members.md)

[<span data-ttu-id="1ebbd-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1ebbd-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
