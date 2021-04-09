---
description: Représente une description d’une tranche de texture.
MS-HAID: vspixengine.PixEngineTextureSliceDescriptor
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PixEngineTextureSliceDescriptor, structure
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1A183AFB-0BEF-4474-A60C-DBCFA4B34604
api_name:
- PixEngineTextureSliceDescriptor
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5b80a23a5ec3340b775c314f66651926743249ad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108822"
---
# <a name="span-idvspixenginepixenginetextureslicedescriptorspanpixenginetextureslicedescriptor-structure"></a><span data-ttu-id="31a85-103"><span id="vspixengine.pixenginetextureslicedescriptor"></span>PixEngineTextureSliceDescriptor, structure</span><span class="sxs-lookup"><span data-stu-id="31a85-103"><span id="vspixengine.pixenginetextureslicedescriptor"></span>PixEngineTextureSliceDescriptor structure</span></span>

<span data-ttu-id="31a85-104">Représente une description d’une tranche de texture.</span><span class="sxs-lookup"><span data-stu-id="31a85-104">Represents a description of a texture slice.</span></span>

## <a name="syntax"></a><span data-ttu-id="31a85-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31a85-105">Syntax</span></span>


```C++
} PixEngineTextureSliceDescriptor;
```

## <a name="members"></a><span data-ttu-id="31a85-106">Membres</span><span class="sxs-lookup"><span data-stu-id="31a85-106">Members</span></span>

<span data-ttu-id="31a85-107">**width**</span><span class="sxs-lookup"><span data-stu-id="31a85-107">**width**</span></span>  
<span data-ttu-id="31a85-108">Largeur (nombre d’échantillons dans l’axe des X) de la tranche.</span><span class="sxs-lookup"><span data-stu-id="31a85-108">The width (number of samples in the X axis) of the slice.</span></span>

<span data-ttu-id="31a85-109">**height**</span><span class="sxs-lookup"><span data-stu-id="31a85-109">**height**</span></span>  
<span data-ttu-id="31a85-110">Hauteur (nombre d’échantillons sur l’axe des Y) de la tranche.</span><span class="sxs-lookup"><span data-stu-id="31a85-110">The height (number of samples in the Y axis) of the slice.</span></span>

<span data-ttu-id="31a85-111">**blockRowBytes**</span><span class="sxs-lookup"><span data-stu-id="31a85-111">**blockRowBytes**</span></span>  
<span data-ttu-id="31a85-112">Nombre d’octets par ligne dans chaque bloc.</span><span class="sxs-lookup"><span data-stu-id="31a85-112">The number of bytes per row in each block.</span></span>

<span data-ttu-id="31a85-113">**offset**</span><span class="sxs-lookup"><span data-stu-id="31a85-113">**offset**</span></span>  
<span data-ttu-id="31a85-114">Décalage de la tranche dans la texture entière.</span><span class="sxs-lookup"><span data-stu-id="31a85-114">The offset of the slice within the whole texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="31a85-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31a85-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="31a85-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="31a85-116">Header</span></span></p></td><td><span data-ttu-id="31a85-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="31a85-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



