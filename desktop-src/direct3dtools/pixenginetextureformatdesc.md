---
description: Représente une description d’un format de texture.
MS-HAID: vspixengine.PixEngineTextureFormatDesc
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PixEngineTextureFormatDesc, structure
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 685DC746-544D-4ACB-AB1F-9FA62C5CF416
api_name:
- PixEngineTextureFormatDesc
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 960186f0c28be88805c1df65f1a517c4ce4a4c64
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103950213"
---
# <a name="span-idvspixenginepixenginetextureformatdescspanpixenginetextureformatdesc-structure"></a><span data-ttu-id="26ed8-103"><span id="vspixengine.pixenginetextureformatdesc"></span>PixEngineTextureFormatDesc, structure</span><span class="sxs-lookup"><span data-stu-id="26ed8-103"><span id="vspixengine.pixenginetextureformatdesc"></span>PixEngineTextureFormatDesc structure</span></span>

<span data-ttu-id="26ed8-104">Représente une description d’un format de texture.</span><span class="sxs-lookup"><span data-stu-id="26ed8-104">Represents a description of a texture format.</span></span>

## <a name="syntax"></a><span data-ttu-id="26ed8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26ed8-105">Syntax</span></span>


```C++
} PixEngineTextureFormatDesc;
```

## <a name="members"></a><span data-ttu-id="26ed8-106">Membres</span><span class="sxs-lookup"><span data-stu-id="26ed8-106">Members</span></span>

<span data-ttu-id="26ed8-107">**dxgiFormat**</span><span class="sxs-lookup"><span data-stu-id="26ed8-107">**dxgiFormat**</span></span>  
<span data-ttu-id="26ed8-108">Format DXGI de la texture.</span><span class="sxs-lookup"><span data-stu-id="26ed8-108">The DXGI format of the texture.</span></span>

<span data-ttu-id="26ed8-109">**dataFormat**</span><span class="sxs-lookup"><span data-stu-id="26ed8-109">**dataFormat**</span></span>  
<span data-ttu-id="26ed8-110">Format de données de la texture.</span><span class="sxs-lookup"><span data-stu-id="26ed8-110">The data format of the texture.</span></span>

<span data-ttu-id="26ed8-111">**blockBytes**</span><span class="sxs-lookup"><span data-stu-id="26ed8-111">**blockBytes**</span></span>  
<span data-ttu-id="26ed8-112">Nombre d’octets dans un bloc de données.</span><span class="sxs-lookup"><span data-stu-id="26ed8-112">The number of bytes in a data block.</span></span>

<span data-ttu-id="26ed8-113">**blockHeight**</span><span class="sxs-lookup"><span data-stu-id="26ed8-113">**blockHeight**</span></span>  
<span data-ttu-id="26ed8-114">Hauteur (échantillons de nombre sur l’axe des Y) du bloc.</span><span class="sxs-lookup"><span data-stu-id="26ed8-114">The height (number samples in the Y axis) of the block.</span></span>

<span data-ttu-id="26ed8-115">**blockWidth**</span><span class="sxs-lookup"><span data-stu-id="26ed8-115">**blockWidth**</span></span>  
<span data-ttu-id="26ed8-116">Largeur (nombre d’échantillons dans l’axe des X) du bloc.</span><span class="sxs-lookup"><span data-stu-id="26ed8-116">The width (number of samples in the X axis) of the block.</span></span>

<span data-ttu-id="26ed8-117">**channelX**</span><span class="sxs-lookup"><span data-stu-id="26ed8-117">**channelX**</span></span>  
<span data-ttu-id="26ed8-118">Décrit les propriétés du canal X.</span><span class="sxs-lookup"><span data-stu-id="26ed8-118">Describes properties of the X channel.</span></span> <span data-ttu-id="26ed8-119">Pour plus d’informations, consultez la structure PixEngineChannelDescription.</span><span class="sxs-lookup"><span data-stu-id="26ed8-119">For more information, see the PixEngineChannelDescription structure.</span></span>

<span data-ttu-id="26ed8-120">**canalisation**</span><span class="sxs-lookup"><span data-stu-id="26ed8-120">**channelY**</span></span>  
<span data-ttu-id="26ed8-121">Décrit les propriétés du canal Y.</span><span class="sxs-lookup"><span data-stu-id="26ed8-121">Describes properties of the Y channel.</span></span> <span data-ttu-id="26ed8-122">Pour plus d’informations, consultez la structure PixEngineChannelDescription.</span><span class="sxs-lookup"><span data-stu-id="26ed8-122">For more information, see the PixEngineChannelDescription structure.</span></span>

<span data-ttu-id="26ed8-123">**channelZ**</span><span class="sxs-lookup"><span data-stu-id="26ed8-123">**channelZ**</span></span>  
<span data-ttu-id="26ed8-124">Décrit les propriétés du Canal Z.</span><span class="sxs-lookup"><span data-stu-id="26ed8-124">Describes properties of the Z channel.</span></span> <span data-ttu-id="26ed8-125">Pour plus d’informations, consultez la structure PixEngineChannelDescription.</span><span class="sxs-lookup"><span data-stu-id="26ed8-125">For more information, see the PixEngineChannelDescription structure.</span></span>

<span data-ttu-id="26ed8-126">**channelW**</span><span class="sxs-lookup"><span data-stu-id="26ed8-126">**channelW**</span></span>  
<span data-ttu-id="26ed8-127">Décrit les propriétés du canal W.</span><span class="sxs-lookup"><span data-stu-id="26ed8-127">Describes properties of the W channel.</span></span> <span data-ttu-id="26ed8-128">Pour plus d’informations, consultez la structure PixEngineChannelDescription.</span><span class="sxs-lookup"><span data-stu-id="26ed8-128">For more information, see the PixEngineChannelDescription structure.</span></span>

<span data-ttu-id="26ed8-129">**swizzle**</span><span class="sxs-lookup"><span data-stu-id="26ed8-129">**swizzle**</span></span>  
<span data-ttu-id="26ed8-130">Décrit le Swizzle (échange de canal) appliqué à l’exemple.</span><span class="sxs-lookup"><span data-stu-id="26ed8-130">Describes the swizzle (channel-swapping) applied to the sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="26ed8-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26ed8-131">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="26ed8-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="26ed8-132">Header</span></span></p></td><td><span data-ttu-id="26ed8-133">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="26ed8-133">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



