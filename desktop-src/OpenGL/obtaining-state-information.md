---
title: Obtention d’informations d’État
description: Obtention d’informations d’État
ms.assetid: 86fc8503-92b9-4b5b-8a28-4c9783983ac6
keywords:
- OpenGL, informations d’État
- OpenGL, variables d’État
- informations d’État OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8329fd34fc68122be8d63e4dc28756f88faf7797
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120684"
---
# <a name="obtaining-state-information"></a><span data-ttu-id="14094-106">Obtention d’informations d’État</span><span class="sxs-lookup"><span data-stu-id="14094-106">Obtaining State Information</span></span>

<span data-ttu-id="14094-107">OpenGL gère de nombreuses variables d’État qui affectent le comportement de nombreuses fonctions.</span><span class="sxs-lookup"><span data-stu-id="14094-107">OpenGL maintains many state variables that affect the behavior of many functions.</span></span> <span data-ttu-id="14094-108">Certaines de ces variables ont des fonctions de requête spécialisées.</span><span class="sxs-lookup"><span data-stu-id="14094-108">Some of these variables have specialized query functions.</span></span>

:::row:::
    :::column:::
        [<span data-ttu-id="14094-109">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="14094-109">**glGetClipPlane**</span></span>](glgetclipplane.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="14094-110">**glGetPixelMap**</span><span class="sxs-lookup"><span data-stu-id="14094-110">**glGetPixelMap**</span></span>](glgetpixelmap.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="14094-111">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="14094-111">**glGetTexImage**</span></span>](glgetteximage.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [<span data-ttu-id="14094-112">**glGetLight**</span><span class="sxs-lookup"><span data-stu-id="14094-112">**glGetLight**</span></span>](glgetlight.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="14094-113">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="14094-113">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="14094-114">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="14094-114">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [<span data-ttu-id="14094-115">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="14094-115">**glGetMap**</span></span>](glgetmap.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="14094-116">**glGetTexEnv**</span><span class="sxs-lookup"><span data-stu-id="14094-116">**glGetTexEnv**</span></span>](glgettexenv.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="14094-117">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="14094-117">**glGetTexParameter**</span></span>](glgettexparameter.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [<span data-ttu-id="14094-118">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="14094-118">**glGetMaterial**</span></span>](glgetmaterial.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="14094-119">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="14094-119">**glGetTexGen**</span></span>](glgettexgen.md)
    :::column-end:::
    :::column:::

    :::column-end:::
:::row-end:::

<span data-ttu-id="14094-120">Pour obtenir la valeur d’autres variables d’État, utilisez [**glGetBooleanv**](glgetbooleanv.md), [**glGetDoublev**](glgetdoublev.md), [**glGetFloatv**](glgetfloatv.md)ou [**glGetIntegerv**](glgetintegerv.md), selon le cas.</span><span class="sxs-lookup"><span data-stu-id="14094-120">To obtain the value of other state variables, use [**glGetBooleanv**](glgetbooleanv.md), [**glGetDoublev**](glgetdoublev.md), [**glGetFloatv**](glgetfloatv.md), or [**glGetIntegerv**](glgetintegerv.md), as appropriate.</span></span> <span data-ttu-id="14094-121">Pour plus d’informations sur l’utilisation de ces fonctions, consultez [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) .</span><span class="sxs-lookup"><span data-stu-id="14094-121">See [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) for information about how to use these functions.</span></span> <span data-ttu-id="14094-122">Les autres fonctions de requête que vous pouvez utiliser sont [**glGetError**](glgeterror.md), [**glGetString**](glgetstring.md)et [**glIsEnabled**](glisenabled.md).</span><span class="sxs-lookup"><span data-stu-id="14094-122">Other query functions you might want to use are [**glGetError**](glgeterror.md), [**glGetString**](glgetstring.md), and [**glIsEnabled**](glisenabled.md).</span></span> <span data-ttu-id="14094-123">(Pour plus d’informations sur les fonctions liées à la gestion des erreurs, consultez [gestion des erreurs](handling-errors.md) .) Pour enregistrer et restaurer des ensembles de variables d’État, utilisez [**glPushAttrib**](glpushattrib.md) et [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="14094-123">(See [Handling Errors](handling-errors.md) for more information about functions related to error handling.) To save and restore sets of state variables, use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span>

-   [<span data-ttu-id="14094-124">Utilisation des fonctions de requête</span><span class="sxs-lookup"><span data-stu-id="14094-124">Using the Query Functions</span></span>](using-the-query-functions.md)
-   [<span data-ttu-id="14094-125">Gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="14094-125">Error Handling</span></span>](error-handling.md)
-   [<span data-ttu-id="14094-126">Codes d’erreur OpenGL</span><span class="sxs-lookup"><span data-stu-id="14094-126">OpenGL Error Codes</span></span>](opengl-error-codes.md)
-   [<span data-ttu-id="14094-127">Enregistrement et restauration de jeux de variables d’État</span><span class="sxs-lookup"><span data-stu-id="14094-127">Saving and Restoring Sets of State Variables</span></span>](saving-and-restoring-sets-of-state-variables.md)
-   [<span data-ttu-id="14094-128">Variables d’État OpenGL</span><span class="sxs-lookup"><span data-stu-id="14094-128">OpenGL State Variables</span></span>](opengl-state-variables.md)
-   [<span data-ttu-id="14094-129">Informations de référence sur l’État</span><span class="sxs-lookup"><span data-stu-id="14094-129">State Information Reference</span></span>](state-information-reference.md)

 

 




