---
title: Portage de modèles d’ombrage
description: Comme IRIS GL, OpenGL vous permet de basculer entre l’ombrage lisse (Gouraud) et l’ombrage plat. Le tableau suivant répertorie les fonctions d’ombrage et de tramage de l’IRIS et leurs fonctions OpenGL équivalentes.
ms.assetid: 93e8f437-381f-4620-ad6f-52ce830d99b6
keywords:
- Portage de l’IRIS dans le GL, ombrage
- Portage à partir de IRIS GL, ombrage
- portage vers OpenGL à partir de IRIS GL, ombrage
- Portage OpenGL à partir de IRIS GL, ombrage
- ombrage lissé
- Ombrage Gouraud
- ombrage plat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124bb002f6f133b4d47dd40e1a0e8738c512ce99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310542"
---
# <a name="porting-shading-models"></a><span data-ttu-id="b64b0-111">Portage de modèles d’ombrage</span><span class="sxs-lookup"><span data-stu-id="b64b0-111">Porting Shading Models</span></span>

<span data-ttu-id="b64b0-112">Comme IRIS GL, OpenGL vous permet de basculer entre l’ombrage lisse (Gouraud) et l’ombrage plat.</span><span class="sxs-lookup"><span data-stu-id="b64b0-112">Like IRIS GL, OpenGL lets you switch between smooth (Gouraud) shading and flat shading.</span></span> <span data-ttu-id="b64b0-113">Le tableau suivant répertorie les fonctions d’ombrage et de tramage de l’IRIS et leurs fonctions OpenGL équivalentes.</span><span class="sxs-lookup"><span data-stu-id="b64b0-113">The following table lists the IRIS GL shading and dithering functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="b64b0-114">Fonction IRIS GL</span><span class="sxs-lookup"><span data-stu-id="b64b0-114">IRIS GL function</span></span>                                   | <span data-ttu-id="b64b0-115">Fonction OpenGL</span><span class="sxs-lookup"><span data-stu-id="b64b0-115">OpenGL function</span></span>                                                                                    | <span data-ttu-id="b64b0-116">Signification</span><span class="sxs-lookup"><span data-stu-id="b64b0-116">Meaning</span></span>                      |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="b64b0-117">**shademodel**(plat)</span><span class="sxs-lookup"><span data-stu-id="b64b0-117">**shademodel**(FLAT)</span></span>                               | <span data-ttu-id="b64b0-118">[**glShadeModel**](glshademodel.md) (GL \_ plat)</span><span class="sxs-lookup"><span data-stu-id="b64b0-118">[**glShadeModel**](glshademodel.md) ( GL\_FLAT )</span></span>                                                  | <span data-ttu-id="b64b0-119">Il s’agit d’un ombrage plat.</span><span class="sxs-lookup"><span data-stu-id="b64b0-119">Does flat shading.</span></span>           |
| <span data-ttu-id="b64b0-120">**shademodel**(Gouraud)</span><span class="sxs-lookup"><span data-stu-id="b64b0-120">**shademodel**(GOURAUD)</span></span>                            | <span data-ttu-id="b64b0-121">**glShadeModel**(GL \_ Smooth)</span><span class="sxs-lookup"><span data-stu-id="b64b0-121">**glShadeModel**( GL\_SMOOTH )</span></span>                                                                     | <span data-ttu-id="b64b0-122">Effectue un ombrage lissé.</span><span class="sxs-lookup"><span data-stu-id="b64b0-122">Does smooth shading.</span></span>         |
| <span data-ttu-id="b64b0-123">**est**</span><span class="sxs-lookup"><span data-stu-id="b64b0-123">**getsm**</span></span>                                          | <span data-ttu-id="b64b0-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ modèle d’ombrage GL \_ )</span><span class="sxs-lookup"><span data-stu-id="b64b0-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_SHADE\_MODEL )</span></span>      | <span data-ttu-id="b64b0-125">Retourne le modèle d’ombrage actuel.</span><span class="sxs-lookup"><span data-stu-id="b64b0-125">Returns current shade model.</span></span> |
| <span data-ttu-id="b64b0-126">**tramage (DT** \_ on) **tramé**(DT \_ off)</span><span class="sxs-lookup"><span data-stu-id="b64b0-126">**dither**(DT\_ON) **dither**(DT\_OFF)</span></span> <br/> | <span data-ttu-id="b64b0-127">[**glEnable**](glenable.md) (GL de \_ tramage)[**glDisable**](gldisable.md)(GL de \_ tramage)</span><span class="sxs-lookup"><span data-stu-id="b64b0-127">[**glEnable**](glenable.md) ( GL\_DITHER )[**glDisable**](gldisable.md)( GL\_DITHER )</span></span><br/> | <span data-ttu-id="b64b0-128">Active/désactive le tramage.</span><span class="sxs-lookup"><span data-stu-id="b64b0-128">Turns dithering on/off.</span></span>      |



 

<span data-ttu-id="b64b0-129">??</span><span class="sxs-lookup"><span data-stu-id="b64b0-129">??</span></span>

 

 





