---
title: Lignes de Portage
description: Le portage du code du GL IRIS qui dessine des lignes est relativement simple, mais vous devez noter les différences de la façon dont OpenGL stipples. Le tableau suivant répertorie les fonctions d’IRIS dans le GL pour dessiner des lignes et leurs fonctions OpenGL équivalentes.
ms.assetid: de5fd544-5a64-44b5-8976-b96867e4006d
keywords:
- Portage de l’IRIS dans le GL, lignes
- Portage à partir de IRIS GL, lignes
- portage vers OpenGL à partir de IRIS GL, lignes
- Portage OpenGL à partir de IRIS GL, lignes
- fonctions de dessin, lignes
- lignes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9c97593d0230d6830cf3d3ce8fa2c13466e21e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197165"
---
# <a name="porting-lines"></a><span data-ttu-id="4eba7-110">Lignes de Portage</span><span class="sxs-lookup"><span data-stu-id="4eba7-110">Porting Lines</span></span>

<span data-ttu-id="4eba7-111">Le portage du code du GL IRIS qui dessine des lignes est relativement simple, mais vous devez noter les différences de la façon dont OpenGL stipples.</span><span class="sxs-lookup"><span data-stu-id="4eba7-111">Porting IRIS GL code that draws lines is fairly straightforward, though you should note the differences in the way OpenGL stipples.</span></span> <span data-ttu-id="4eba7-112">Le tableau suivant répertorie les fonctions d’IRIS dans le GL pour dessiner des lignes et leurs fonctions OpenGL équivalentes.</span><span class="sxs-lookup"><span data-stu-id="4eba7-112">The following table lists IRIS GL functions for drawing lines and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="4eba7-113">Fonction IRIS GL</span><span class="sxs-lookup"><span data-stu-id="4eba7-113">IRIS GL function</span></span>                               | <span data-ttu-id="4eba7-114">Fonction OpenGL</span><span class="sxs-lookup"><span data-stu-id="4eba7-114">OpenGL function</span></span>                                                                                         | <span data-ttu-id="4eba7-115">Signification</span><span class="sxs-lookup"><span data-stu-id="4eba7-115">Meaning</span></span>                                                                                                                                      |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4eba7-116">**bgnclosedline**,**endclosedline**</span><span class="sxs-lookup"><span data-stu-id="4eba7-116">**bgnclosedline**,**endclosedline**</span></span><br/> | <span data-ttu-id="4eba7-117">[**glBegin**](glbegin.md) ( \_ boucle de ligne GL \_ )[**glEnd**](glend.md)</span><span class="sxs-lookup"><span data-stu-id="4eba7-117">[**glBegin**](glbegin.md) ( GL\_LINE\_LOOP )[**glEnd**](glend.md)</span></span><br/>                          | <span data-ttu-id="4eba7-118">Dessine une ligne fermée.</span><span class="sxs-lookup"><span data-stu-id="4eba7-118">Draws a closed line.</span></span>                                                                                                                         |
| <span data-ttu-id="4eba7-119">**bgnline**</span><span class="sxs-lookup"><span data-stu-id="4eba7-119">**bgnline**</span></span>                                    | <span data-ttu-id="4eba7-120">[**glBegin**](glbegin.md) ( \_ bande de lignes GL \_ )</span><span class="sxs-lookup"><span data-stu-id="4eba7-120">[**glBegin**](glbegin.md) ( GL\_LINE\_STRIP )</span></span>                                                          | <span data-ttu-id="4eba7-121">Dessine des segments de ligne.</span><span class="sxs-lookup"><span data-stu-id="4eba7-121">Draws line segments.</span></span>                                                                                                                         |
| <span data-ttu-id="4eba7-122">**linewidth**</span><span class="sxs-lookup"><span data-stu-id="4eba7-122">**linewidth**</span></span>                                  | [<span data-ttu-id="4eba7-123">**glLineWidth**</span><span class="sxs-lookup"><span data-stu-id="4eba7-123">**glLineWidth**</span></span>](gllinewidth.md)                                                                      | <span data-ttu-id="4eba7-124">Définit la largeur de ligne.</span><span class="sxs-lookup"><span data-stu-id="4eba7-124">Sets line width.</span></span>                                                                                                                             |
| <span data-ttu-id="4eba7-125">**getlwidth**</span><span class="sxs-lookup"><span data-stu-id="4eba7-125">**getlwidth**</span></span>                                  | <span data-ttu-id="4eba7-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (largeur de ligne du GL \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="4eba7-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_LINE\_WIDTH )</span></span>            | <span data-ttu-id="4eba7-127">Retourne la largeur de la ligne active.</span><span class="sxs-lookup"><span data-stu-id="4eba7-127">Returns current line width.</span></span>                                                                                                                  |
| <span data-ttu-id="4eba7-128">**deflinestyle**,**setlinestyle**</span><span class="sxs-lookup"><span data-stu-id="4eba7-128">**deflinestyle**,**setlinestyle**</span></span><br/>   | [<span data-ttu-id="4eba7-129">**glLineStipple**</span><span class="sxs-lookup"><span data-stu-id="4eba7-129">**glLineStipple**</span></span>](gllinestipple.md)                                                                  | <span data-ttu-id="4eba7-130">Spécifie un modèle de stipple de ligne.</span><span class="sxs-lookup"><span data-stu-id="4eba7-130">Specifies a line stipple pattern.</span></span>                                                                                                            |
| <span data-ttu-id="4eba7-131">**lsrepeat**</span><span class="sxs-lookup"><span data-stu-id="4eba7-131">**lsrepeat**</span></span>                                   | <span data-ttu-id="4eba7-132">argument factor de **glLineStipple**</span><span class="sxs-lookup"><span data-stu-id="4eba7-132">factor argument of **glLineStipple**</span></span>                                                                    | <span data-ttu-id="4eba7-133">Définit un facteur de répétition pour le style de ligne.</span><span class="sxs-lookup"><span data-stu-id="4eba7-133">Sets a repeat factor for the line style.</span></span>                                                                                                     |
| <span data-ttu-id="4eba7-134">**getlstyle**</span><span class="sxs-lookup"><span data-stu-id="4eba7-134">**getlstyle**</span></span>                                  | <span data-ttu-id="4eba7-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ modèle STIPPLE de la ligne GL \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="4eba7-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_LINE\_STIPPLE\_PATTERN )</span></span> | <span data-ttu-id="4eba7-136">Retourne le modèle de stipple de ligne.</span><span class="sxs-lookup"><span data-stu-id="4eba7-136">Returns line stipple pattern.</span></span>                                                                                                                |
| <span data-ttu-id="4eba7-137">**getlsrepeat**</span><span class="sxs-lookup"><span data-stu-id="4eba7-137">**getlsrepeat**</span></span>                                | <span data-ttu-id="4eba7-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (STIPPLE de la ligne GL- \_ \_ \_ répéter)</span><span class="sxs-lookup"><span data-stu-id="4eba7-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_LINE\_STIPPLE\_REPEAT )</span></span>  | <span data-ttu-id="4eba7-139">Retourne le facteur de répétition.</span><span class="sxs-lookup"><span data-stu-id="4eba7-139">Returns repeat factor.</span></span>                                                                                                                       |
| <span data-ttu-id="4eba7-140">**linesmooth**, **smoothline**</span><span class="sxs-lookup"><span data-stu-id="4eba7-140">**linesmooth**, **smoothline**</span></span>                 | <span data-ttu-id="4eba7-141">[**glEnable**](glenable.md) (lisse de la \_ ligne GL \_ )</span><span class="sxs-lookup"><span data-stu-id="4eba7-141">[**glEnable**](glenable.md) ( GL\_LINE\_SMOOTH )</span></span>                                                       | <span data-ttu-id="4eba7-142">Active l’anticrénelage de ligne (pour plus d’informations sur l’anticrénelage, consultez [Portage de fonctions d’anticrénelage](porting-antialiasing-functions.md).)</span><span class="sxs-lookup"><span data-stu-id="4eba7-142">Turns on line antialiasing (For more information on antialiasing, see [Porting Antialiasing Functions](porting-antialiasing-functions.md).)</span></span> |



 

<span data-ttu-id="4eba7-143">OpenGL n’utilise pas de tables pour la ligne stipples ; il ne gère qu’un seul modèle stipple.</span><span class="sxs-lookup"><span data-stu-id="4eba7-143">OpenGL doesn't use tables for line stipples; it maintains only one line-stipple pattern.</span></span> <span data-ttu-id="4eba7-144">Vous pouvez utiliser [**glPushAttrib**](glpushattrib.md) et [**glPopAttrib**](glpopattrib.md) pour basculer entre les différents modèles de stipple.</span><span class="sxs-lookup"><span data-stu-id="4eba7-144">You can use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) to switch between different stipple patterns.</span></span>

<span data-ttu-id="4eba7-145">OpenGL ne prend pas en charge les fonctions anciennes de style de ligne de l’IRIS dans le GL (telles que **Draw**, **lsbackup**, **getlsbackup**, etc.).</span><span class="sxs-lookup"><span data-stu-id="4eba7-145">Older IRIS GL line style functions (such as **draw**, **lsbackup**, **getlsbackup**, and so on) are not supported by OpenGL.</span></span>

<span data-ttu-id="4eba7-146">Pour plus d’informations sur le dessin des lignes avec anticrénelage, consultez [Portage de fonctions d’anticrénelage](porting-antialiasing-functions.md).</span><span class="sxs-lookup"><span data-stu-id="4eba7-146">For information on drawing antialiased lines, see [Porting Antialiasing Functions](porting-antialiasing-functions.md).</span></span>

<span data-ttu-id="4eba7-147">??</span><span class="sxs-lookup"><span data-stu-id="4eba7-147">??</span></span>

 

 





