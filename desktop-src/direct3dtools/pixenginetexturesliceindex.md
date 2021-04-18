---
description: Représente l’index d’une tranche de texture.
MS-HAID: vspixengine.PixEngineTextureSliceIndex
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PixEngineTextureSliceIndex, structure
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 127765F7-4EBF-4B66-9491-A6FE9DC673C8
api_name:
- PixEngineTextureSliceIndex
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0fd954b5ba9d4dd20f35245350857352bc9b8ae3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515903"
---
# <a name="span-idvspixenginepixenginetexturesliceindexspanpixenginetexturesliceindex-structure"></a><span data-ttu-id="be3ec-103"><span id="vspixengine.pixenginetexturesliceindex"></span>PixEngineTextureSliceIndex, structure</span><span class="sxs-lookup"><span data-stu-id="be3ec-103"><span id="vspixengine.pixenginetexturesliceindex"></span>PixEngineTextureSliceIndex structure</span></span>

<span data-ttu-id="be3ec-104">Représente l’index d’une tranche de texture</span><span class="sxs-lookup"><span data-stu-id="be3ec-104">Represents the index of a texture slice</span></span>

## <a name="syntax"></a><span data-ttu-id="be3ec-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be3ec-105">Syntax</span></span>


```C++
} PixEngineTextureSliceIndex;
```

## <a name="members"></a><span data-ttu-id="be3ec-106">Membres</span><span class="sxs-lookup"><span data-stu-id="be3ec-106">Members</span></span>

<span data-ttu-id="be3ec-107">**arrayIndex**</span><span class="sxs-lookup"><span data-stu-id="be3ec-107">**arrayIndex**</span></span>  
<span data-ttu-id="be3ec-108">Lorsque la texture est un tableau de textures, l’index de tableau de la tranche.</span><span class="sxs-lookup"><span data-stu-id="be3ec-108">When the texture is a texture array, the array index of the slice.</span></span>

<span data-ttu-id="be3ec-109">**mipmapLevel**</span><span class="sxs-lookup"><span data-stu-id="be3ec-109">**mipmapLevel**</span></span>  
<span data-ttu-id="be3ec-110">Niveau de mipmap de la tranche.</span><span class="sxs-lookup"><span data-stu-id="be3ec-110">The mipmap level of the slice.</span></span>

<span data-ttu-id="be3ec-111">**sampleIndex**</span><span class="sxs-lookup"><span data-stu-id="be3ec-111">**sampleIndex**</span></span>  
<span data-ttu-id="be3ec-112">Exemple d’index de la tranche.</span><span class="sxs-lookup"><span data-stu-id="be3ec-112">The sample index of the slice.</span></span>

<span data-ttu-id="be3ec-113">**zSlice**</span><span class="sxs-lookup"><span data-stu-id="be3ec-113">**zSlice**</span></span>  
<span data-ttu-id="be3ec-114">Profondeur (z) de la tranche.</span><span class="sxs-lookup"><span data-stu-id="be3ec-114">The depth (z) of the slice.</span></span>

## <a name="requirements"></a><span data-ttu-id="be3ec-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be3ec-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="be3ec-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="be3ec-116">Header</span></span></p></td><td><span data-ttu-id="be3ec-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="be3ec-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



