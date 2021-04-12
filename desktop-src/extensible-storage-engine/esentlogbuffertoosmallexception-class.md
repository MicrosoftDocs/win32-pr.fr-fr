---
description: 'En savoir plus sur : classe EsentLogBufferTooSmallException'
title: EsentLogBufferTooSmallException, classe
TOCTitle: EsentLogBufferTooSmallException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogBufferTooSmallException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogbuffertoosmallexception(v=EXCHG.10)
ms:contentKeyID: 55102132
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogBufferTooSmallException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogBufferTooSmallException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4b8313ddbe5961d270a7342a7240b5f5bc02e946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320770"
---
# <a name="esentlogbuffertoosmallexception-class"></a><span data-ttu-id="4fb5c-103">EsentLogBufferTooSmallException, classe</span><span class="sxs-lookup"><span data-stu-id="4fb5c-103">EsentLogBufferTooSmallException class</span></span>

<span data-ttu-id="4fb5c-104">Classe de base pour JET_err. Exceptions LogBufferTooSmall.</span><span class="sxs-lookup"><span data-stu-id="4fb5c-104">Base class for JET_err.LogBufferTooSmall exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="4fb5c-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="4fb5c-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="4fb5c-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="4fb5c-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="4fb5c-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="4fb5c-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="4fb5c-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="4fb5c-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="4fb5c-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="4fb5c-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="4fb5c-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="4fb5c-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="4fb5c-111">Microsoft. ISAM. esent. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="4fb5c-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="4fb5c-112">Microsoft. ISAM. esent. Interop. EsentLogBufferTooSmallException</span><span class="sxs-lookup"><span data-stu-id="4fb5c-112">Microsoft.Isam.Esent.Interop.EsentLogBufferTooSmallException</span></span>  

<span data-ttu-id="4fb5c-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4fb5c-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4fb5c-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4fb5c-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4fb5c-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4fb5c-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogBufferTooSmallException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentLogBufferTooSmallException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogBufferTooSmallException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="4fb5c-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="4fb5c-116">Thread safety</span></span>

<span data-ttu-id="4fb5c-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="4fb5c-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="4fb5c-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="4fb5c-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="4fb5c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fb5c-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4fb5c-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="4fb5c-120">Reference</span></span>

[<span data-ttu-id="4fb5c-121">Membres EsentLogBufferTooSmallException</span><span class="sxs-lookup"><span data-stu-id="4fb5c-121">EsentLogBufferTooSmallException members</span></span>](./esentlogbuffertoosmallexception-members.md)

[<span data-ttu-id="4fb5c-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4fb5c-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
