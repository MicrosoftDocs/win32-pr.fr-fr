---
title: Utilisation des fonctions d’anticrénelage
description: Le tableau suivant répertorie les fonctions d’anticrénelage du GL d’IRIS et leurs fonctions OpenGL équivalentes.
ms.assetid: d54990b6-5645-4389-82ca-7d7f0a7fd7e9
keywords:
- Portage de l’IRIS dans le GL, anticrénelage
- Portage à partir de IRIS GL, anticrénelage
- portage vers OpenGL à partir de IRIS GL, anticrénelage
- Portage OpenGL depuis IRIS GL, anticrénelage
- anticrénelage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896d02dec050c72e59762ff5ee139b0bd091d9a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196577"
---
# <a name="using-antialiasing-functions"></a><span data-ttu-id="24f9c-108">Utilisation des fonctions d’anticrénelage</span><span class="sxs-lookup"><span data-stu-id="24f9c-108">Using Antialiasing Functions</span></span>

<span data-ttu-id="24f9c-109">Le tableau suivant répertorie les fonctions d’anticrénelage du GL d’IRIS et leurs fonctions OpenGL équivalentes.</span><span class="sxs-lookup"><span data-stu-id="24f9c-109">The following table lists IRIS GL antialiasing functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="24f9c-110">Fonction IRIS GL</span><span class="sxs-lookup"><span data-stu-id="24f9c-110">IRIS GL function</span></span> | <span data-ttu-id="24f9c-111">Fonction OpenGL</span><span class="sxs-lookup"><span data-stu-id="24f9c-111">OpenGL function</span></span>                                      | <span data-ttu-id="24f9c-112">Signification</span><span class="sxs-lookup"><span data-stu-id="24f9c-112">Meaning</span></span>                           |
|------------------|------------------------------------------------------|-----------------------------------|
| <span data-ttu-id="24f9c-113">**pntsmooth**</span><span class="sxs-lookup"><span data-stu-id="24f9c-113">**pntsmooth**</span></span>    | <span data-ttu-id="24f9c-114">[**glEnable**](glenable.md) ( \_ Smooth point GL \_ )</span><span class="sxs-lookup"><span data-stu-id="24f9c-114">[**glEnable**](glenable.md) ( GL\_POINT\_SMOOTH )</span></span>   | <span data-ttu-id="24f9c-115">Permet l’anticrénelage des points.</span><span class="sxs-lookup"><span data-stu-id="24f9c-115">Enables antialiasing of points.</span></span>   |
| <span data-ttu-id="24f9c-116">**linesmooth**</span><span class="sxs-lookup"><span data-stu-id="24f9c-116">**linesmooth**</span></span>   | <span data-ttu-id="24f9c-117">**glEnable**(lisse de la \_ ligne GL \_ )</span><span class="sxs-lookup"><span data-stu-id="24f9c-117">**glEnable**( GL\_LINE\_SMOOTH )</span></span>                     | <span data-ttu-id="24f9c-118">Permet l’anticrénelage des lignes.</span><span class="sxs-lookup"><span data-stu-id="24f9c-118">Enables antialiasing of lines.</span></span>    |
| <span data-ttu-id="24f9c-119">**polylisse**</span><span class="sxs-lookup"><span data-stu-id="24f9c-119">**polysmooth**</span></span>   | <span data-ttu-id="24f9c-120">[**glEnable**](glenable.md) ( \_ polygones GL \_ lisse)</span><span class="sxs-lookup"><span data-stu-id="24f9c-120">[**glEnable**](glenable.md) ( GL\_POLYGON\_SMOOTH )</span></span> | <span data-ttu-id="24f9c-121">Permet l’anticrénelage des polygones.</span><span class="sxs-lookup"><span data-stu-id="24f9c-121">Enables antialiasing of polygons.</span></span> |



 

<span data-ttu-id="24f9c-122">Utilisez les appels [**glDisable**](gldisable.md) équivalents pour désactiver l’anticrénelage.</span><span class="sxs-lookup"><span data-stu-id="24f9c-122">Use the equivalent [**glDisable**](gldisable.md) calls to turn off antialiasing.</span></span>

<span data-ttu-id="24f9c-123">Dans IRIS GL, vous pouvez contrôler la qualité de l’anticrénelage en appelant :</span><span class="sxs-lookup"><span data-stu-id="24f9c-123">In IRIS GL, you can control the quality of the antialiasing by calling:</span></span>


```C++
linesmooth(SML_ON + SML_SMOOTHER);
```



<span data-ttu-id="24f9c-124">OpenGL fournit des [**glHint**](glhint.md)controluse similaires :</span><span class="sxs-lookup"><span data-stu-id="24f9c-124">OpenGL provides similar controluse [**glHint**](glhint.md):</span></span>


```C++
glHint(GL_POINT_SMOOTH_HINT, hintMode); 
glHint(GL_LINE_SMOOTH_HINT, hintMode); 
glHint(GL_POLYGON_SMOOTH_HINT, hintMode);
```



<span data-ttu-id="24f9c-125">où *hintMode* est l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="24f9c-125">where *hintMode* is one of the following:</span></span>

-   <span data-ttu-id="24f9c-126">Grand livrest \_ (utilisez le lissage de qualité le plus élevé).</span><span class="sxs-lookup"><span data-stu-id="24f9c-126">GL\_NICEST (Use the highest quality smoothing.)</span></span>
-   <span data-ttu-id="24f9c-127">GL plus \_ rapide (utilisez le lissage le plus efficace).</span><span class="sxs-lookup"><span data-stu-id="24f9c-127">GL\_FASTEST (Use the most efficient smoothing.)</span></span>
-   <span data-ttu-id="24f9c-128">comptabilité \_ générale \_</span><span class="sxs-lookup"><span data-stu-id="24f9c-128">GL\_DONT\_CARE</span></span>

<span data-ttu-id="24f9c-129">IRIS GL autorise également la correction finale en appelant :</span><span class="sxs-lookup"><span data-stu-id="24f9c-129">IRIS GL also permits end-correction by calling:</span></span>


```C++
linesmooth(SML_ON +  SML_END_CORRECT);
```



<span data-ttu-id="24f9c-130">OpenGL n’a pas d’équivalent pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="24f9c-130">OpenGL has no equivalent for this function.</span></span>

 

 




