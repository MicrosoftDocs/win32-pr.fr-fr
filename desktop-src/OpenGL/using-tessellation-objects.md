---
title: Utilisation d’objets pavage
description: Comme un polygone complexe est décrit et fractionné, il requiert des données associées, telles que les vertex, les bords et les fonctions de rappel.
ms.assetid: b6102e25-280c-4d0d-9350-d0038d1a0306
keywords:
- Utilitaire OpenGL (GLU), pavage d’objets
- GLU (utilitaire OpenGL), pavage d’objets
- pavage d’objets OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 590ab571e656fcd346da265bfa921cb965fdf540
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309638"
---
# <a name="using-tessellation-objects"></a><span data-ttu-id="885df-106">Utilisation d’objets pavage</span><span class="sxs-lookup"><span data-stu-id="885df-106">Using Tessellation Objects</span></span>

<span data-ttu-id="885df-107">Comme un polygone complexe est décrit et fractionné, il requiert des données associées, telles que les vertex, les bords et les fonctions de rappel.</span><span class="sxs-lookup"><span data-stu-id="885df-107">As a complex polygon is being described and tessellated, it requires associated data, such as the vertices, edges, and callback functions.</span></span> <span data-ttu-id="885df-108">Toutes ces données sont liées à un seul objet de pavage.</span><span class="sxs-lookup"><span data-stu-id="885df-108">All this data is tied to a single tessellation object.</span></span> <span data-ttu-id="885df-109">Pour paver un polygone, vous utilisez d’abord la fonction [**gluNewTess**](glunewtess.md) qui crée un nouvel objet pavage et retourne un pointeur vers celui-ci.</span><span class="sxs-lookup"><span data-stu-id="885df-109">To tessellate a polygon, you first use the [**gluNewTess**](glunewtess.md) function which creates a new tessellation object and returns a pointer to it.</span></span> <span data-ttu-id="885df-110">Un pointeur null est retourné si la fonction échoue.</span><span class="sxs-lookup"><span data-stu-id="885df-110">A null pointer is returned if the function fails.</span></span>

<span data-ttu-id="885df-111">Si vous n’avez plus besoin d’un objet polygonalisation, vous pouvez le supprimer et libérer toute la mémoire associée avec [**gluDeleteTess**](gludeletetess.md).</span><span class="sxs-lookup"><span data-stu-id="885df-111">If you no longer need a tessellation object, you can delete it and free all associated memory with [**gluDeleteTess**](gludeletetess.md).</span></span>

<span data-ttu-id="885df-112">Vous pouvez réutiliser un seul objet pavage pour tous vos pavages.</span><span class="sxs-lookup"><span data-stu-id="885df-112">You can reuse a single tessellation object for all your tessellations.</span></span> <span data-ttu-id="885df-113">Cet objet est requis uniquement parce que les fonctions de bibliothèque peuvent avoir besoin d’effectuer leurs propres pavages, et qu’ils doivent pouvoir le faire sans interférer avec les facettes que votre programme exécute.</span><span class="sxs-lookup"><span data-stu-id="885df-113">This object is required only because library functions may need to do their own tessellations, and they should be able to do so without interfering with any tessellation that your program is performing.</span></span> <span data-ttu-id="885df-114">Plusieurs objets de pavage sont également utiles si vous souhaitez utiliser différents jeux de rappels pour différents pavages.</span><span class="sxs-lookup"><span data-stu-id="885df-114">Multiple tessellation objects are also useful if you want to use different sets of callbacks for different tessellations.</span></span> <span data-ttu-id="885df-115">En général, toutefois, vous allouez un seul objet pavage et l’utilisez pour tous les pavages.</span><span class="sxs-lookup"><span data-stu-id="885df-115">Typically, however, you allocate a single tessellation object and use it for all the tessellations.</span></span> <span data-ttu-id="885df-116">Il n’y a pas vraiment besoin de le libérer, car il utilise une petite quantité de mémoire.</span><span class="sxs-lookup"><span data-stu-id="885df-116">There's no real need to free it, because it uses a small amount of memory.</span></span> <span data-ttu-id="885df-117">En revanche, si vous écrivez une fonction de bibliothèque qui utilise le pavage GLU, veillez à libérer tous les objets de pavage que vous créez.</span><span class="sxs-lookup"><span data-stu-id="885df-117">On the other hand, if you're writing a library function that uses GLU tessellation, be careful to free any tessellation objects you create.</span></span>

 

 




