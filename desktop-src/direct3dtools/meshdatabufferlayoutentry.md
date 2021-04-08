---
description: Représente des informations sur une seule entrée dans la disposition de la mémoire tampon d’un maillage.
MS-HAID: vspixengine.MeshDataBufferLayoutEntry
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MeshDataBufferLayoutEntry, structure
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FE1D796C-DFD8-4C6E-9914-3063408FE565
api_name:
- MeshDataBufferLayoutEntry
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bce67b8316e9eb9b96e641e2a90260fab6bfdaad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747573"
---
# <a name="span-idvspixenginemeshdatabufferlayoutentryspanmeshdatabufferlayoutentry-structure"></a><span data-ttu-id="02577-103"><span id="vspixengine.meshdatabufferlayoutentry"></span>MeshDataBufferLayoutEntry, structure</span><span class="sxs-lookup"><span data-stu-id="02577-103"><span id="vspixengine.meshdatabufferlayoutentry"></span>MeshDataBufferLayoutEntry structure</span></span>

<span data-ttu-id="02577-104">Représente des informations sur une seule entrée dans la disposition de la mémoire tampon d’un maillage.</span><span class="sxs-lookup"><span data-stu-id="02577-104">Represents information about a single entry in the buffer layout of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="02577-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02577-105">Syntax</span></span>


```C++
} MeshDataBufferLayoutEntry;
```

## <a name="members"></a><span data-ttu-id="02577-106">Membres</span><span class="sxs-lookup"><span data-stu-id="02577-106">Members</span></span>

<span data-ttu-id="02577-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="02577-107">**pName**</span></span>  
<span data-ttu-id="02577-108">Chaîne COM contenant le nom de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="02577-108">A COM string containing the name of the entry.</span></span>

<span data-ttu-id="02577-109">**numComponents**</span><span class="sxs-lookup"><span data-stu-id="02577-109">**numComponents**</span></span>  
<span data-ttu-id="02577-110">Nombre de composants homogènes (valeurs) qui composent cette entrée.</span><span class="sxs-lookup"><span data-stu-id="02577-110">The number of homogenous components (values) that make up this entry.</span></span>

<span data-ttu-id="02577-111">**isPosition**</span><span class="sxs-lookup"><span data-stu-id="02577-111">**isPosition**</span></span>  
<span data-ttu-id="02577-112">true si l’entrée est une position ; Sinon, false.</span><span class="sxs-lookup"><span data-stu-id="02577-112">true if the entry is a position; otherwise, false.</span></span>

<span data-ttu-id="02577-113">**format**</span><span class="sxs-lookup"><span data-stu-id="02577-113">**format**</span></span>  
<span data-ttu-id="02577-114">Le format de données de l’entrée (Register).</span><span class="sxs-lookup"><span data-stu-id="02577-114">The data format of the entry (register).</span></span> <span data-ttu-id="02577-115">Pour plus d’informations, consultez l' \_ énumération de format de registre.</span><span class="sxs-lookup"><span data-stu-id="02577-115">For more information, see the REGISTER\_FORMAT enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="02577-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02577-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="02577-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="02577-117">Header</span></span></p></td><td><span data-ttu-id="02577-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="02577-118">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



