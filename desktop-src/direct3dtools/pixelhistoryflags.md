---
description: Énumération contenant les indicateurs utilisés pour décrire le résultat de l’historique des pixels. Consultez PixelHistoryOperation.
MS-HAID: vspixengine.PIXELHISTORYFLAGS
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Énumération PIXELHISTORYFLAGS
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BDB88A2D-016A-4E15-B47A-870A2959E943
api_name:
- PIXELHISTORYFLAGS
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2a1b4b0e5b3df84af04d5533ec9d53b15ebe5057
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108939"
---
# <a name="span-idvspixenginepixelhistoryflagsspanpixelhistoryflags-enumeration"></a><span data-ttu-id="42cf9-104"><span id="vspixengine.pixelhistoryflags"></span>Énumération PIXELHISTORYFLAGS</span><span class="sxs-lookup"><span data-stu-id="42cf9-104"><span id="vspixengine.pixelhistoryflags"></span>PIXELHISTORYFLAGS enumeration</span></span>

<span data-ttu-id="42cf9-105">Énumération contenant les indicateurs utilisés pour décrire le résultat de l’historique des pixels.</span><span class="sxs-lookup"><span data-stu-id="42cf9-105">An enum containing flags used to describe a pixel history result.</span></span> <span data-ttu-id="42cf9-106">Consultez PixelHistoryOperation.</span><span class="sxs-lookup"><span data-stu-id="42cf9-106">See PixelHistoryOperation.</span></span>

## <a name="syntax"></a><span data-ttu-id="42cf9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42cf9-107">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="42cf9-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="42cf9-108">Constants</span></span>

<span data-ttu-id="42cf9-109"><span id="PHF_INITIALVALUE"></span><span id="phf_initialvalue"></span>**PHF \_ INITIALVALUE**</span><span class="sxs-lookup"><span data-stu-id="42cf9-109"><span id="PHF_INITIALVALUE"></span><span id="phf_initialvalue"></span>**PHF\_INITIALVALUE**</span></span>  
<span data-ttu-id="42cf9-110">Indicateur qui correspond à la valeur de couleur initiale (avant le cadre).</span><span class="sxs-lookup"><span data-stu-id="42cf9-110">A flag that corresponds to the initial color value (prior to frame).</span></span>

<span data-ttu-id="42cf9-111"><span id="PHF_CLEAR"></span><span id="phf_clear"></span>**PHF \_ Clear**</span><span class="sxs-lookup"><span data-stu-id="42cf9-111"><span id="PHF_CLEAR"></span><span id="phf_clear"></span>**PHF\_CLEAR**</span></span>  
<span data-ttu-id="42cf9-112">Indicateur qui correspond au résultat de la couleur d’effacement.</span><span class="sxs-lookup"><span data-stu-id="42cf9-112">A flag that corresponds to the clear color result.</span></span>

<span data-ttu-id="42cf9-113"><span id="PHF_DRAW"></span><span id="phf_draw"></span>**PHF \_ dessin**</span><span class="sxs-lookup"><span data-stu-id="42cf9-113"><span id="PHF_DRAW"></span><span id="phf_draw"></span>**PHF\_DRAW**</span></span>  
<span data-ttu-id="42cf9-114">Indicateur qui correspond au résultat de la couleur de dessin.</span><span class="sxs-lookup"><span data-stu-id="42cf9-114">A flag that corresponds to the draw color result.</span></span>

<span data-ttu-id="42cf9-115"><span id="PHF_FINALVALUE"></span><span id="phf_finalvalue"></span>**PHF \_ FINALVALUE**</span><span class="sxs-lookup"><span data-stu-id="42cf9-115"><span id="PHF_FINALVALUE"></span><span id="phf_finalvalue"></span>**PHF\_FINALVALUE**</span></span>  
<span data-ttu-id="42cf9-116">Indicateur qui correspond au résultat final de la couleur.</span><span class="sxs-lookup"><span data-stu-id="42cf9-116">A flag that corresponds to the final color result.</span></span>

<span data-ttu-id="42cf9-117"><span id="PHF_HASCOLOR"></span><span id="phf_hascolor"></span>**PHF \_ HASCOLOR**</span><span class="sxs-lookup"><span data-stu-id="42cf9-117"><span id="PHF_HASCOLOR"></span><span id="phf_hascolor"></span>**PHF\_HASCOLOR**</span></span>  
<span data-ttu-id="42cf9-118">Indicateur qui correspond à si le résultat de couleur est présent dans le struct PixelHistoryOperation.</span><span class="sxs-lookup"><span data-stu-id="42cf9-118">A flag that corresponds to whether the color result is present in the PixelHistoryOperation struct.</span></span>

<span data-ttu-id="42cf9-119"><span id="PHF_HASFBCOLOR"></span><span id="phf_hasfbcolor"></span>**PHF \_ HASFBCOLOR**</span><span class="sxs-lookup"><span data-stu-id="42cf9-119"><span id="PHF_HASFBCOLOR"></span><span id="phf_hasfbcolor"></span>**PHF\_HASFBCOLOR**</span></span>  
<span data-ttu-id="42cf9-120">Indicateur qui correspond à si le résultat final de la couleur de la mémoire tampon est présent dans la structure PixelHistoryOperation.</span><span class="sxs-lookup"><span data-stu-id="42cf9-120">A flag that corresponds to whether the final buffer color result is present in the PixelHistoryOperation struct.</span></span>

<span data-ttu-id="42cf9-121"><span id="PHF_ERROR"></span><span id="phf_error"></span>**\_erreur PHF**</span><span class="sxs-lookup"><span data-stu-id="42cf9-121"><span id="PHF_ERROR"></span><span id="phf_error"></span>**PHF\_ERROR**</span></span>  

<span data-ttu-id="42cf9-122"><span id="PHF_VERTEXPROCESSINGSKIPPED"></span><span id="phf_vertexprocessingskipped"></span>**PHF \_ VERTEXPROCESSINGSKIPPED**</span><span class="sxs-lookup"><span data-stu-id="42cf9-122"><span id="PHF_VERTEXPROCESSINGSKIPPED"></span><span id="phf_vertexprocessingskipped"></span>**PHF\_VERTEXPROCESSINGSKIPPED**</span></span>  
<span data-ttu-id="42cf9-123">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="42cf9-123">Not used.</span></span>

<span data-ttu-id="42cf9-124"><span id="PHF_MODIFYRESOURCE"></span><span id="phf_modifyresource"></span>**PHF \_ MODIFYRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="42cf9-124"><span id="PHF_MODIFYRESOURCE"></span><span id="phf_modifyresource"></span>**PHF\_MODIFYRESOURCE**</span></span>  

<span data-ttu-id="42cf9-125"><span id="PHF_CANNOTRUNFULLDEPTHSTENCILTEST"></span><span id="phf_cannotrunfulldepthstenciltest"></span>**PHF \_ CANNOTRUNFULLDEPTHSTENCILTEST**</span><span class="sxs-lookup"><span data-stu-id="42cf9-125"><span id="PHF_CANNOTRUNFULLDEPTHSTENCILTEST"></span><span id="phf_cannotrunfulldepthstenciltest"></span>**PHF\_CANNOTRUNFULLDEPTHSTENCILTEST**</span></span>  
<span data-ttu-id="42cf9-126">Indicateur qui correspond à ne pas pouvoir exécuter le test de profondeur ou de stencil.</span><span class="sxs-lookup"><span data-stu-id="42cf9-126">A flag that corresponds to not being able to run the depth or stencil test.</span></span>

## <a name="requirements"></a><span data-ttu-id="42cf9-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42cf9-127">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="42cf9-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="42cf9-128">Header</span></span></p></td><td><span data-ttu-id="42cf9-129">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="42cf9-129">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



