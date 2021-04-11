---
description: 'En savoir plus sur : JET_PFNREALLOC délégué'
title: Délégué JET_PFNREALLOC
TOCTitle: JET_PFNREALLOC delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_pfnrealloc(v=EXCHG.10)
ms:contentKeyID: 39515764
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC..ctor
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.BeginInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.Invoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7aab9fef2d7a449c877f88d2ed77aa19cbb2409d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953113"
---
# <a name="jet_pfnrealloc-delegate"></a><span data-ttu-id="afe62-103">Délégué JET_PFNREALLOC</span><span class="sxs-lookup"><span data-stu-id="afe62-103">JET_PFNREALLOC delegate</span></span>

<span data-ttu-id="afe62-104">Rappel utilisé par JetEnumerateColumns pour allouer de la mémoire pour ses mémoires tampons de sortie.</span><span class="sxs-lookup"><span data-stu-id="afe62-104">Callback used by JetEnumerateColumns to allocate memory for its output buffers.</span></span>

<span data-ttu-id="afe62-105">Cette API n’est pas conforme CLS.</span><span class="sxs-lookup"><span data-stu-id="afe62-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="afe62-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="afe62-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="afe62-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="afe62-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="afe62-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="afe62-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Delegate Function JET_PFNREALLOC ( _
    context As IntPtr, _
    memory As IntPtr, _
    requestedSize As UInteger _
) As IntPtr
'Usage
Dim instance As New JET_PFNREALLOC(AddressOf HandlerMethod)
```

``` csharp
[CLSCompliantAttribute(false)]
public delegate IntPtr JET_PFNREALLOC(
    IntPtr context,
    IntPtr memory,
    uint requestedSize
)
```

#### <a name="parameters"></a><span data-ttu-id="afe62-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="afe62-109">Parameters</span></span>

  - <span data-ttu-id="afe62-110">contexte</span><span class="sxs-lookup"><span data-stu-id="afe62-110">context</span></span>  
    <span data-ttu-id="afe62-111">Type : [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="afe62-111">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="afe62-112">Contexte donné à JetEnumerateColumns.</span><span class="sxs-lookup"><span data-stu-id="afe62-112">Context given to JetEnumerateColumns.</span></span>

<!-- end list -->

  - <span data-ttu-id="afe62-113">mémoire</span><span class="sxs-lookup"><span data-stu-id="afe62-113">memory</span></span>  
    <span data-ttu-id="afe62-114">Type : [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="afe62-114">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="afe62-115">Si la valeur est différente de zéro, pointeur vers un bloc de mémoire précédemment alloué par ce rappel.</span><span class="sxs-lookup"><span data-stu-id="afe62-115">If non-zero, a pointer to a memory block previously allocated by this callback.</span></span>

<!-- end list -->

  - <span data-ttu-id="afe62-116">requestedSize</span><span class="sxs-lookup"><span data-stu-id="afe62-116">requestedSize</span></span>  
    <span data-ttu-id="afe62-117">Type : [System. UInt32](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="afe62-117">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
    
    <span data-ttu-id="afe62-118">Nouvelle taille du bloc de mémoire (en octets).</span><span class="sxs-lookup"><span data-stu-id="afe62-118">The new size of the memory block (in bytes).</span></span> <span data-ttu-id="afe62-119">Si la valeur est égale à 0 et qu’un bloc de mémoire est spécifié, ce bloc de mémoire est libéré.</span><span class="sxs-lookup"><span data-stu-id="afe62-119">If this is 0 and a memory block is specified, that memory block will be freed.</span></span>

#### <a name="return-value"></a><span data-ttu-id="afe62-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="afe62-120">Return value</span></span>

<span data-ttu-id="afe62-121">Type : [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="afe62-121">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
<span data-ttu-id="afe62-122">Pointeur vers la mémoire nouvellement allouée.</span><span class="sxs-lookup"><span data-stu-id="afe62-122">A pointer to newly allocated memory.</span></span> <span data-ttu-id="afe62-123">Si la mémoire n’a pas pu être allouée, la [valeur zéro](/dotnet/api/system.intptr.zero) doit être retournée.</span><span class="sxs-lookup"><span data-stu-id="afe62-123">If memory could not be allocated then [Zero](/dotnet/api/system.intptr.zero) should be returned.</span></span>  

## <a name="see-also"></a><span data-ttu-id="afe62-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="afe62-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="afe62-125">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="afe62-125">Reference</span></span>

[<span data-ttu-id="afe62-126">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="afe62-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
