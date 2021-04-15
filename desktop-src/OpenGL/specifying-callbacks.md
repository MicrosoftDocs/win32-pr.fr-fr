---
title: Spécifier des rappels
description: Vous pouvez spécifier jusqu’à cinq fonctions de rappel pour un pavage.
ms.assetid: b49a8400-8111-450d-a2d7-c313a898a213
keywords:
- Utilitaire OpenGL (GLU), spécification de fonctions de rappel
- GLU (utilitaire OpenGL), spécification de fonctions de rappel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6086448cf6f4a71ea6a49359d5656f12f613d760
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507410"
---
# <a name="specifying-callbacks"></a><span data-ttu-id="61136-105">Spécifier des rappels</span><span class="sxs-lookup"><span data-stu-id="61136-105">Specifying Callbacks</span></span>

<span data-ttu-id="61136-106">Vous pouvez spécifier jusqu’à cinq fonctions de rappel pour un pavage.</span><span class="sxs-lookup"><span data-stu-id="61136-106">You can specify up to five callback functions for a tessellation.</span></span> <span data-ttu-id="61136-107">Toutes les fonctions que vous ne spécifiez pas ne sont pas appelées pendant le pavage et aucune information n’est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="61136-107">Any functions that you do not specify are not called during the tessellation, and you do not get any information they might have returned.</span></span> <span data-ttu-id="61136-108">Vous spécifiez les fonctions de rappel avec [*gluTessCallback*](glutess.md).</span><span class="sxs-lookup"><span data-stu-id="61136-108">You specify the callback functions with [*gluTessCallback*](glutess.md).</span></span>

<span data-ttu-id="61136-109">La fonction **gluTessCallback** associe la fonction de rappel *FN* à l’objet de pavage *tessobj*.</span><span class="sxs-lookup"><span data-stu-id="61136-109">The **gluTessCallback** function associates the callback function *fn* with the tessellation object *tessobj*.</span></span> <span data-ttu-id="61136-110">Le type du rappel est déterminé par le *type* de paramètre, qui peut être **Glu \_ Begin**, **Glu \_ Edge \_ Flag**, **Glu \_ vertex**, **Glu \_ end** ou **Glu \_ Error**.</span><span class="sxs-lookup"><span data-stu-id="61136-110">The type of the callback is determined by the parameter *type*, which can be **GLU\_BEGIN**, **GLU\_EDGE\_FLAG**, **GLU\_VERTEX**, **GLU\_END**, or **GLU\_ERROR**.</span></span> <span data-ttu-id="61136-111">Les cinq fonctions de rappel possibles ont les prototypes suivants.</span><span class="sxs-lookup"><span data-stu-id="61136-111">The five possible callback functions have the following prototypes.</span></span>



| <span data-ttu-id="61136-112">Fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="61136-112">Callback function</span></span>   | <span data-ttu-id="61136-113">Prototype</span><span class="sxs-lookup"><span data-stu-id="61136-113">Prototype</span></span>                                    |
|---------------------|----------------------------------------------|
| <span data-ttu-id="61136-114">**début de GLU \_**</span><span class="sxs-lookup"><span data-stu-id="61136-114">**GLU\_BEGIN**</span></span>      | <span data-ttu-id="61136-115">**void** **Begin**(\**GLenum \* \* \* type* );</span><span class="sxs-lookup"><span data-stu-id="61136-115">**void** **begin**(\**GLenum\*\*\*type* );</span></span>       |
| <span data-ttu-id="61136-116">**\_indicateur de bord Glu \_**</span><span class="sxs-lookup"><span data-stu-id="61136-116">**GLU\_EDGE\_FLAG**</span></span> | <span data-ttu-id="61136-117">**void** **EdgeFlag**(\**GLboolean \* \* \* indicateur* );</span><span class="sxs-lookup"><span data-stu-id="61136-117">**void** **edgeFlag**(\**GLboolean\*\*\*flag* );</span></span> |
| <span data-ttu-id="61136-118">**GLU \_ vertex**</span><span class="sxs-lookup"><span data-stu-id="61136-118">**GLU\_VERTEX**</span></span>     | <span data-ttu-id="61136-119">**void** **vertex**(\**void \* \* \* \* Data* );</span><span class="sxs-lookup"><span data-stu-id="61136-119">**void** **vertex**(\**void \*\*\*\*data* );</span></span>     |
| <span data-ttu-id="61136-120">**fin de GLU \_**</span><span class="sxs-lookup"><span data-stu-id="61136-120">**GLU\_END**</span></span>        | <span data-ttu-id="61136-121">**void** **end**( *void* );</span><span class="sxs-lookup"><span data-stu-id="61136-121">**void** **end**( *void* );</span></span>                  |
| <span data-ttu-id="61136-122">**\_erreur Glu**</span><span class="sxs-lookup"><span data-stu-id="61136-122">**GLU\_ERROR**</span></span>      | <span data-ttu-id="61136-123"> **erreur** void \(\**GLenum\ \**\ *\ * errno);</span><span class="sxs-lookup"><span data-stu-id="61136-123">**void** **error**(\**GLenum\*\*\*errno* );</span></span>      |



 

<span data-ttu-id="61136-124">Pour modifier une fonction de rappel, appelez [*gluTessCallback*](glutess.md) avec la nouvelle fonction.</span><span class="sxs-lookup"><span data-stu-id="61136-124">To change a callback function, call [*gluTessCallback*](glutess.md) with the new function.</span></span> <span data-ttu-id="61136-125">Pour éliminer une fonction de rappel sans la remplacer par une nouvelle, transmettez **gluTessCallback** un pointeur null pour la fonction appropriée.</span><span class="sxs-lookup"><span data-stu-id="61136-125">To eliminate a callback function without replacing it with a new one, pass **gluTessCallback** a null pointer for the appropriate function.</span></span>

<span data-ttu-id="61136-126">À mesure que le pavage se poursuit, les fonctions de rappel sont appelées de manière similaire à la façon dont vous utilisez les fonctions OpenGL [**glBegin**](glbegin.md), [glEdgeFlag](gledgeflag-functions.md), [glVertex](glvertex-functions.md)et [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="61136-126">As tessellation proceeds, the callback functions are called in a manner similar to the way you would use the OpenGL functions [**glBegin**](glbegin.md), [glEdgeFlag](gledgeflag-functions.md), [glVertex](glvertex-functions.md), and [**glEnd**](glend.md).</span></span>

<span data-ttu-id="61136-127">La fonction de rappel **Glu \_ Begin** est appelée avec l’un des trois paramètres possibles :</span><span class="sxs-lookup"><span data-stu-id="61136-127">The **GLU\_BEGIN** callback function is invoked with one of three possible parameters:</span></span>

-   <span data-ttu-id="61136-128">\_ventilateur à triangles GL \_</span><span class="sxs-lookup"><span data-stu-id="61136-128">GL\_TRIANGLE\_FAN</span></span>
-   <span data-ttu-id="61136-129">\_bande triangulaire GL \_</span><span class="sxs-lookup"><span data-stu-id="61136-129">GL\_TRIANGLE\_STRIP</span></span>
-   <span data-ttu-id="61136-130">\_TRIangles GL</span><span class="sxs-lookup"><span data-stu-id="61136-130">GL\_TRIANGLES</span></span>

<span data-ttu-id="61136-131">Après l’appel de la fonction de rappel **Glu \_ Begin** , et avant l’appel de la fonction de rappel associée à **Glu \_ end**, une combinaison de l' **\_ \_ indicateur de périphérie Glu** et des rappels de **\_ vertex Glu** est appelée.</span><span class="sxs-lookup"><span data-stu-id="61136-131">After calling the **GLU\_BEGIN** callback function, and before calling the callback function associated with **GLU\_END**, some combination of the **GLU\_EDGE\_FLAG** and **GLU\_VERTEX** callbacks is invoked.</span></span> <span data-ttu-id="61136-132">Les sommets et les indicateurs de bord associés sont interprétés exactement comme ils se trouvent dans OpenGL entre **glBegin**(ventilateur triangulaire GL \_ \_ ), **glBegin**( \_ bande triangulaire GL \_ ) ou **GlBegin**( \_ triangles GL **)** et le **glEnd** de correspondance.</span><span class="sxs-lookup"><span data-stu-id="61136-132">The associated vertices and edge flags are interpreted exactly as they are in OpenGL between **glBegin**(GL\_TRIANGLE\_FAN), **glBegin**(GL\_TRIANGLE\_STRIP), or **glBegin**(GL\_TRIANGLES **)** and the matching **glEnd**.</span></span>

<span data-ttu-id="61136-133">Étant donné que les indicateurs de périphérie n’ont aucune signification dans un ventilateur triangulaire ou une bande triangulaire, si une fonction de rappel est associée à l' **\_ \_ indicateur Glu Edge**, le rappel de **\_ début Glu** est appelé uniquement avec des **\_ triangles GL**.</span><span class="sxs-lookup"><span data-stu-id="61136-133">Because edge flags make no sense in a triangle fan or triangle strip, if there is a callback function associated with **GLU\_EDGE\_FLAG**, the **GLU\_BEGIN** callback is called only with **GL\_TRIANGLES**.</span></span> <span data-ttu-id="61136-134">La fonction de rappel de l' **\_ \_ indicateur Edge Glu** fonctionne de la même façon que la fonction [glEdgeFlag](gledgeflag-functions.md) OpenGL.</span><span class="sxs-lookup"><span data-stu-id="61136-134">The **GLU\_EDGE\_FLAG** callback function works analogously to the OpenGL [glEdgeFlag](gledgeflag-functions.md) function.</span></span>

<span data-ttu-id="61136-135">En cas d’erreur pendant le pavage, la fonction de rappel d’erreur est appelée.</span><span class="sxs-lookup"><span data-stu-id="61136-135">If there is an error during the tessellation, the error callback function is invoked.</span></span> <span data-ttu-id="61136-136">La fonction de rappel d’erreur reçoit un numéro d’erreur GLU.</span><span class="sxs-lookup"><span data-stu-id="61136-136">The error callback function is passed a GLU error number.</span></span> <span data-ttu-id="61136-137">Vous pouvez obtenir une chaîne de caractères décrivant l’erreur avec la fonction [**gluErrorString**](gluerrorstring.md) .</span><span class="sxs-lookup"><span data-stu-id="61136-137">You can obtain a character string describing the error with the [**gluErrorString**](gluerrorstring.md) function.</span></span>

 

 




