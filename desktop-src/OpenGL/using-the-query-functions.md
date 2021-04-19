---
title: Utilisation des fonctions de requête
description: Utilisation des fonctions de requête
ms.assetid: 5f874a0e-77c0-4009-a18f-a852d7ffe891
keywords:
- OpenGL, fonctions de requête
- fonctions de requête OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14804b260451d4b51b0146b1cb2f796ba6b6778e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106508983"
---
# <a name="using-the-query-functions"></a><span data-ttu-id="4f2d7-105">Utilisation des fonctions de requête</span><span class="sxs-lookup"><span data-stu-id="4f2d7-105">Using the Query Functions</span></span>

<span data-ttu-id="4f2d7-106">Il existe quatre fonctions de requête pour obtenir des variables d’État simples et une pour déterminer si un état particulier est activé ou désactivé :</span><span class="sxs-lookup"><span data-stu-id="4f2d7-106">There are four query functions for obtaining simple state variables and one for determining whether a particular state is enabled or disabled:</span></span>

-   [<span data-ttu-id="4f2d7-107">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="4f2d7-107">**glGetBooleanv**</span></span>](glgetbooleanv.md)
-   [<span data-ttu-id="4f2d7-108">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="4f2d7-108">**glGetIntegerv**</span></span>](glgetintegerv.md)
-   [<span data-ttu-id="4f2d7-109">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="4f2d7-109">**glGetFloatv**</span></span>](glgetfloatv.md)
-   [<span data-ttu-id="4f2d7-110">**glGetDoublev**</span><span class="sxs-lookup"><span data-stu-id="4f2d7-110">**glGetDoublev**</span></span>](glgetdoublev.md)
-   [<span data-ttu-id="4f2d7-111">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="4f2d7-111">**glIsEnabled**</span></span>](glisenabled.md)

<span data-ttu-id="4f2d7-112">Les prototypes des fonctions de requête sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="4f2d7-112">The prototypes for the query functions are:</span></span>

<span data-ttu-id="4f2d7-113">**void** **glGetBooleanv**(**GLenum** *pname* , **GLboolean \*** *params* );</span><span class="sxs-lookup"><span data-stu-id="4f2d7-113">**void** **glGetBooleanv**(**GLenum** *pname* , **GLboolean \*** *params* );</span></span>

<span data-ttu-id="4f2d7-114">**void** **glGetIntegerv**(**GLenum** *pname* , **glint \*** *params* );</span><span class="sxs-lookup"><span data-stu-id="4f2d7-114">**void** **glGetIntegerv**(**GLenum** *pname* , **GLint \*** *params* );</span></span>

<span data-ttu-id="4f2d7-115">**void** **glGetFloatv**(**GLenum** *pname* , **GLfloat \*** *params* );</span><span class="sxs-lookup"><span data-stu-id="4f2d7-115">**void** **glGetFloatv**(**GLenum** *pname* , **GLfloat \*** *params* );</span></span>

<span data-ttu-id="4f2d7-116">**void** **glGetDoublev**(**GLenum** *pname* , **GLdouble \*** *params* );</span><span class="sxs-lookup"><span data-stu-id="4f2d7-116">**void** **glGetDoublev**(**GLenum** *pname* , **GLdouble \*** *params* );</span></span>

<span data-ttu-id="4f2d7-117">Respectivement, les fonctions de requête obtiennent des variables d’État booléennes, entières, à virgule flottante ou à double précision.</span><span class="sxs-lookup"><span data-stu-id="4f2d7-117">Respectively, the query functions obtain Boolean, integer, floating-point, or double-precision state variables.</span></span> <span data-ttu-id="4f2d7-118">Le paramètre *pname* est une constante symbolique indiquant la variable d’État à retourner, et *params* est un pointeur vers un tableau du type indiqué dans lequel placer les données retournées.</span><span class="sxs-lookup"><span data-stu-id="4f2d7-118">The *pname* parameter is a symbolic constant indicating the state variable to return, and *params* is a pointer to an array of the indicated type in which to place the returned data.</span></span> <span data-ttu-id="4f2d7-119">Les valeurs possibles pour *pname* sont répertoriées dans les [variables d’État OpenGL](opengl-state-variables.md).</span><span class="sxs-lookup"><span data-stu-id="4f2d7-119">The possible values for *pname* are listed in [OpenGL State Variables](opengl-state-variables.md).</span></span> <span data-ttu-id="4f2d7-120">Une conversion de type est effectuée si nécessaire pour retourner la variable souhaitée en tant que type de données demandé.</span><span class="sxs-lookup"><span data-stu-id="4f2d7-120">A type conversion is performed if necessary to return the desired variable as the requested data type.</span></span>

<span data-ttu-id="4f2d7-121">Le prototype de [**glIsEnabled**](glisenabled.md) est le suivant :</span><span class="sxs-lookup"><span data-stu-id="4f2d7-121">The prototype for [**glIsEnabled**](glisenabled.md) is:</span></span>

<span data-ttu-id="4f2d7-122">**GLboolean** **glIsEnabled**(GLenum *Cap* );</span><span class="sxs-lookup"><span data-stu-id="4f2d7-122">**GLboolean** **glIsEnabled**(GLenum *cap* );</span></span>

<span data-ttu-id="4f2d7-123">Si le mode spécifié par *Cap* est activé, **glIsEnabled** retourne la \_ valeur GL true.</span><span class="sxs-lookup"><span data-stu-id="4f2d7-123">If the mode specified by *cap* is enabled, **glIsEnabled** returns GL\_TRUE.</span></span> <span data-ttu-id="4f2d7-124">Si le mode spécifié par *Cap* est désactivé, **glIsEnabled** retourne GL \_ false.</span><span class="sxs-lookup"><span data-stu-id="4f2d7-124">If the mode specified by *cap* is disabled, **glIsEnabled** returns GL\_FALSE.</span></span> <span data-ttu-id="4f2d7-125">Les valeurs possibles pour *Cap* sont répertoriées dans les [variables d’État OpenGL](opengl-state-variables.md).</span><span class="sxs-lookup"><span data-stu-id="4f2d7-125">The possible values for *cap* are listed in [OpenGL State Variables](opengl-state-variables.md).</span></span>

<span data-ttu-id="4f2d7-126">D’autres fonctions spécialisées retournent des variables d’État spécifiques.</span><span class="sxs-lookup"><span data-stu-id="4f2d7-126">Other specialized functions return specific state variables.</span></span> <span data-ttu-id="4f2d7-127">Pour savoir quand utiliser ces fonctions, consultez la page variables d’État OpenGL et le *Manuel de référence OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="4f2d7-127">To find out when to use these functions, see OpenGL State Variables and the *OpenGL Reference Manual*.</span></span> <span data-ttu-id="4f2d7-128">Pour plus d’informations sur la fonctionnalité de gestion des erreurs de OpenGL et la fonction **glGetError** , consultez [gestion des erreurs](error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="4f2d7-128">For more information on OpenGL's error handling facility and the **glGetError** function, see [Error Handling](error-handling.md).</span></span>

<span data-ttu-id="4f2d7-129">Les fonctions qui retournent des variables d’État spécifiques sont :</span><span class="sxs-lookup"><span data-stu-id="4f2d7-129">The functions that return specific state variables are:</span></span>

-   [<span data-ttu-id="4f2d7-130">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="4f2d7-130">**glGetClipPlane**</span></span>](glgetclipplane.md)
-   [<span data-ttu-id="4f2d7-131">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="4f2d7-131">**glGetError**</span></span>](glgeterror.md)
-   [<span data-ttu-id="4f2d7-132">**glGetLight**</span><span class="sxs-lookup"><span data-stu-id="4f2d7-132">**glGetLight**</span></span>](glgetlight.md)
-   [<span data-ttu-id="4f2d7-133">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="4f2d7-133">**glGetMap**</span></span>](glgetmap.md)
-   [<span data-ttu-id="4f2d7-134">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="4f2d7-134">**glGetMaterial**</span></span>](glgetmaterial.md)
-   [<span data-ttu-id="4f2d7-135">**glGetPixelMap**</span><span class="sxs-lookup"><span data-stu-id="4f2d7-135">**glGetPixelMap**</span></span>](glgetpixelmap.md)
-   [<span data-ttu-id="4f2d7-136">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="4f2d7-136">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)
-   [<span data-ttu-id="4f2d7-137">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="4f2d7-137">**glGetString**</span></span>](glgetstring.md)
-   [<span data-ttu-id="4f2d7-138">**glGetTexEnv**</span><span class="sxs-lookup"><span data-stu-id="4f2d7-138">**glGetTexEnv**</span></span>](glgettexenv.md)
-   [<span data-ttu-id="4f2d7-139">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="4f2d7-139">**glGetTexGen**</span></span>](glgettexgen.md)
-   [<span data-ttu-id="4f2d7-140">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="4f2d7-140">**glGetTexImage**</span></span>](glgetteximage.md)
-   [<span data-ttu-id="4f2d7-141">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="4f2d7-141">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
-   [<span data-ttu-id="4f2d7-142">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="4f2d7-142">**glGetTexParameter**</span></span>](glgettexparameter.md)

 

 




