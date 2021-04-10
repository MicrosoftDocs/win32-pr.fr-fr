---
description: Représente un package de quatre appels.
MS-HAID: vspixengine.PackedCallPkg
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PackedCallPkg, structure
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BE345C1A-9F6E-4FE0-99C7-6B332A1ED079
api_name:
- PackedCallPkg
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 104e764725213f7030c90a0240641c7c9b063785
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103950124"
---
# <a name="span-idvspixenginepackedcallpkgspanpackedcallpkg-structure"></a><span data-ttu-id="081b3-103"><span id="vspixengine.packedcallpkg"></span>PackedCallPkg, structure</span><span class="sxs-lookup"><span data-stu-id="081b3-103"><span id="vspixengine.packedcallpkg"></span>PackedCallPkg structure</span></span>

<span data-ttu-id="081b3-104">Représente un package de quatre appels.</span><span class="sxs-lookup"><span data-stu-id="081b3-104">Represents a package of four calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="081b3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="081b3-105">Syntax</span></span>


```C++
typedef struct PackedCallPkg {
  UINT pcp1;
  UINT pcp2;
  UINT pcp3;
  UINT pcp4;
} PackedCallPkg;
```

## <a name="members"></a><span data-ttu-id="081b3-106">Membres</span><span class="sxs-lookup"><span data-stu-id="081b3-106">Members</span></span>

<span data-ttu-id="081b3-107">**pcp1**</span><span class="sxs-lookup"><span data-stu-id="081b3-107">**pcp1**</span></span>  
<span data-ttu-id="081b3-108">Premier appel dans le package.</span><span class="sxs-lookup"><span data-stu-id="081b3-108">The first call in the package.</span></span>

<span data-ttu-id="081b3-109">**pcp2**</span><span class="sxs-lookup"><span data-stu-id="081b3-109">**pcp2**</span></span>  
<span data-ttu-id="081b3-110">Deuxième appel dans le package.</span><span class="sxs-lookup"><span data-stu-id="081b3-110">The second call in the package.</span></span>

<span data-ttu-id="081b3-111">**pcp3**</span><span class="sxs-lookup"><span data-stu-id="081b3-111">**pcp3**</span></span>  
<span data-ttu-id="081b3-112">Troisième appel du package.</span><span class="sxs-lookup"><span data-stu-id="081b3-112">The third call in the package.</span></span>

<span data-ttu-id="081b3-113">**pcp4**</span><span class="sxs-lookup"><span data-stu-id="081b3-113">**pcp4**</span></span>  
<span data-ttu-id="081b3-114">Quatrième appel du package.</span><span class="sxs-lookup"><span data-stu-id="081b3-114">The fourth call in the package.</span></span>

## <a name="requirements"></a><span data-ttu-id="081b3-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="081b3-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="081b3-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="081b3-116">Header</span></span></p></td><td><span data-ttu-id="081b3-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="081b3-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



