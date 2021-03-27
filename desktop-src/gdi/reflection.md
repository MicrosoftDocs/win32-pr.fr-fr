---
description: Certaines applications fournissent des fonctionnalités qui reflètent (ou miroir) des objets dessinés dans la zone cliente.
ms.assetid: 2205dc3c-ca4b-4a0a-be3e-0332ce8467a0
title: Réflexion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d8e327af098a4e232e2a6734b37a17a1ac85f19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972550"
---
# <a name="reflection"></a><span data-ttu-id="b295c-103">Réflexion</span><span class="sxs-lookup"><span data-stu-id="b295c-103">Reflection</span></span>

<span data-ttu-id="b295c-104">Certaines applications fournissent des fonctionnalités qui reflètent (ou miroir) des objets dessinés dans la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="b295c-104">Some applications provide features that reflect (or mirror) objects drawn in the client area.</span></span> <span data-ttu-id="b295c-105">Les applications qui contiennent des fonctionnalités de réflexion utilisent la fonction [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) pour définir les valeurs appropriées dans l’espace universel pour la transformation d’espace de page.</span><span class="sxs-lookup"><span data-stu-id="b295c-105">Applications that contain reflection capabilities use the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set the appropriate values in the world-space to page-space transformation.</span></span> <span data-ttu-id="b295c-106">Cette fonction reçoit un pointeur vers une structure [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) contenant les valeurs appropriées.</span><span class="sxs-lookup"><span data-stu-id="b295c-106">This function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="b295c-107">Les membres eM11 et eM22 de XFORM spécifient respectivement les composants de réflexion horizontale et verticale.</span><span class="sxs-lookup"><span data-stu-id="b295c-107">The eM11 and eM22 members of XFORM specify the horizontal and vertical reflection components, respectively.</span></span>

<span data-ttu-id="b295c-108">La *transformation de réflexion* crée une image miroir d’un objet par rapport à l’axe x ou y.</span><span class="sxs-lookup"><span data-stu-id="b295c-108">The *reflection transformation* creates a mirror image of an object with respect to either the x- or y-axis.</span></span> <span data-ttu-id="b295c-109">En résumé, la réflexion n’est qu’une mise à l’échelle négative.</span><span class="sxs-lookup"><span data-stu-id="b295c-109">In short, reflection is just negative scaling.</span></span> <span data-ttu-id="b295c-110">Pour produire une réflexion horizontale, les coordonnées x sont multipliées par 1.</span><span class="sxs-lookup"><span data-stu-id="b295c-110">To produce a horizontal reflection, x-coordinates are multiplied by 1.</span></span> <span data-ttu-id="b295c-111">Pour produire une réflexion verticale, les coordonnées y sont multipliées par 1.</span><span class="sxs-lookup"><span data-stu-id="b295c-111">To produce a vertical reflection, y-coordinates are multiplied by 1.</span></span>

<span data-ttu-id="b295c-112">La réflexion horizontale peut être représentée par l’algorithme suivant :</span><span class="sxs-lookup"><span data-stu-id="b295c-112">Horizontal reflection can be represented by the following algorithm:</span></span>

``` syntax
x' = -x 
```

<span data-ttu-id="b295c-113">où x est la coordonnée x et x’est le résultat de la réflexion.</span><span class="sxs-lookup"><span data-stu-id="b295c-113">where x is the x-coordinate and x' is the result of the reflection.</span></span>

<span data-ttu-id="b295c-114">La matrice 2 par 2 qui a produit une réflexion horizontale contient les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="b295c-114">The 2-by-2 matrix that produced horizontal reflection contains the following values:</span></span>

``` syntax
|-1    0| 
|0     1| 
```

<span data-ttu-id="b295c-115">La réflexion verticale peut être représentée par l’algorithme suivant :</span><span class="sxs-lookup"><span data-stu-id="b295c-115">Vertical reflection can be represented by the following algorithm:</span></span>

``` syntax
y' = -y 
```

<span data-ttu-id="b295c-116">où y est la coordonnée y et y est le résultat de la réflexion.</span><span class="sxs-lookup"><span data-stu-id="b295c-116">where y is the y-coordinate and y' is the result of the reflection.</span></span>

<span data-ttu-id="b295c-117">La matrice 2-par-2 qui a produit la réflexion verticale contient les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="b295c-117">The 2-by-2 matrix that produced vertical reflection contains the following values:</span></span>

``` syntax
|1    0| 
|0   -1| 
```

<span data-ttu-id="b295c-118">Les opérations de réflexion horizontale et de réflexion verticale peuvent être combinées en une seule opération à l’aide de la matrice 2 par 2 suivante :</span><span class="sxs-lookup"><span data-stu-id="b295c-118">The horizontal-reflection and vertical-reflection operations can be combined into a single operation by using the following 2-by-2 matrix:</span></span>

``` syntax
|-1    0| 
|0    -1| 
```

 

 



