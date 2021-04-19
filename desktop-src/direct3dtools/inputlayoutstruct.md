---
description: Représente les champs de disposition d’entrée d’une mémoire tampon de vertex, un par champ dans la mémoire tampon de vertex.
MS-HAID: vspixengine.InputLayoutStruct
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: InputLayoutStruct, structure
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC7AAC2F-FDB1-4AD8-9B87-A97EE557FEAC
api_name:
- InputLayoutStruct
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1369d80d202682b67eacbb184b215d9da1711874
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106512859"
---
# <a name="span-idvspixengineinputlayoutstructspaninputlayoutstruct-structure"></a><span data-ttu-id="95e7e-103"><span id="vspixengine.inputlayoutstruct"></span>InputLayoutStruct, structure</span><span class="sxs-lookup"><span data-stu-id="95e7e-103"><span id="vspixengine.inputlayoutstruct"></span>InputLayoutStruct structure</span></span>

<span data-ttu-id="95e7e-104">Représente les champs de disposition d’entrée d’une mémoire tampon de vertex, un par champ dans la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="95e7e-104">Represents the input layout fields of a vertex buffer, one per field in the vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="95e7e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95e7e-105">Syntax</span></span>


```C++
} InputLayoutStruct;
```

## <a name="members"></a><span data-ttu-id="95e7e-106">Membres</span><span class="sxs-lookup"><span data-stu-id="95e7e-106">Members</span></span>

<span data-ttu-id="95e7e-107">**SemanticName**</span><span class="sxs-lookup"><span data-stu-id="95e7e-107">**SemanticName**</span></span>  
<span data-ttu-id="95e7e-108">Chaîne COM contenant le nom de la sémantique associée.</span><span class="sxs-lookup"><span data-stu-id="95e7e-108">A COM string containing the name of the associated semantic.</span></span>

<span data-ttu-id="95e7e-109">**SemanticIndex**</span><span class="sxs-lookup"><span data-stu-id="95e7e-109">**SemanticIndex**</span></span>  
<span data-ttu-id="95e7e-110">Index de la sémantique associée.</span><span class="sxs-lookup"><span data-stu-id="95e7e-110">The index of the associated semantic.</span></span>

<span data-ttu-id="95e7e-111">**Format**</span><span class="sxs-lookup"><span data-stu-id="95e7e-111">**Format**</span></span>  
<span data-ttu-id="95e7e-112">Format du champ.</span><span class="sxs-lookup"><span data-stu-id="95e7e-112">The format of the field.</span></span> <span data-ttu-id="95e7e-113">Pour plus d’informations, consultez l' \_ énumération de format DXGI.</span><span class="sxs-lookup"><span data-stu-id="95e7e-113">For more information see the DXGI\_FORMAT enumeration.</span></span>

<span data-ttu-id="95e7e-114">**InputSlot**</span><span class="sxs-lookup"><span data-stu-id="95e7e-114">**InputSlot**</span></span>  
<span data-ttu-id="95e7e-115">Emplacement d’entrée associé.</span><span class="sxs-lookup"><span data-stu-id="95e7e-115">The associated input slot.</span></span>

<span data-ttu-id="95e7e-116">**AlignedByteOffset**</span><span class="sxs-lookup"><span data-stu-id="95e7e-116">**AlignedByteOffset**</span></span>  

<span data-ttu-id="95e7e-117">**InputSlotClass**</span><span class="sxs-lookup"><span data-stu-id="95e7e-117">**InputSlotClass**</span></span>  

<span data-ttu-id="95e7e-118">**InstanceDataStepRate**</span><span class="sxs-lookup"><span data-stu-id="95e7e-118">**InstanceDataStepRate**</span></span>  

## <a name="requirements"></a><span data-ttu-id="95e7e-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95e7e-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="95e7e-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="95e7e-120">Header</span></span></p></td><td><span data-ttu-id="95e7e-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="95e7e-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



